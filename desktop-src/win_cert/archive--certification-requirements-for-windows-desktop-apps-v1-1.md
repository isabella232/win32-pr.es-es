---
title: Requisitos de certificación de archivo para aplicaciones de escritorio de Windows v 1.1
description: Documento versión 1.1 documento fecha 26 de enero de 2012This documento contiene los requisitos técnicos y las calificaciones de elegibilidad que una aplicación de escritorio debe cumplir para poder participar en el programa de certificación de aplicaciones de escritorio de Windows 8.
ms.assetid: 48ED216D-90C6-4DB4-AC4E-DF2948285A34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdb7c598a27e4a68e01629bf01b54c534e1bff85
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488126"
---
# <a name="archive-certification-requirements-for-windows-desktop-apps-v11"></a>Archivo: requisitos de certificación para aplicaciones de escritorio de Windows v 1.1

**Versión del documento:** 1,1

**Fecha del documento:** 26 de enero de 2012

Este documento contiene los requisitos técnicos y las calificaciones de elegibilidad que una aplicación de escritorio debe cumplir para poder participar en el programa de certificación de aplicaciones de escritorio de Windows 8. En Windows 7, este programa se conocía como el programa del logotipo de software de Windows.

## <a name="welcome"></a>¡Bienvenido!

La plataforma Windows admite un amplio ecosistema de productos y asociados. Mostrar el logotipo de Windows en el producto representa una relación y un compromiso compartido con la calidad entre Microsoft y su empresa. Los clientes confían en la marca de Windows de su producto, ya que garantiza que cumple los estándares de compatibilidad y funciona correctamente en la plataforma Windows. Pasar correctamente la certificación de aplicaciones de Windows permite mostrar la aplicación en el centro de compatibilidad de Windows y también es un paso necesario para mostrar una referencia de aplicación de escritorio en la tienda Windows.

El programa de certificación de aplicaciones de Windows está formado por requisitos técnicos y de programa para garantizar que las aplicaciones de terceros que llevan la marca de Windows sean fáciles de instalar y confiables en los equipos que ejecutan Windows. Los clientes son la estabilidad, la compatibilidad, la confiabilidad, el rendimiento y la calidad en los sistemas que compran. Microsoft se centra en sus inversiones en cumplir estos requisitos para las aplicaciones de software diseñadas para ejecutarse en la plataforma de Windows para PC. Estos esfuerzos incluyen pruebas de compatibilidad para la coherencia de la experiencia, el rendimiento mejorado y la seguridad mejorada en equipos que ejecutan software de Windows. Las pruebas de compatibilidad de Microsoft se han diseñado en colaboración con asociados del sector y se han mejorado continuamente en respuesta a los progresos del sector y a la demanda del consumidor.

El kit para la certificación de aplicaciones de Windows se usa para validar el cumplimiento de estos requisitos y reemplaza el WSLK que se usa para la validación en el programa del logotipo de software de Windows 7. El kit para la certificación de aplicaciones de Windows es uno de los componentes incluidos en el kit de desarrollo de software (SDK) de Windows.

## <a name="app-eligibility"></a>Idoneidad de la aplicación

Para que una aplicación pueda optar a la certificación de aplicaciones de escritorio de Windows 8, debe cumplir los siguientes criterios y todos los requisitos técnicos que se enumeran en este documento.

-   Debe ser una aplicación independiente
-   Debe ejecutarse en un equipo Windows 8.1 local
-   Puede ser un componente de cliente de una aplicación certificada de Windows Server
-   Debe ser código y características completadas

## <a name="1-apps-are-compatible-and-resilient"></a>1. las aplicaciones son compatibles y resistentes

Los momentos en los que una aplicación se bloquea o deja de responder causan mucha frustración del usuario. Se espera que las aplicaciones sean resistentes y estables y la eliminación de estos errores ayuda a garantizar que el software sea más predecible, mantenible, de rendimiento y de confianza.<dl> 1,1 la aplicación no debe tener una dependencia en los modos de compatibilidad de Windows, el mensaje de AppHelp y otras correcciones de compatibilidad  
1,2 la aplicación no debe tener una dependencia en el tiempo de ejecución de VB6  
1,3 la aplicación no debe cargar archivos dll arbitrarios para interceptar llamadas a la API de Win32 mediante HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows AppInit \_ dll.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. las aplicaciones deben cumplir los procedimientos recomendados de seguridad de Windows

