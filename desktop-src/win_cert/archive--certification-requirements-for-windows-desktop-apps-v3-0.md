---
title: Requisitos de certificación de Windows Desktop Apps v3.0
description: Document version 3.0Document date June 29, 2012This document contains the technical requirements and eligibility qualifications that a desktop app must meet in order to participate in the Windows 8 Desktop App Certification Program.
ms.assetid: 7107EF93-8401-481A-B433-8C36A539D790
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13af9f9cb0464ff7f0f9c57f057685b360d09928
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359584"
---
# <a name="archive-certification-requirements-for-windows-desktop-apps-v30"></a>Archivo: Requisitos de certificación para Windows Desktop Apps v3.0

**Versión del documento:** 3.0

**Fecha del documento:** 29 de junio de 2012

Este documento contiene los requisitos técnicos y los requisitos de idoneidad que debe cumplir una aplicación de escritorio para participar en el programa de certificación de aplicaciones Windows 8 escritorio. Para Windows 7, este programa se conocía como el programa Windows logotipo de software.

## <a name="welcome"></a>¡Bienvenido!

La Windows admite un amplio ecosistema de productos y asociados. Mostrar el Windows en el producto representa una relación y un compromiso compartido con la calidad entre Microsoft y su empresa. Los clientes confían Windows marca en el producto porque garantiza que cumple los estándares de compatibilidad y funciona bien en la plataforma Windows cliente. Pasar correctamente Windows certificación de aplicaciones permite que la aplicación se muestre en el Centro de compatibilidad de Windows y también es un paso necesario para enumerar una referencia de aplicación de escritorio en Windows Store.

El Programa de certificación de aplicaciones de Windows se conste de requisitos técnicos y de programa para ayudar a garantizar que las aplicaciones de terceros que llevan la marca Windows son fáciles de instalar y confiables en equipos que ejecutan Windows. Los clientes valoran la estabilidad, la compatibilidad, la confiabilidad, el rendimiento y la calidad en los sistemas que adquieren. Microsoft centra sus inversiones en cumplir estos requisitos para las aplicaciones de software diseñadas para ejecutarse Windows plataforma de equipos. Estos esfuerzos incluyen pruebas de compatibilidad para la coherencia de la experiencia, un rendimiento mejorado y una seguridad mejorada en equipos que ejecutan Windows software. Las pruebas de compatibilidad de Microsoft se han diseñado en colaboración con asociados del sector y se mejoran continuamente en respuesta a los desarrollos del sector y a la demanda de los consumidores.

El Windows App Certification Kit se usa para validar el cumplimiento de estos requisitos y reemplaza el WSLK usado para la validación en el programa Windows 7 Software Logo. El Windows App Certification Kit es uno de los componentes incluidos en el Kit de desarrollo de software (SDK) de Windows para Windows 8. También se integra en Microsoft Visual Studio 2012 Express para Windows 8.

## <a name="app-eligibility"></a>Elegibilidad de la aplicación

Para que una aplicación cumpla los requisitos Windows 8 certificación de aplicación de escritorio debe cumplir los siguientes criterios y todos los requisitos técnicos enumerados en este documento.

-   Debe ser una aplicación independiente.
-   Debe ejecutarse en un equipo Windows 8.1 local.
-   Puede ser un componente de cliente de una aplicación Windows Server certificada
-   Debe ser código y característica completadas

## <a name="1-apps-are-compatible-and-resilient"></a>1. Las aplicaciones son compatibles y resistentes

Las veces en que una aplicación se bloquea o deja de responder provoca mucha frustración del usuario. Se espera que las aplicaciones sean resistentes y estables, y eliminar estos errores ayuda a garantizar que el software sea más predecible, fácil de mantener, de rendimiento y de confianza.<dl> 1.1 La aplicación no debe tener una dependencia de los modos de compatibilidad Windows, el mensaje AppHelp ni ninguna otra corrección de compatibilidad.  
1.2 La aplicación no debe tener una dependencia en el tiempo de ejecución de VB6  
1.3 La aplicación no debe cargar archivos DLL arbitrarios para interceptar llamadas API win32 mediante dll de Microsoft Windows NT CurrentVersion de HKLM \\ Software \\ Windows \\ \\ \\ \_ AppInit.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. Las aplicaciones deben cumplir los Windows recomendados de seguridad

