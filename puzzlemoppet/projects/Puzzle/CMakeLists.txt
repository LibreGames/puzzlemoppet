# Only things that need changing here.

set(projectName puzzlemoppet)

set(sourceFiles
main.cpp
Level.cpp
Map.cpp
Events.cpp
Editor.cpp
#MonsterCharacterController.cpp
#MainMenu.cpp
Positioner.cpp
#RoundedGUISkin.cpp
MainState.cpp
StartScreen.cpp
SimpleMenu.cpp
EndLevelScreen.cpp
level_stats.cpp
volume.cpp
options.cpp
)


# No need to modify these lines.
add_executable(${projectName} ${sourceFiles})
if (projectProperties)
	set_target_properties(${projectName} ${projectProperties})
endif (projectProperties)
target_link_libraries(${projectName} ${projectLibs})

install(TARGETS ${projectName} RUNTIME DESTINATION bin)