El uso de prácticas recomendadas de seguridad de Windows le ayudará a evitar la creación de exposiciones a las superficies de ataque de Windows. Las superficies de ataque son los puntos de entrada que un atacante malintencionado podría usar para aprovechar el sistema operativo aprovechando las vulnerabilidades del software de destino. Una de las peores vulnerabilidades de seguridad es la elevación de privilegios.

<dl> 2,1 la aplicación debe usar las <a href="/windows/desktop/SecAuthZ/access-control-lists">ACL</a> seguras y adecuadas para proteger los archivos ejecutables  
2,2 la aplicación debe usar las <a href="/windows/desktop/SecAuthZ/access-control-lists">ACL</a> seguras y adecuadas para proteger los directorios.  
2,3 la aplicación debe usar las <a href="/windows/desktop/SecAuthZ/access-control-lists">ACL</a> seguras y adecuadas para proteger las claves del registro  
2,4 la aplicación debe usar las <a href="/windows/desktop/SecAuthZ/access-control-lists">ACL</a> seguras y adecuadas para proteger los directorios que contienen objetos  
2,5 la aplicación debe reducir el acceso de usuarios que no son administradores a los servicios que son vulnerables a alteraciones.  
2,6 la aplicación debe evitar que los servicios con reinicios rápidos se reinicien más de dos veces cada 24 horas.
</dl>**Nota: el acceso solo debe concederse a las entidades que lo requieran.**

El programa de certificación de aplicaciones de Windows comprobará que las superficies de ataque de Windows no se exponen comprobando que las ACL y los servicios se implementan de forma que no ponga en peligro el sistema de Windows.

## <a name="3-apps-support-windows-security-features"></a>3. las aplicaciones admiten las características de seguridad de Windows

El sistema operativo Windows tiene muchas características que admiten la seguridad y privacidad del sistema. Las aplicaciones deben admitir estas características para mantener la integridad del sistema operativo. Las aplicaciones compiladas incorrectamente podrían provocar saturaciones de búfer que pueden, a su vez, provocar la denegación de servicio o permitir la ejecución de código malintencionado. <dl> 3,1 la aplicación no debe usar AllowPartiallyTrustedCallersAttribute (APTCA) para garantizar el acceso seguro a los ensamblados con nombre seguro.  
3,2 la aplicación debe compilarse con la marca/SafeSEH para garantizar el control de excepciones seguras  
3,3 la aplicación debe compilarse con la marca de/NXCOMPAT para evitar la ejecución de datos  
3,4 la aplicación debe compilarse con la marca/DYNAMICBASE para la selección aleatoria del diseño del espacio de direcciones (ASLR)  
3,5 la aplicación no debe leer ni escribir las secciones de PE compartidas  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. las aplicaciones deben adherirse a los mensajes del administrador de reinicio del sistema

Cuando los usuarios inician el cierre, normalmente tienen un fuerte deseo de ver que el apagado se realiza correctamente. pueden darse prisa para salir de la oficina y simplemente desea que sus equipos se desactiven. Las aplicaciones deben respetar este deseo si no bloquean el cierre. Aunque en la mayoría de los casos, es posible que un cierre no sea crítico, las aplicaciones deben estar preparadas para la posibilidad de un apagado crítico.<dl> 4,1 la aplicación debe controlar los cierres críticos correctamente <dl> En un cierre crítico, las aplicaciones que devuelven FALSE a WM \_ QUERYENDSESSION se enviarán a WM \_ ENDSESSION y closed, mientras que los que agotaron el tiempo de respuesta a WM \_ QUERYENDSESSION finalizarán.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ QUERYENDSESSION con lParam = ENDSESSION \_ CLOSEAPP (0x1).  
Las aplicaciones de consola pueden llamar a SetConsoleCtrlHandler para especificar la función que controlará las notificaciones de cierre. Las aplicaciones de servicio pueden llamar a RegisterServiceCtrlHandlerEx para especificar la función que recibirá las notificaciones de cierre.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> WM \_ ENDSESSION con lParam = ENDSESSION \_ CLOSEAPP (0x1).  
Como mínimo, la aplicación se debe preparar guardando los datos de usuario y el estado de la información que se necesita después de un reinicio.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>**Note: Apps that must block shutdown because of an operation that cannot be interrupted should explain the reason to the user.** Use ShutdownBlockReasonCreate to register a string that explains the reason to the user. When the operation has completed, the app should call ShutdownBlockReasonDestroy to indicate that the system can be shut down.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. las aplicaciones deben admitir una instalación limpia y reversible