El Windows recomendados de seguridad le ayudará a evitar la exposición a Windows superficies expuestas a ataques. Las superficies de ataque son los puntos de entrada que un atacante malintencionado podría usar para aprovechar el sistema operativo aprovechando las vulnerabilidades del software de destino. Una de las peores vulnerabilidades de seguridad es la elevación de privilegios.

<dl> 2.1 La aplicación debe usar acl seguras y adecuadas <a href="/windows/desktop/SecAuthZ/access-control-lists">para</a> proteger archivos ejecutables  
2.2 La aplicación debe usar acl seguras <a href="/windows/desktop/SecAuthZ/access-control-lists">y</a> adecuadas para proteger directorios  
2.3 La aplicación debe usar acl seguras y adecuadas <a href="/windows/desktop/SecAuthZ/access-control-lists">para</a> proteger las claves del Registro  
2.4 La aplicación debe <a href="/windows/desktop/SecAuthZ/access-control-lists"></a> usar ACL seguras y adecuadas para proteger los directorios que contienen objetos.  
2.5 La aplicación debe reducir el acceso que no sea de administrador a los servicios vulnerables a la manipulación.  
2.6 La aplicación debe evitar que los servicios con reinicios rápidos se reinicien más de dos veces cada 24 horas.
</dl>**Nota: El acceso solo se debe conceder a las entidades que lo requieran.**

El Windows de certificación de aplicaciones de Windows comprobará que las superficies de ataque de Windows no se exponen comprobando que las ACL y los servicios se implementan de forma que no ponga en riesgo el sistema Windows.

## <a name="3-apps-support-windows-security-features"></a>3. Las aplicaciones admiten Windows de seguridad

El Windows operativo tiene muchas características que admiten la seguridad y la privacidad del sistema. Las aplicaciones deben admitir estas características para mantener la integridad del sistema operativo. Las aplicaciones compiladas incorrectamente podrían provocar saturaciones de búfer que, a su vez, pueden provocar denegación de servicio o permitir la ejecución de código malintencionado. <dl> 3.1 La aplicación no debe usar AllowPartiallyTrustedCallersAttribute (APTCA) para garantizar el acceso seguro a ensamblados con nombre seguro  
3.2 La aplicación debe compilarse con la marca /SafeSEH para garantizar el control seguro de excepciones  
3.3 La aplicación debe compilarse con la marca /NXCOMPAT para evitar la ejecución de datos  
3.4 La aplicación debe compilarse con la marca /DYNAMICBASE para la selección aleatoria del diseño del espacio de direcciones (ASLR)  
3.5 La aplicación no debe leer ni escribir las secciones de PE compartido  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. Las aplicaciones deben cumplir los mensajes del administrador de reinicio del sistema

Cuando los usuarios inician el apagado, normalmente tienen un gran deseo de ver que el cierre se realiza correctamente. es posible que se desespejen de la oficina y solo quieran que sus equipos se apaguen. Las aplicaciones deben respetar este deseo al no bloquear el cierre. Aunque en la mayoría de los casos, un apagado puede no ser crítico, las aplicaciones deben estar preparadas para la posibilidad de un apagado crítico.<dl> 4.1 La aplicación debe controlar los apagados críticos correctamente <dl> En un cierre crítico, las aplicaciones que devuelven FALSE a WM QUERYENDSESSION se enviarán a WM ENDSESSION y se cerrarán, mientras que aquellas que se queden sin tiempo de espera en respuesta a \_ \_ WM QUERYENDSESSION se \_ finalizarán.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ QUERYENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Las aplicaciones de consola pueden llamar a SetConsoleCtrlHandler para especificar la función que controlará las notificaciones de apagado. Las aplicaciones de servicio pueden llamar a RegisterServiceCtrlHandlerEx para especificar la función que recibirá notificaciones de cierre.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> WM \_ ENDSESSION con LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Como mínimo, la aplicación debe prepararse guardando los datos de usuario y el estado de la información necesaria después de un reinicio.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>**Note: Apps that must block shutdown because of an operation that cannot be interrupted should explain the reason to the user.** Use ShutdownBlockReasonCreate to register a string that explains the reason to the user. When the operation has completed, the app should call ShutdownBlockReasonDestroy to indicate that the system can be shut down.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. Las aplicaciones deben admitir una instalación limpia y reversible

