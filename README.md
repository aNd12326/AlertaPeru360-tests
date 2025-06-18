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

US19.feature
Feature: Personalizar tipos de alertas

  Como usuario
  quiero configurar qué tipos de desastres recibir
  para evitar notificaciones irrelevantes.

  Scenario: Filtro de alertas por tipo
    Dado que ingreso a configuración de alerta
    Cuando selecciono solo SISMOS y HUAICOS
    Entonces solo recibo notificaciones relacionadas con esos eventos

 US41.feature
 Feature: Registro de usuario

  Como habitante de localidad en zona de riesgo
  quiero registrarme en la plataforma
  para informarme y recibir alertas sobre desastres naturales.

  Scenario: Registro exitoso
    Dado que soy usuario nuevo
    Cuando completo los campos necesarios como nombres, correo y ubicación y hago clic en “Crear cuenta”
    Entonces mi cuenta fue creada
    
US32.feature
Feature: Ver nivel de peligro actual en mi zona

  Como usuario
  quiero saber el nivel de riesgo actual (bajo, medio, alto)
  para prepararme mejor.

  Scenario: Indicador visual del nivel de peligro
    Dado que abro la app
    Cuando accedo a “Estado actual”
    Entonces veo un semáforo de riesgo basado en datos oficiales

US29.feature
Feature: Notificación de eventos climáticos extremos

  Como usuario
  quiero ser alertado ante tormentas o vientos intensos
  para tomar precauciones.

  Scenario: Alerta meteorológica
    Dado que se emite una alerta de SENAMHI
    Cuando estoy en zona afectada
    Entonces recibo una notificación prioritaria

 US16.feature
 Feature: Consulta de historial de desastres

  Como usuario
  quiero revisar eventos pasados en mi distrito
  para entender qué tipo de emergencias son frecuentes.

  Scenario: Historial por distrito
    Dado que quiero informarme sobre riesgos
    Cuando consulto mi distrito en la app
    Entonces veo un listado con fechas y tipos de desastres anteriores

US02.feature
Feature: Acceso a guías de primeros auxilios

  Como ciudadano que enfrenta una emergencia
  quiero acceder a instrucciones claras y visuales para aplicar primeros auxilios
  para poder ayudar a una persona herida de manera rápida y correcta antes de recibir atención médica.

  Scenario: Ver guías de primeros auxilios
    Dado que el usuario está en el modo emergencia
    Cuando accede a la sección de “Primeros auxilios” desde el modo emergencia
    Entonces la app muestra todas las guías de primeros auxilios

  Scenario: Consultar guías de primeros auxilios sin conexión
    Dado que no tengo conexión a internet
    Cuando ingreso al módulo de primeros auxilios
    Entonces la app debe mostrar el contenido previamente descargado para poder actuar sin necesidad de red