Una instalación limpia, reversible, permite a los usuarios administrar (implementar y quitar) aplicaciones correctamente en sus sistemas.<dl> 5,1 la aplicación debe implementar correctamente una instalación limpia y reversible <dl> Si se produce un error en la instalación, la aplicación debe ser capaz de revertirla y restaurar el estado anterior de la máquina.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> El reinicio del equipo nunca debe ser la única opción al final de una instalación o actualización. Los usuarios deben tener la oportunidad de reiniciarse más adelante.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Las herramientas de inventario de Windows y las herramientas de telemetría requieren información completa sobre las aplicaciones instaladas. Si usa un instalador basado en MSI, MSI crea automáticamente las entradas del registro siguientes. Si no utiliza un instalador MSI, el módulo de instalación debe crear las siguientes entradas del registro durante la instalación:  
</dl>

-   DisplayName
-   InstallLocation
-   Publicador
-   UninstallString
-   Propiedad versionmajor o MajorVersion
-   VersionMinor o MinorVersion

</dd> </dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. las aplicaciones deben firmar digitalmente los archivos y los controladores

Una firma digital Authenticode permite a los usuarios asegurarse de que el software es auténtico. También permite detectar si se ha alterado un archivo, por ejemplo, si ha sido infectado por un virus. El cumplimiento de la firma de código en modo kernel es una característica de Windows conocida como integridad de código (CI), que mejora la seguridad del sistema operativo mediante la comprobación de la integridad de un archivo cada vez que la imagen del archivo se carga en la memoria. CI detecta si el código malintencionado ha modificado un archivo binario del sistema. También genera un evento de registro de auditoría de sistema y diagnóstico cuando no se puede comprobar correctamente la firma de un módulo del kernel. <dl> 6,1 todos los archivos ejecutables (. exe,. dll,. ocx,. sys,. cpl,. drv,. SCR) deben estar firmados con un certificado Authenticode.  
6,2 todos los controladores de modo kernel instalados por la aplicación deben tener una firma de Microsoft obtenida a través del programa de certificación de hardware de Windows. Todos los controladores del filtro del sistema de archivos deben estar firmados por Microsoft.  
6,3 excepciones y exenciones <dl> Las exenciones se considerarán solo para los redistribuibles de terceros sin signo, excepto los controladores. Se requiere una prueba de comunicación que solicite una versión firmada de los redistribuibles para que se conceda esta renuncia.  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. las aplicaciones no bloquean la instalación o el inicio de la aplicación en función de una comprobación de la versión del sistema operativo

Es importante que los clientes no se bloqueen artificialmente de la instalación o ejecución de su aplicación cuando no hay ninguna limitación técnica. En general, si las aplicaciones se escribieron para Windows Vista o versiones posteriores de Windows, no deben tener que comprobar la versión del sistema operativo.<dl> 7,1 la aplicación no debe realizar comprobaciones de la versión de igualdad <dl> Si necesita una característica específica, compruebe si la propia característica está disponible. Si necesita Windows XP, compruebe Windows XP o posterior (>= 5,1). De esta manera, el código de detección seguirá funcionando en versiones futuras de Windows. Los instaladores de controladores y los módulos de desinstalación nunca deben comprobar la versión del sistema operativo.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   Las aplicaciones que se entregan como un paquete que también se ejecutan en Windows XP, Windows Vista y Windows 7, y deben comprobar la versión del sistema operativo para determinar qué componentes se deben instalar en un sistema operativo determinado.
-   Aplicaciones que solo comprueban la versión mínima del sistema operativo (solo durante la instalación, no en tiempo de ejecución) mediante el uso de las llamadas API aprobadas y que enumeran correctamente el requisito de versión mínima en el manifiesto de la aplicación.
-   Aplicaciones de seguridad (antivirus, firewall, etc.), utilidades del sistema (por ejemplo, desfragmentación, copias de seguridad y herramientas de diagnóstico) que comprueban la versión del sistema operativo usando solo las llamadas API aprobadas.

  
</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. las aplicaciones no cargan servicios o controladores en modo seguro