Una instalación limpia, reversible, permite a los usuarios administrar (implementar y quitar) correctamente aplicaciones en sus sistemas.<dl> 5.1 La aplicación debe implementar correctamente una instalación limpia y reversible <dl> Si se produce un error en la instalación, la aplicación debería poder revertirla y restaurar la máquina a su estado anterior.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Reiniciar el equipo nunca debe ser la única opción al final de una instalación o actualización. Los usuarios deben tener la oportunidad de reiniciarse más adelante.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Windows herramientas de inventario y de telemetría requieren información completa sobre las aplicaciones instaladas. Si usa un instalador basado en MSI, MSI crea automáticamente las entradas del Registro siguientes. Si no usa un instalador msi, el módulo de instalación debe crear las siguientes entradas del Registro durante la instalación:  
</dl>

-   DisplayName
-   InstallLocation
-   Publisher
-   UninstallString
-   VersionMajor o MajorVersion
-   VersionMinor o MinorVersion

</dd> </dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. Las aplicaciones deben firmar digitalmente archivos y controladores

Una firma digital Authenticode permite a los usuarios asegurarse de que el software es original. También permite detectar si un archivo se ha alterado, por ejemplo, si se ha infectado por un virus. El cumplimiento de la firma de código en modo kernel es una característica de Windows conocida como integridad de código (CI), que mejora la seguridad del sistema operativo al comprobar la integridad de un archivo cada vez que la imagen del archivo se carga en la memoria. CI detecta si el código malintencionado ha modificado un archivo binario del sistema. También genera un evento de registro de diagnóstico y auditoría del sistema cuando la firma de un módulo de kernel no se puede comprobar correctamente. <dl> 6.1 Todos los archivos ejecutables (.exe, .dll, .ocx, .sys, .cpl, .drv, .scr) deben estar firmados con un certificado Authenticode  
6.2 Todos los controladores de modo kernel instalados por la aplicación deben tener una firma de Microsoft obtenida a través del Windows de certificación de hardware. Todos los controladores de filtro del sistema de archivos deben estar firmados por Microsoft.  
6.3 Excepciones y exenciones <dl> Las exenciones solo se considerarán para los redistribuibles de terceros sin firmar, excepto los controladores. Se requiere una prueba de comunicación que solicite una versión firmada de los redistribuibles para que se conceda esta exención.  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. Las aplicaciones no bloquean la instalación o el inicio de la aplicación en función de una comprobación de versión del sistema operativo

Es importante que los clientes no se bloqueen artificialmente para instalar o ejecutar su aplicación cuando no hay limitaciones técnicas. En general, si las aplicaciones se escribieron para Windows Vista o versiones posteriores de Windows, no deben tener que comprobar la versión del sistema operativo.<dl> 7.1 La aplicación no debe realizar comprobaciones de versión en busca de igualdad <dl> Si necesita una característica específica, compruebe si la propia característica está disponible. Si necesita Windows XP, compruebe si Windows XP o posterior (>= 5.1). De este modo, el código de detección seguirá funcionando en versiones futuras de Windows. Los instaladores de controladores y los módulos de desinstalación nunca deben comprobar la versión del sistema operativo.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   Las aplicaciones que se entregan como un paquete que también se ejecutan en Windows XP, Windows Vista y Windows 7, y necesitan comprobar la versión del sistema operativo para determinar qué componentes instalar en un sistema operativo determinado.
-   Aplicaciones que comprueban solo la versión mínima del sistema operativo (solo durante la instalación, no en tiempo de ejecución) mediante solo las llamadas API aprobadas y que enumera correctamente el requisito de versión mínima en el manifiesto de aplicación.
-   Aplicaciones de seguridad (antivirus, firewall, etc.), utilidades del sistema (por ejemplo, desfragmentación, copias de seguridad y herramientas de diagnóstico) que comprueban la versión del sistema operativo mediante solo las llamadas API aprobadas.

  
</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. Las aplicaciones no cargan servicios ni controladores en modo seguro

