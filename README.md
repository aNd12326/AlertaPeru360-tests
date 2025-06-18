# AlertaPeru360 acceptance test

US05.feature

Feature: Llamar a emergencias desde el Modo Emergencia

  Como ciudadano que enfrenta una emergencia médica
  quiero poder llamar rápidamente a una ambulancia desde el Modo Emergencia
  para recibir atención urgente sin perder tiempo buscando el número.

  Scenario: Llamar a un contacto de emergencia
    Dado que el usuario ingresa al Modo Emergencia por una situación médica
    Cuando selecciona la opción "Contactos de Emergencia" y presiona "Ambulancia"
    Entonces debe llamar automáticamente a la ambulancia sin pérdida de tiempo

  Scenario: Llamar a otro contacto de emergencia tras demora
    Dado que el usuario ingresa al Modo Emergencia por una situación médica
    Y la llamada a la ambulancia demora más de 30 segundos en ser atendida
    Cuando selecciona "Cancelar llamada"
    Entonces debe ser redirigido a la pantalla anterior para llamar a otro contacto de emergencia