El modo seguro permite a los usuarios diagnosticar y solucionar problemas de Windows. Los controladores y servicios no deben estar configurados para cargarse en modo seguro, a menos que sean necesarios para las operaciones básicas del sistema de, como los controladores de dispositivo de almacenamiento o para fines de diagnóstico y recuperación, como los detectores de virus,. De forma predeterminada, cuando Windows está en modo seguro, solo inicia los controladores y servicios que venían preinstalados con Windows.

-   8,1 excepciones y exenciones <dl> Los controladores y servicios que se deben iniciar en modo seguro requieren una renuncia. La solicitud de exención debe incluir cada controlador o servicio aplicable que escriba en las claves del registro de SafeBoot y describir los motivos técnicos por los que la aplicación o el servicio deben ejecutarse en modo seguro. El instalador de la aplicación debe registrar todos estos controladores y servicios mediante estas claves del registro:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Nota:** Debe probar estos controladores y servicios para asegurarse de que funcionan en modo seguro sin errores.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. las aplicaciones deben seguir las directrices de control de cuentas de usuario

Algunas aplicaciones de Windows se ejecutan en el contexto de seguridad de una cuenta de administrador y, a menudo, las aplicaciones solicitan permisos de usuario y privilegios de Windows excesivos. Controlar el acceso a los recursos permite a los usuarios controlar sus sistemas y protegerlos frente a cambios no deseados. Un cambio no deseado puede ser malintencionado, como un rootkit que toma el control del equipo o ser el resultado de una acción realizada por personas con privilegios limitados. La regla más importante para controlar el acceso a los recursos es proporcionar la menor cantidad de contexto de usuario estándar de acceso necesario para que un usuario realice sus tareas necesarias. Las siguientes directrices de control de cuentas de usuario (UAC) proporcionan a la aplicación los permisos necesarios cuando son necesarios para la aplicación, sin que el sistema quede expuesto constantemente a riesgos de seguridad. La mayoría de las aplicaciones no requieren privilegios de administrador en tiempo de ejecución y deben ejecutarse correctamente como usuario estándar.<dl> 9,1 la aplicación debe tener un manifiesto que defina los niveles de ejecución e indique al sistema operativo qué privilegios requiere la aplicación para poder ejecutarse <dl> El marcado del manifiesto de la aplicación solo se aplica a los archivos exe, no a las dll. Esto se debe a que UAC no inspecciona los archivos dll durante la creación del proceso. También merece la pena mencionar que las reglas de UAC no se aplican a los servicios de Windows. El manifiesto puede ser incrustado o externo.  
Para crear un manifiesto, cree un archivo con el nombre <APP \_ Name # C1.exe. manifest y almacénelo en el mismo directorio que el archivo exe. Tenga en cuenta que cualquier manifiesto externo se omite si la aplicación tiene un manifiesto interno. Por ejemplo:  
<el nivel de requestedExecutionLevel = "" AsInvoker \| highestAvailable \| requireAdministrator "" UIAccess = "" true \| false ""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Cualquier característica administrativa debe moverse a un proceso independiente que se ejecute con privilegios administrativos. Las aplicaciones orientadas al usuario, como las que tienen acceso a través del grupo de programas en el menú Inicio, y que requieren elevación deben estar firmadas con Authenticode.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> Una renuncia es necesaria para las aplicaciones que ejecutan su proceso principal con privilegios elevados (requireAdministrator o highestAvailable). El proceso principal se identifica como el punto de entrada del usuario en la aplicación. Las exenciones se considerarán para los siguientes escenarios:

-   Herramientas administrativas o del sistema con el nivel de ejecución establecido en highestAvailable y/o requireAdministrator
-   Solo la aplicación del marco de automatización de la interfaz de usuario o de accesibilidad establece la marca uiAccess en true para omitir el aislamiento de privilegios de la interfaz de usuario (UIPI). Para iniciar correctamente el uso de la aplicación, esta marca debe estar firmada con Authenticode y debe residir en una ubicación protegida del sistema de archivos, es decir, archivos de programa.

  
</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. de forma predeterminada, las aplicaciones deben instalarse en las carpetas correctas