Caja fuerte modo permite a los usuarios diagnosticar y solucionar problemas Windows. Los controladores y servicios no deben establecerse para cargarse en modo seguro a menos que sean necesarios para las operaciones básicas del sistema de , como los controladores de dispositivos de almacenamiento o para fines de diagnóstico y recuperación, como los escáneres antivirus. De forma predeterminada, Windows está en modo seguro, inicia solo los controladores y servicios que se instalaron previamente con Windows.

-   8.1 Excepciones y exenciones <dl> Los controladores y servicios que deben iniciarse en modo seguro requieren una anulación. La solicitud de anulación debe incluir cada controlador o servicio aplicable escribiendo en las claves del Registro SafeBoot y describir los motivos técnicos por los que la aplicación o el servicio deben ejecutarse en modo seguro. El instalador de la aplicación debe registrar todos estos controladores y servicios mediante estas claves del Registro:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Nota:** Debe probar estos controladores y servicios para asegurarse de que funcionan en modo seguro sin errores.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. Las aplicaciones deben seguir las directrices de control de cuentas de usuario

Algunas Windows se ejecutan en el contexto de seguridad de una cuenta de administrador, y las aplicaciones a menudo solicitan derechos de usuario excesivos y Windows privilegios. El control del acceso a los recursos permite a los usuarios controlar sus sistemas y protegerlos frente a cambios no deseados. Un cambio no deseado puede ser malintencionado, como que un rootkit tome el control del equipo o sea el resultado de una acción realizada por personas con privilegios limitados. La regla más importante para controlar el acceso a los recursos es proporcionar la menor cantidad de acceso al contexto de usuario estándar necesario para que un usuario realice las tareas necesarias. Las siguientes directrices de control de cuentas de usuario (UAC) proporcionan a la aplicación los permisos necesarios cuando la aplicación los necesita, sin dejar el sistema expuesto constantemente a riesgos de seguridad. La mayoría de las aplicaciones no requieren privilegios de administrador en tiempo de ejecución y solo deben ejecutarse como un usuario estándar.<dl> 9.1 La aplicación debe tener un manifiesto que defina los niveles de ejecución e indique al sistema operativo qué privilegios requiere la aplicación para poder ejecutarse. <dl> El marcado del manifiesto de aplicación solo se aplica a los ARCHIVOS EX, no a los archivos DLL. Esto se debe a que UAC no inspecciona los archivos DLL durante la creación del proceso. También merece la pena tener en cuenta que las reglas de UAC no se aplican a servicios Microsoft. El manifiesto puede estar incrustado o externo.  
Para crear un manifiesto, cree un archivo con el nombre <nombre de la aplicación>.exe.manifest y almacéne en el mismo directorio \_ que el exe. Tenga en cuenta que cualquier manifiesto externo se omite si la aplicación tiene un manifiesto interno. Por ejemplo:  
<requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess="true \| false"""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Las características administrativas deben moverse a un proceso independiente que se ejecute con privilegios administrativos. Las aplicaciones orientadas al usuario, como las accesibles a través del grupo de programas en el menú Inicio, y que requieren elevación deben estar firmadas por Authenticode.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> Se requiere una exención para las aplicaciones que ejecutan su proceso principal con privilegios elevados (requireAdministrator o highestAvailable). El proceso principal se identifica como el punto de entrada del usuario a la aplicación. Se tendrán en cuenta las exenciones para los escenarios siguientes:

-   Herramientas administrativas o del sistema con el nivel de ejecución establecido en highestAvailable o requireAdministrator
-   Solo la aplicación de marco de automatización de la interfaz de usuario o accesibilidad establece la marca uiAccess en true para omitir el aislamiento de privilegios de la interfaz de usuario (UIPI). Para iniciar correctamente el uso de la aplicación, esta marca debe estar firmada por Authenticode y debe residir en una ubicación protegida en el sistema de archivos, es decir, Archivos de programa.

  
</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. Las aplicaciones deben instalarse en las carpetas correctas de forma predeterminada

