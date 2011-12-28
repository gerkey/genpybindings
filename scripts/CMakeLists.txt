install(FILES module.cpp.template msg.cpp.template srv.cpp.template __init__.py
  DESTINATION share/genpybindings
  )

install(FILES gen_pybindings.py
  DESTINATION share/genpybindings/bin
  )