Los usuarios deben tener una experiencia coherente y segura con la ubicación de instalación predeterminada de los archivos, a la vez que se mantiene la opción de instalar una aplicación en la ubicación de su elección. También es necesario almacenar los datos de la aplicación en la ubicación correcta para permitir que varias personas usen el mismo equipo sin dañar o sobrescribir la configuración y los datos de los demás. Windows proporciona ubicaciones específicas en el sistema de archivos para almacenar programas y componentes de software, datos de aplicaciones compartidas y datos de aplicaciones específicos de un usuario.<dl> 10,1 la aplicación debe instalarse de forma predeterminada en la carpeta archivos de programa <dl> Para aplicaciones nativas de 32 y 64 bits en% ProgramFiles% y% ProgramFiles (x86)% para aplicaciones de 32 bits que se ejecutan en x64. Los datos de usuario o los datos de la aplicación nunca deben almacenarse en esta ubicación debido a los permisos de seguridad configurados para esta carpeta.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Por ejemplo, la aplicación no debe establecer ninguno de los siguientes elementos:  
</dl>

-   Claves de ejecución del registro HKLM y, o HKCU en software \\ Microsoft \\ Windows \\ CurrentVersion
-   Claves de ejecución del registro HKLM, o HKCU en software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
-   Menú Inicio AllPrograms > Inicio

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\<username>\\AppData  
10,5 la aplicación nunca debe escribir directamente en el directorio "Windows" ni en los subdirectorios. <dl> Use los métodos correctos para instalar archivos, como fuentes o controladores.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Cuando se instala la aplicación, no hay una ubicación de usuario correcta en la que almacenar los datos. Los intentos de una aplicación para modificar los comportamientos de asociación predeterminados en un nivel de equipo después de la instalación no se realizarán correctamente. En su lugar, se deben reclamar los valores predeterminados para cada nivel de usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados de los demás.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> Se requiere una exención para las aplicaciones que escriben en las aplicaciones .NET de la caché de ensamblados global (GAC) deben mantener las dependencias de ensamblado privadas y almacenarlas en el directorio de la aplicación, a menos que se requiera el uso compartido de un ensamblado.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. las aplicaciones deben admitir sesiones de varios usuarios

Los usuarios de Windows deben ser capaces de ejecutar sesiones simultáneas sin conflictos ni interrupciones.<dl> 11,1 la aplicación debe asegurarse de que, cuando se ejecuta en varias sesiones, ya sea de forma local o remota, la funcionalidad normal de la aplicación no se ve afectada negativamente.  
11,2 la configuración y los archivos de datos de la aplicación no deben persistir entre usuarios  
11,3 la privacidad y las preferencias de usuario deben estar aisladas para la sesión de usuario.  
11,4 las instancias de la aplicación deben estar aisladas entre sí. <dl> Esto significa que los datos de usuario de una instancia de no son visibles para otra instancia de la aplicación. El sonido de una sesión de usuario inactiva no debe escucharse en una sesión de usuario activa. En los casos en que varias instancias de la aplicación usan recursos compartidos, la aplicación debe asegurarse de que no haya ningún conflicto.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Consulte los requisitos de UAC.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>**Note:** If an app does not support multiple user sessions or remote access, it must clearly state this when launched from this kind of session.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. las aplicaciones deben admitir versiones x64 de Windows

Dado que el hardware de 64 bits es más común, los usuarios esperan que los desarrolladores de aplicaciones aprovechen las ventajas de la arquitectura de 64 bits mediante la migración de sus aplicaciones a 64 bits o que las versiones de 32 bits de la aplicación se ejecuten correctamente en versiones de Windows de 64 bits.<dl> 12,1 la aplicación debe admitir de forma nativa 64 bits o, como mínimo, las aplicaciones basadas en Windows de 32 bits deben ejecutarse sin problemas en sistemas de 64 bits para mantener la compatibilidad con versiones de Windows de 64 bits  
12,2 la aplicación y sus instaladores no deben contener ningún código de 16 bits ni confiar en ningún componente de 16 bits  
12,3 el programa de instalación de la aplicación debe detectar e instalar los controladores y componentes adecuados para la arquitectura de 64 bits  
12,4 los complementos de Shell deben ejecutarse en versiones de Windows de 64 bits  
12,5 la aplicación que se ejecuta en el emulador WoW64 no debe intentar sobretocar u omitir los mecanismos de virtualización de WOW64 <dl> Si hay escenarios específicos en los que las aplicaciones deben detectar si se ejecutan en el emulador WoW64, deben hacerlo llamando a IsWow64Process.  
</dl> </dd> </dl>