Los usuarios deben tener una experiencia coherente y segura con la ubicación de instalación predeterminada de los archivos, al tiempo que mantienen la opción de instalar una aplicación en la ubicación que prefieran. También es necesario almacenar los datos de la aplicación en la ubicación correcta para permitir que varias personas usen el mismo equipo sin dañar ni sobrescribir los datos y la configuración de los demás. Windows proporciona ubicaciones específicas en el sistema de archivos para almacenar programas y componentes de software, datos de aplicación compartidos y datos de aplicación específicos de un usuario<dl> 10.1 La aplicación debe estar instalada de forma predeterminada en la carpeta Archivos de programa. <dl> Para aplicaciones nativas de 32 y 64 bits en %ProgramFiles%, y %ProgramFiles(x86)% para aplicaciones de 32 bits que se ejecutan en x64. Los datos de usuario o de aplicación nunca deben almacenarse en esta ubicación debido a los permisos de seguridad configurados para esta carpeta.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Por ejemplo, la aplicación no debe establecer ninguna de las siguientes opciones:  
</dl>

-   Claves de ejecución del Registro HKLM y, o HKCU, en Software \\ Microsoft \\ Windows \\ CurrentVersion
-   Claves de ejecución del Registro HKLM o HKCU en Software \\ Wow6432Node \\ Microsoft \\ windows \\ CurrentVersion
-   Menú Inicio AllPrograms > STARTUP

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\&lt;username&gt;\\AppData  
10.5 Your app must never write directly to the "Windows" directory and or subdirectories <dl> Use los métodos correctos para instalar archivos, como fuentes o controladores.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Cuando se instala la aplicación, no hay ninguna ubicación de usuario correcta en la que almacenar los datos. Los intentos de una aplicación para modificar los comportamientos de asociación predeterminados en el nivel de equipo después de la instalación no se realizarán correctamente. En su lugar, los valores predeterminados se deben reclamar en un nivel por usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados de los demás.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> Se requiere una exención para las aplicaciones que escriben en la caché global de ensamblados (GAC) las aplicaciones .NET deben mantener las dependencias de ensamblado privadas y almacenarla en el directorio de la aplicación a menos que se requiera explícitamente el uso compartido de un ensamblado.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. Las aplicaciones deben admitir sesiones de varios usuarios

Windows usuarios deben poder ejecutar sesiones simultáneas sin conflictos ni interrupciones.<dl> 11.1 La aplicación debe asegurarse de que, cuando se ejecuta en varias sesiones de forma local o remota, la funcionalidad normal de la aplicación no se ve afectada negativamente.  
11.2 La configuración de la aplicación y los archivos de datos no deben conservarse entre los usuarios  
11.3 La privacidad y las preferencias de un usuario deben aislarse en la sesión del usuario.  
11.4 Las instancias de la aplicación deben estar aisladas entre sí <dl> Esto significa que los datos de usuario de una instancia no son visibles para otra instancia de la aplicación. El sonido de una sesión de usuario inactiva no debe escucharse en una sesión de usuario activa. En los casos en los que varias instancias de la aplicación usan recursos compartidos, la aplicación debe asegurarse de que no haya ningún conflicto.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Consulte los requisitos de UAC.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>**Note:** If an app does not support multiple user sessions or remote access, it must clearly state this when launched from this kind of session.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. Las aplicaciones deben admitir versiones x64 de Windows

A medida que el hardware de 64 bits se vuelve más común, los usuarios esperan que los desarrolladores de aplicaciones aprovechen las ventajas de la arquitectura de 64 bits mediante la migración de sus aplicaciones a 64 bits o que las versiones de 32 bits de la aplicación se ejecuten bien en versiones de 64 bits de Windows.<dl> 12.1 La aplicación debe admitir de forma nativa aplicaciones de 64 bits o, como mínimo, aplicaciones basadas en Windows de 32 bits deben ejecutarse sin problemas en sistemas de 64 bits para mantener la compatibilidad con versiones de 64 bits de Windows  
12.2 La aplicación y sus instaladores no deben contener ningún código de 16 bits ni confiar en ningún componente de 16 bits  
12.3 El programa de instalación de la aplicación debe detectar e instalar los controladores y componentes adecuados para la arquitectura de 64 bits  
12.4 Los complementos de shell deben ejecutarse en versiones de 64 bits de Windows  
12.5 La aplicación que se ejecuta en el emulador de WoW64 no debe intentar subvertir ni omitir los mecanismos de virtualización Wow64 <dl> Si hay escenarios específicos en los que las aplicaciones necesitan detectar si se ejecutan en el emulador de WoW64, deben hacerlo llamando a IsWow64Process.  
</dl> </dd> </dl>

## <a name="conclusion"></a>Conclusión

A medida que estos requisitos evolucionan, se observan los cambios en el historial de revisiones siguiente. Los requisitos estables son fundamentales para realizar su mejor trabajo, por lo que nos aseguraremos de que los cambios que hacemos sean sostenibles y sigan protegiendo y mejorando las aplicaciones.

Gracias de nuevo por unirse a nuestro compromiso de ofrecer excelentes experiencias de cliente.

## <a name="revision-history"></a>Historial de revisiones



| Date         | Versión | Descripción de la revisión                   | Vínculo a documento                                                             |
|--------------|---------|----------------------------------------|------------------------------------------------------------------------------|
| 20 de diciembre de 2011 | 1.0     | Borrador inicial del documento para la versión preliminar. |                                                                              |
| 26 de enero de 2012 | 1.1     | Actualice a la \# sección 2.                 | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md) |
| 31 de mayo de 2012 | 1.2     | Se han agregado resultados de pruebas de resumen.             | [1.2](archive--certification-requirements-for-windows-desktop-apps-v1-2.md) |
| 29 de junio de 2012 | 3.0     | Windows 8 documento final               | 3.0                                                                          |



 

## <a name="learn-more-about-desktop-app-certification"></a>Más información sobre la certificación de aplicaciones de escritorio