## <a name="conclusion"></a>Conclusión

A medida que se desarrollen estos requisitos, anotaremos los cambios en el historial de revisiones. Los requisitos estables son fundamentales para realizar el mejor trabajo, por lo que nos esforzaremos para asegurarse de que los cambios que hacemos son sostenibles y continúan protegiendo y mejorando las aplicaciones.

Gracias de nuevo por unirse a nuestro compromiso de ofrecer fantásticas experiencias de los clientes.

## <a name="revision-history"></a>Historial de revisiones



|              |         |                                        |                  |
|--------------|---------|----------------------------------------|------------------|
| Fecha         | Versión | Descripción de la revisión                   | Vínculo a documento |
| 20 de diciembre de 2011 | 1,0     | Borrador inicial del documento para la vista previa. |                  |
| 26 de enero de 2012 | 1,1     | Actualice a la sección \# 2.                 | 1,1              |



 

## <a name="learn-more-about-desktop-app-certification"></a>Más información sobre la certificación de aplicaciones de escritorio



|                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Requisito                                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Más detalles                                                                                                                                                                                                                                                                                |
| Compatibilidad y resistencia                                                    | Los bloqueos & bloqueos son una interrupción importante para los usuarios y causan frustración. Se espera que las aplicaciones sean resistentes y estables, lo que elimina este tipo de errores ayuda a garantizar que el software sea más predecible, mantenible, de rendimiento y de confianza.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Sistemas operativos Windows Vista, Windows 7 y Windows 8](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [Comprobador de aplicación](/previous-versions/aa480483(v=msdn.10))<br/> [Archivos dll de AppInit](https://support.microsoft.com/kb/197571)<br/> |
| Cumplir los procedimientos recomendados de seguridad de Windows                                       | El uso de prácticas recomendadas de seguridad de Windows le ayudará a evitar la creación de exposiciones a las superficies de ataque de Windows. Las superficies de ataque son los puntos de entrada que un atacante malintencionado podría usar para aprovechar el sistema operativo aprovechando las vulnerabilidades del software de destino. Una de las peores vulnerabilidades de seguridad es la elevación de privilegios.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Analizador de superficie expuesta a ataques](https://technet.microsoft.com/security/gg749821)<br/> [Access Control listas](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                |
| Compatibilidad con características de seguridad de Windows                                               | El sistema operativo Windows ha implementado muchas medidas para admitir la seguridad y la privacidad del sistema. Las aplicaciones deben admitir estas medidas para mantener la integridad del sistema operativo. Las aplicaciones compiladas incorrectamente podrían provocar saturaciones de búfer que, a su vez, podrían provocar la denegación de servicio o la ejecución de código malintencionado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Referencia de la herramienta BinScope](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                             |
| Adhiere a los mensajes del administrador de reinicio del sistema                                       | Cuando los usuarios inician el cierre, en la mayoría de los casos, tienen un fuerte deseo de ver que el apagado se realiza correctamente. puede que se detengan prisas para salir de la oficina y "desea" que los equipos se desactiven. Las aplicaciones deben respetar este deseo si no bloquean el cierre. Aunque en la mayoría de los casos, es posible que un cierre no sea crítico, las aplicaciones deben estar preparadas para la posibilidad de un apagado crítico.                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Cambios de cierre de la aplicación en Windows Vista](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [Desarrollo del administrador de reinicio](/previous-versions/bb756958(v=msdn.10))<br/>                                                                              |
| Limpieza de la instalación reversible                                                   | Una instalación limpia, reversible, permite a los usuarios administrar (implementar y quitar) aplicaciones correctamente en sus sistemas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Cómo: Instalación de requisitos previos con una aplicación ClickOnce](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [Instalación de aplicaciones en sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)<br/>                                                |
| Firmar archivos y controladores digitalmente                                                | Una firma digital Authenticode permite a los usuarios asegurarse de que el software es auténtico. También permite detectar si un archivo se ha alterado, por ejemplo, si ha sido infectado por un virus. El cumplimiento de la firma de código en modo kernel es una característica de Windows conocida como integridad de código (CI), que mejora la seguridad del sistema operativo mediante la comprobación de la integridad de un archivo cada vez que la imagen del archivo se carga en la memoria. CI detecta si el código malintencionado ha modificado un archivo binario del sistema. También genera un evento de registro de auditoría de sistema y diagnóstico cuando no se puede comprobar correctamente la firma de un módulo del kernel.                                                                                                                                                                            | [Firmas digitales para módulos de kernel en Windows](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                             |
| No bloquear la instalación o el inicio de la aplicación en función de la comprobación de la versión del sistema operativo | Es importante que los clientes no se bloqueen artificialmente de la instalación o ejecución de su aplicación cuando no hay ninguna limitación técnica. En general, si las aplicaciones se escribieron para Windows Vista o versiones posteriores, no deben tener ninguna razón para comprobar la versión del sistema operativo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [Control de versiones del sistema operativo](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                           |
| No cargar servicios y controladores en modo seguro                                   | El modo seguro permite a los usuarios diagnosticar y solucionar problemas de Windows. A menos que sea necesario para las operaciones básicas del sistema (por ejemplo, los controladores de dispositivos de almacenamiento) o para fines de diagnóstico y recuperación (por ejemplo, escáneres antivirus), los controladores y servicios no deben estar configurados para cargarse en modo seguro. De forma predeterminada, el modo seguro no inicia la mayoría de los controladores y servicios que no estaban preinstalados con Windows. Deben permanecer deshabilitadas a menos que el sistema las necesite para operaciones básicas o para fines de diagnóstico y recuperación.                                                                                                                                                                                                                                                                                         | [Determinar si el sistema operativo se ejecuta en modo seguro](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [Cómo determinar si el sistema se ejecuta en modo seguro desde un controlador de dispositivo](https://support.microsoft.com/kb/837643)<br/>       |
| Siga las directrices de control de cuentas de usuario (UAC)                                    | Algunas aplicaciones de Windows se ejecutan en el contexto de seguridad de una cuenta de administrador y muchas requieren derechos de usuario excesivos y privilegios de Windows. Controlar el acceso a los recursos permite que los usuarios tengan el control de sus sistemas frente a los cambios no deseados (un cambio no deseado puede ser malintencionado, por ejemplo, un rootkit que toma el equipo, o una acción de personas con privilegios limitados, por ejemplo, un empleado que instala software prohibido en un equipo de trabajo). La regla más importante para controlar el acceso a los recursos es proporcionar la menor cantidad de contexto de usuario estándar de acceso necesario para que un usuario realice sus tareas necesarias. Las siguientes directrices de UAC proporcionan a la aplicación los permisos necesarios cuando sea necesario, sin que el sistema quede expuesto constantemente a riesgos de seguridad. | [Control de cuentas de usuario](/windows/desktop/uxguide/winenv-uac)<br/> [UAC: instrucciones de actualización de la aplicación](/previous-versions/aa480152(v=msdn.10))<br/>                                                                       |
| Instalar en las carpetas correctas de forma predeterminada                                       | Los usuarios deben tener una experiencia coherente y segura con la ubicación de instalación predeterminada de los archivos, a la vez que se mantiene la opción de instalar una aplicación en la ubicación que elijan. También es necesario almacenar los datos de la aplicación en la ubicación correcta para permitir que varias personas usen el mismo equipo sin dañar o sobrescribir la configuración y los datos de los demás.                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [Resumen de los requisitos de instalación y desinstalación](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                    |
| Compatibilidad con sesiones de varios usuarios                                                     | Los usuarios de Windows deben ser capaces de ejecutar sesiones simultáneas sin conflictos ni interrupciones.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [Instrucciones de programación de Servicios de Escritorio remoto](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                      |
| Compatibilidad con versiones x64 de Windows                                                 | A medida que el hardware de 64 bits se vuelve más frecuente, los usuarios esperan que los desarrolladores de aplicaciones aprovechen las ventajas de la arquitectura de 64 bits mediante la migración de sus aplicaciones a 64 bits o que las versiones de 32 bits de la aplicación se ejecuten correctamente en versiones de Windows de 64 bits.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Compatibilidad de aplicaciones: Windows Vista 64 bits](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                              |



 

## <a name="see-also"></a>Vea también

-   [Programa de certificación de hardware de Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))

 