| Requisito                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Más detalles                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compatibilidad y resistencia                                                    | Los bloqueos & bloqueos son una interrupción importante para los usuarios y causan frustración. Se espera que las aplicaciones sean resistentes y estables, ya que la eliminación de estos errores ayuda a garantizar que el software sea más predecible, fácil de mantener, de rendimiento y de confianza.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Windows Vista, Windows 7 y Windows 8 operativos](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [Comprobador de aplicación](/previous-versions/aa480483(v=msdn.10))<br/> [Archivos DLL de AppInit](https://support.microsoft.com/kb/197571)<br/> |
| Cumplimiento de Seguridad de Windows recomendados                                       | El Windows recomendados de seguridad le ayudará a evitar la exposición a Windows superficies expuestas a ataques. Las superficies de ataque son los puntos de entrada que un atacante malintencionado podría usar para aprovechar el sistema operativo aprovechando las vulnerabilidades del software de destino. Una de las peores vulnerabilidades de seguridad es la elevación de privilegios.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Analizador de superficie expuesta a ataques](https://technet.microsoft.com/security/gg749821)<br/> [Access Control listas](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                |
| Compatibilidad con Seguridad de Windows características                                               | El Windows operativo ha implementado muchas medidas para admitir la seguridad y la privacidad del sistema. Las aplicaciones deben admitir estas medidas para mantener la integridad del sistema operativo. Las aplicaciones compiladas incorrectamente podrían provocar saturaciones de búfer que, a su vez, podrían provocar una denegación de servicio o hacer que se ejecutara código malintencionado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Referencia de la herramienta BinScope](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                             |
| Cumplimiento de los mensajes del Administrador de reinicio del sistema                                       | Cuando los usuarios inician el apagado, en la gran mayoría de los casos, tienen un gran deseo de ver que el cierre se realiza correctamente. es posible que se desespejen de la oficina y "simplemente quieran" que sus equipos se apaguen. Las aplicaciones deben respetar este deseo al no bloquear el cierre. Aunque en la mayoría de los casos, un apagado puede no ser crítico, las aplicaciones deben estar preparadas para la posibilidad de un apagado crítico.                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Cambios de apagado de aplicaciones en Windows Vista](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [Reinicio del desarrollo de Manager](/previous-versions/bb756958(v=msdn.10))<br/>                                                                              |
| Limpieza de la instalación reversible                                                   | Una instalación limpia, reversible, permite a los usuarios administrar (implementar y quitar) correctamente aplicaciones en sus sistemas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Cómo: Instalación de requisitos previos con una aplicación ClickOnce](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [Instalación de aplicaciones en sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)<br/>                                                |
| Firma digital de archivos y controladores                                                | Una firma digital Authenticode permite a los usuarios asegurarse de que el software es original. También permite detectar si un archivo se ha alterado, por ejemplo, si se ha infectado por un virus. El cumplimiento de la firma de código en modo kernel es una característica de Windows conocida como integridad de código (CI), que mejora la seguridad del sistema operativo al comprobar la integridad de un archivo cada vez que la imagen del archivo se carga en la memoria. CI detecta si el código malintencionado ha modificado un archivo binario del sistema. También genera un evento de registro de diagnóstico y auditoría del sistema cuando la firma de un módulo de kernel no se puede comprobar correctamente.                                                                                                                                                                            | [Firmas digitales para módulos de kernel en Windows](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                             |
| No bloquee la instalación o el inicio de la aplicación en función de la comprobación de la versión del sistema operativo. | Es importante que los clientes no se bloqueen artificialmente para instalar o ejecutar su aplicación cuando no hay limitaciones técnicas. En general, si las aplicaciones se escribieron para Windows Vista o versiones posteriores, no deben tener ninguna razón para comprobar la versión del sistema operativo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [Control de versiones del sistema operativo](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                           |
| No cargar servicios y controladores en modo Caja fuerte usuario                                   | Caja fuerte modo permite a los usuarios diagnosticar y solucionar problemas Windows. A menos que sea necesario para operaciones básicas del sistema (por ejemplo, controladores de dispositivos de almacenamiento) o para fines de diagnóstico y recuperación (por ejemplo, escáneres antivirus), los controladores y servicios no deben establecerse para cargarse en modo seguro. De forma predeterminada, el modo seguro no inicia la mayoría de los controladores y servicios que no se instalaron previamente con Windows. Deben permanecer deshabilitados a menos que el sistema las requiera para operaciones básicas o con fines de diagnóstico y recuperación.                                                                                                                                                                                                                                                                                         | [Determinar si el sistema operativo se está ejecutando en Caja fuerte operativo](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [Cómo determinar si el sistema se ejecuta en modo Caja fuerte desde un controlador de dispositivo](https://support.microsoft.com/kb/837643)<br/>       |
| Seguir las directrices de control de cuentas de usuario (UAC)                                    | Algunas Windows aplicación se ejecutan en el contexto de seguridad de una cuenta de administrador, y muchas requieren derechos de usuario excesivos y privilegios Windows usuario. El control del acceso a los recursos permite a los usuarios controlar sus sistemas frente a cambios no deseados (un cambio no deseado puede ser malintencionado, como un rootkit que toma el control de forma sigilosa de la máquina o una acción de personas que tienen privilegios limitados, por ejemplo, un empleado que instala software prohibido en un equipo profesional). La regla más importante para controlar el acceso a los recursos es proporcionar la menor cantidad de acceso al contexto de usuario estándar necesario para que un usuario realice las tareas necesarias. Las siguientes directrices de UAC proporcionan a la aplicación los permisos necesarios cuando sea necesario, sin dejar el sistema expuesto constantemente a riesgos de seguridad. | [Control de cuentas de usuario](/windows/desktop/uxguide/winenv-uac)<br/> [UAC: Directrices de actualización de aplicaciones](/previous-versions/aa480152(v=msdn.10))<br/>                                                                       |
| Instalar en las carpetas correctas de forma predeterminada                                       | Los usuarios deben tener una experiencia coherente y segura con la ubicación de instalación predeterminada de los archivos, al tiempo que mantienen la opción de instalar una aplicación en la ubicación que elijan. También es necesario almacenar los datos de la aplicación en la ubicación correcta para permitir que varias personas usen el mismo equipo sin dañar ni sobrescribir los datos y la configuración de los demás.                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [Resumen de los requisitos de instalación o desinstalación](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                    |
| Compatibilidad con sesiones de varios usuarios                                                     | Windows usuarios deben poder ejecutar sesiones simultáneas sin conflictos ni interrupciones.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [Servicios de Escritorio remoto de programación](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                      |
| Compatibilidad con versiones x64 de Windows                                                 | A medida que el hardware de 64 bits es más frecuente, los usuarios esperan que los desarrolladores de aplicaciones aprovechen las ventajas de la arquitectura de 64 bits mediante la migración de sus aplicaciones a 64 bits o que las versiones de 32 bits de la aplicación se ejecuten bien en versiones de 64 bits de Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Compatibilidad de aplicaciones: Windows Vista de 64 bits](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                              |



 

## <a name="see-also"></a>Vea también

-   [Windows Programa de certificación de hardware](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))

 

