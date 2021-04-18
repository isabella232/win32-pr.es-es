---
title: Pruebas del Kit para la certificación de aplicaciones en Windows
description: A continuación se muestran los detalles de las pruebas para la certificación de aplicaciones de Dekstop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a353eef0cd73fecac275b750345b3dd97d05dc87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720166"
---
# <a name="windows-app-certification-kit-tests"></a>Pruebas del Kit para la certificación de aplicaciones en Windows

A continuación se muestran los detalles de las pruebas para la certificación de aplicaciones de Dekstop. Para obtener más información, consulte [uso del kit para la certificación de aplicaciones de Windows](using-the-windows-app-certification-kit.md).

-   [Instalación reversible limpia](#clean-reversible-install)
-   [Instalar en la prueba de carpetas correcta](#install-to-the-correct-folders-test)
-   [Prueba de archivos firmados digitalmente](#digitally-signed-file-test)
-   [Compatibilidad con la prueba de Windows x64](#support-x64-windows-test)
-   [Prueba de comprobación de la versión del SO](#os-version-checking-test)
-   [Prueba de control de cuentas de usuario (UAC)](#user-account-control-uac-test)
-   [Adhiere a los mensajes del administrador de reinicio del sistema](#adhere-to-system-restart-manager-messages)
-   [Prueba de modo seguro](#safe-mode-test)
-   [Prueba de sesión multiusuario](#multiuser-session-test)
-   [Prueba de bloqueos y bloqueos](#crashes-and-hangs-test)
-   [Prueba de compatibilidad y resistencia](#compatibility-and-resiliency-test)
-   [Prueba de prácticas recomendadas de seguridad de Windows](#windows-security-best-practices-test)
-   [Prueba de características de seguridad de Windows](#windows-security-features-test)
-   [Prueba de PPP alta](#high-dpi-test)

## <a name="clean-reversible-install"></a>Instalación reversible limpia

Instala y desinstala la aplicación y comprueba si hay archivos residuales y entradas del registro.

-   Información previa
    -   Una instalación limpia y reversible permite a los usuarios implementar y quitar aplicaciones. Para pasar esta prueba, la aplicación debe hacer lo siguiente:
        -   La aplicación no obliga al sistema a reiniciarse inmediatamente después de instalar o desinstalar la aplicación. *El proceso de instalación o desinstalación de una aplicación nunca debe requerir un reinicio del sistema después de que se complete. Si esto requiere que el sistema se reinicie, los usuarios deben poder reiniciar el sistema a su comodidad.*
        -   La aplicación no depende de los nombres de archivo cortos de 8,3 (SFN). *Los procesos de instalación y desinstalación de la aplicación deben poder usar nombres de archivo largos y rutas de acceso a carpetas.*
        -   La aplicación no bloquea la instalación/desinstalación silenciosa
        -   La aplicación realiza las entradas necesarias en el registro del sistema. *Las herramientas de inventario de Windows y de telemetría requieren información completa sobre las aplicaciones instaladas. Los instaladores de aplicaciones deben crear las entradas del registro correctas para permitir la detección y desinstalaciones correctas.*
    -   Si usa un instalador basado en MSI, MSI crea automáticamente las entradas del registro siguientes. Si no utiliza un instalador MSI, el módulo de instalación debe crear las siguientes entradas del registro durante la instalación:
        -   DisplayName
        -   InstallLocation
        -   Publicador
        -   UninstallString
        -   Propiedad versionmajor o MajorVersion
        -   VersionMinor o MinorVersion
    -   La aplicación debe quitar todas sus entradas en Agregar o quitar programas.
-   Detalles de las pruebas
    -   Esta prueba comprueba los procesos de instalación y desinstalación de la aplicación para el comportamiento requerido.
-   Acción correctora
    -   Revise el diseño y el comportamiento de la aplicación con los requisitos descritos anteriormente.

## <a name="install-to-the-correct-folders-test"></a>Instalar en la prueba de carpetas correcta

Comprueba que la aplicación escribe sus archivos de programa y de datos en las carpetas correctas.

-   Información previa
    -   Las aplicaciones deben tener el sistema de usuario y las carpetas por usuario correctamente para poder tener acceso a los datos y la configuración que necesita, al mismo tiempo que protege los datos y la configuración del usuario del acceso no autorizado.
-   Carpetas de archivos de programa
    -   La aplicación debe instalarse de forma predeterminada en la carpeta archivos de programa (% ProgramFiles% para las aplicaciones nativas de 32 y 64 bits y% ProgramFiles (x86)% para las aplicaciones de 32 bits que se ejecutan en x64).
    -   **Nota:** La aplicación no debe almacenar los datos de usuario o los datos de la aplicación en una carpeta de archivos de programa debido a los permisos de seguridad configurados para esta carpeta.
    -   Las ACL de las carpetas del sistema de Windows permiten que solo las cuentas de administrador puedan leer y escribir en ellas. Como resultado, las cuentas de usuario estándar no tendrán acceso a estas carpetas. Sin embargo, la virtualización de archivos permite que las aplicaciones almacenen un archivo, como un archivo de configuración, en una ubicación del sistema que normalmente solo pueden escribir los administradores. La ejecución de programas como usuario estándar en esta situación podría producir un error si no puede tener acceso a un archivo necesario.
    -   Las aplicaciones deben usar [carpetas conocidas](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) para asegurarse de que podrán acceder a sus datos.
    -   **Nota:** Windows proporciona virtualización de archivos para mejorar la compatibilidad de aplicaciones y eliminar problemas cuando las aplicaciones se ejecutan como un usuario estándar en Windows. La aplicación no debe basarse en la virtualización presente en versiones futuras de Windows.
-   Carpetas de datos de aplicaciones específicas del usuario
    -   En las instalaciones "por máquina", la aplicación no debe escribir datos específicos del usuario durante la instalación. Los datos de instalación específicos del usuario solo se deben escribir cuando un usuario inicia la aplicación por primera vez. Esto se debe a que no hay una ubicación de usuario correcta en la que almacenar los datos en el momento de la instalación. Los intentos de una aplicación para modificar los comportamientos de asociación predeterminados en un nivel de equipo después de la instalación no se realizarán correctamente. En su lugar, se deben reclamar los valores predeterminados para cada nivel de usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados de los demás.
    -   Todos los datos de aplicación exclusivos para un usuario específico y que no se comparten con otros usuarios del equipo deben almacenarse en los usuarios \\ <username> \\ appdata.
    -   Todos los datos de la aplicación que se deben compartir entre los usuarios del equipo deben almacenarse en ProgramData.
-   Otras carpetas del sistema y claves del registro
    -   La aplicación nunca debe escribir directamente en el directorio y los subdirectorios de Windows. Use los métodos correctos para instalar archivos, como fuentes o controladores, en estos directorios.
    -   Las aplicaciones no deben iniciarse automáticamente al iniciarse, como agregar una entrada a una o más de estas ubicaciones:
        -   Claves de ejecución del registro HKLM y, o HKCU en software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Claves de ejecución del registro HKLM, o HKCU en software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
        -   Menú Inicio AllPrograms > Inicio
-   Detalles de las pruebas
    -   Esta prueba comprueba que la aplicación usa las ubicaciones específicas del sistema de archivos que Windows proporciona para almacenar programas y componentes de software, datos de aplicaciones compartidas y datos de aplicación específicos de un usuario.
-   Acciones correctivas
    -   Revise el modo en que la aplicación usa las carpetas del sistema y asegúrese de que las usa correctamente.
-   Excepciones y exenciones
    -   Una renuncia es necesaria para que las aplicaciones de escritorio escriban en la caché de ensamblados global (GAC) (las aplicaciones .NET deben mantener las dependencias de ensamblado privadas y almacenarlas en el directorio de la aplicación, a menos que se requiera el uso compartido de un ensamblado).
    -   La instalación en la carpeta programas archivos no es un requisito para que los paquetes de SW Desktop consigan el logotipo de SW, solo en la categoría fundamentos de SW.

## <a name="digitally-signed-file-test"></a>Prueba de archivos firmados digitalmente

Prueba los archivos ejecutables y los controladores de dispositivos para comprobar que tienen una firma digital válida.

-   Información previa
    -   Los archivos firmados digitalmente permiten comprobar que el archivo es auténtico y detectar si se ha alterado el archivo.
    -   El cumplimiento de la firma de código en modo kernel es una característica de Windows que también se conoce como integridad de código (CI). CI mejora la seguridad de Windows mediante la comprobación de la integridad de un archivo cada vez que se carga en la memoria. CI detecta si el código malintencionado ha modificado un archivo binario del sistema y genera un evento de registro de auditoría de sistema y diagnóstico cuando la firma de un módulo de kernel no se comprueba correctamente.
    -   Si la aplicación requiere permisos elevados, la petición de elevación muestra información contextual sobre el archivo ejecutable que solicita acceso con privilegios elevados. En función de si la aplicación está firmada con Authenticode, el usuario puede ver la solicitud de consentimiento o la solicitud de credenciales.
    -   Los nombres seguros evitan que terceras empresas suplanten el código, siempre y cuando mantenga la clave privada segura. En el .NET Framework se comprueba la firma digital cuando se carga el ensamblado o se instala en la GAC. Sin acceso a la clave privada, un usuario malintencionado no puede modificar el código y volver a iniciar sesión.
-   Detalles de las pruebas
    -   Todos los archivos ejecutables, como los que tienen las extensiones de archivo. exe,. dll,. ocx,. sys,. cpl,. drv y. SCR, deben estar firmados con un certificado Authenticode.
    -   Todos los controladores de modo kernel instalados por la aplicación deben tener una firma de Microsoft obtenida a través del programa WHQL o DRS. Todos los controladores del filtro del sistema de archivos deben estar firmados por WHQL.
-   Acción correctora
    -   Firmar los archivos ejecutables de la aplicación.
    -   Use makecert.exe para generar un certificado u obtener una clave de firma de código de una de las entidades de certificación (CA) comerciales, como VeriSign, Thawte o una CA de Microsoft.
-   Excepciones y exenciones
    -   Las exenciones se considerarán solo para redistribuibles de terceros sin signo. Se requiere una prueba de comunicación que solicite una versión firmada de los redistribuibles para que se conceda esta renuncia.
    -   Los paquetes de software agregados por valor de dispositivo están exentos de la certificación del controlador en modo kernel, ya que los controladores deben estar certificados en la certificación de hardware de Windows.

## <a name="support-x64-windows-test"></a>Compatibilidad con la prueba de Windows x64

Pruebe la aplicación para asegurarse de que el archivo. exe se crea para la arquitectura de la plataforma en la que se instalará.

-   Información previa
    -   El archivo ejecutable se debe compilar para la arquitectura de procesador en la que está instalado. Algunos archivos ejecutables podrían ejecutarse en una arquitectura de procesador diferente, pero esto no es confiable.
    -   La compatibilidad con la arquitectura es importante porque los procesos de 32 bits no pueden cargar archivos dll de 64 bits y los procesos de 64 bits no pueden cargar archivos dll de 32 bits. Del mismo modo, las versiones de 64 bits de Windows no admiten la ejecución de aplicaciones basadas en Windows de 16 bits, ya que los identificadores tienen 32 bits significativos en Windows de 64 bits, por lo que no se pueden pasar a aplicaciones de 16 bits. Por lo tanto, si se intenta iniciar una aplicación de 16 bits, se producirá un error en las versiones de 64 bits de Windows.
    -   los controladores de dispositivos de 32 bits no se pueden ejecutar en versiones de Windows de 64 bits y, por lo tanto, se deben trasladar a la arquitectura de 64 bits.
    -   En el caso de las aplicaciones de modo de usuario, las ventanas de 64 bits incluyen WOW64, que permite que las aplicaciones Windows de 32 bits se ejecuten en sistemas que ejecutan Windows de 64 bits, aunque con cierta pérdida de rendimiento. No existe ninguna capa de traducción equivalente para los controladores de dispositivo.
    -   Para mantener la compatibilidad con las versiones de 64 bits de Windows, las aplicaciones deben admitir de forma nativa 64 bits o, como mínimo, las aplicaciones basadas en Windows de 32 bits deben ejecutarse sin problemas en los sistemas de 64 bits:
        -   Las aplicaciones y sus instaladores no debe contienen código de 16 bits o dependen de cualquier componente de 16 bits.
        -   La instalación de la aplicación debe detectar e instalar los controladores y componentes adecuados en las versiones de 64 bits de Windows.
        -   Los complementos de Shell deben ejecutarse en las versiones de 64 bits de Windows.
        -   Las aplicaciones que se ejecutan en el emulador WoW64 no deben intentar omitir los mecanismos de virtualización de WOW64. Si hay escenarios específicos en los que las aplicaciones deben detectar si se ejecutan en un emulador WoW64, deben hacerlo llamando a [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Detalles de las pruebas
    -   La aplicación no debe instalar ningún binario de 16 bits. La aplicación no debe instalar un controlador de modo kernel de 32 bits si se supone que se ejecuta en un equipo de 64 bits.
-   Acciones correctivas
    -   Compile los archivos ejecutables y los controladores para la arquitectura de procesador para la que desea instalarlos.

## <a name="os-version-checking-test"></a>Prueba de comprobación de la versión del SO

Comprueba cómo la aplicación comprueba la versión de Windows en la que se ejecuta.

-   Información previa
    -   Las aplicaciones comprueban la versión del sistema operativo probando una versión mayor o igual que la versión necesaria para garantizar la compatibilidad con versiones futuras de Windows.
-   Detalles de las pruebas
    -   Simula la ejecución de la aplicación en diferentes versiones de Windows para ver cómo reacciona.
-   Acciones correctivas
    -   Pruebe la versión correcta de Windows comprobando si la versión actual es mayor o igual que la versión que necesita su aplicación, servicio o controlador.
    -   Los instaladores de controladores y los módulos de desinstalación nunca deben comprobar la versión del sistema operativo.
-   Excepciones y exenciones
    -   Las exenciones se considerarán para las aplicaciones que cumplan los siguientes criterios: *(se aplica solo a la certificación de aplicaciones de escritorio)*
        -   Las aplicaciones que se entregan como un paquete que se ejecuta en Windows XP, Windows Vista y Windows 7 y tienen que comprobar la versión del sistema operativo para determinar qué componentes se deben instalar en un sistema operativo determinado.
        -   Aplicaciones que solo comprueban la versión mínima del sistema operativo (solo durante la instalación, no en tiempo de ejecución) usando solo las llamadas API aprobadas y enumeran el requisito de versión mínima en el manifiesto de la aplicación, según sea necesario.
        -   Aplicaciones de seguridad como aplicaciones antivirus y de firewall, utilidades del sistema como utilidades de desfragmentación y aplicaciones de copia de seguridad, y herramientas de diagnóstico que comprueban la versión del sistema operativo usando solo las llamadas API aprobadas.

## <a name="user-account-control-uac-test"></a>Prueba de control de cuentas de usuario (UAC)

Prueba la aplicación para comprobar que no necesita permisos elevados innecesariamente elevados para ejecutarse.

-   Información previa
    -   Una aplicación que solo funciona o se instala cuando el usuario es un administrador obliga a los usuarios a ejecutar la aplicación con permisos elevados innecesariamente, lo que puede permitir que el malware escriba el equipo del usuario.
    -   Cuando los usuarios siempre están obligados a ejecutar aplicaciones con tokens de acceso elevados, la aplicación puede ser servidor como punto de entrada para el código malintencionado o engañoso. Este malware puede modificar fácilmente el sistema operativo o, lo que es peor, afectar a otros usuarios. Es casi imposible controlar un usuario que tiene acceso de administrador completo, ya que los administradores pueden instalar aplicaciones y ejecutar cualquier aplicación o script en el equipo. Los administradores de ti siempre buscan maneras de crear "escritorios estándar" en los que los usuarios inician sesión como usuarios estándar. Los escritorios estándar reducen considerablemente los costos del Departamento de soporte técnico y reducen la sobrecarga de ti.
    -   La mayoría de las aplicaciones no requieren privilegios de administrador en tiempo de ejecución. Una cuenta de usuario estándar debe ser capaz de ejecutarlas. Las aplicaciones de Windows deben tener un manifiesto (incrustado o externo) para definir el nivel de ejecución que indica al sistema operativo los privilegios necesarios para ejecutar la aplicación. El manifiesto de aplicación solo se aplica a los archivos. exe, no a los archivos. dll. Control de cuentas de usuario (UAC) no inspecciona archivos dll durante la creación del proceso. Las reglas de UAC no se aplican a los servicios de Microsoft. El manifiesto de la aplicación puede estar incrustado o ser externo.
    -   Para crear un manifiesto, cree un archivo con el nombre <APP \_ Name # C1.exe. manifest y almacénelo en el mismo directorio que el archivo exe. Tenga en cuenta que cualquier manifiesto externo se omite si la aplicación tiene un manifiesto interno.
        -   Por ejemplo, <el nivel de requestedExecutionLevel = "" AsInvoker \| highestAvailable \| requireAdministrator "" UIAccess = "" true \| false ""/>
        -   El proceso principal de la aplicación debe ejecutarse como un usuario estándar (**asInvoker**). Cualquier característica administrativa debe moverse a un proceso independiente que se ejecute con privilegios administrativos.
        -   Las aplicaciones orientadas al usuario que requieren privilegios elevados deben estar firmadas con Authenticode.
-   Detalles de las pruebas
    -   Todos los archivos exe orientados al usuario deben marcarse con el atributo AsInvoker. Si están marcados como highestAvailable o requireAdministrator, deben firmarse correctamente con Authenticode. Cualquier archivo exe de la aplicación no debe tener el atributo uiAccess establecido en true. Cualquier archivo exe que se ejecute como un servicio se excluye de esta comprobación en particular.
-   Acciones correctivas
    -   Revise el archivo de manifiesto de la aplicación para ver las entradas y los niveles de permiso correctos.
-   Excepciones y exenciones
    -   Una renuncia es necesaria para las aplicaciones que ejecutan su proceso principal con privilegios elevados (**requireAdministrator** o **highestAvailable**). El proceso principal es el proceso que proporciona el punto de entrada del usuario a la aplicación.
    -   Las exenciones se considerarán para los siguientes escenarios:
        -   Herramientas administrativas o del sistema con el nivel de ejecución establecido en **highestAvailable**, **requireAdministrator** o ambos.
        -   Solo la aplicación del marco de automatización de la interfaz de usuario o de accesibilidad establece la marca uiAccess en TRUE para omitir el aislamiento de privilegios de la interfaz de usuario (UIPI). Para iniciar correctamente el uso de la aplicación, esta marca debe estar firmada con Authenticode y debe residir en una ubicación protegida del sistema de archivos, como archivos de programa.

## <a name="adhere-to-system-restart-manager-messages"></a>Adhiere a los mensajes del administrador de reinicio del sistema

Comprueba el modo en que la aplicación responde a los mensajes de cierre del sistema y de reinicio.

-   Información previa
    -   Las aplicaciones deben salir lo más rápido posible cuando se les notifica que el sistema se está cerrando para proporcionar una experiencia de apagado o apagado para el usuario.
    -   En un cierre crítico, las aplicaciones que devuelven FALSE a [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) se enviarán a **WM \_ ENDSESSION** y closed, mientras que el tiempo de espera en respuesta a WM \_ QUERYENDSESSION se terminará forzosamente.
-   Detalles de las pruebas
    -   Examina el modo en que la aplicación responde para cerrar y salir de los mensajes.
-   Acciones correctivas
    -   Si se produce un error en la aplicación en esta prueba, revise cómo trata estos mensajes de Windows:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *lParam*  =  **ENDSESSION \_ CLOSEAPP**(0x1): las aplicaciones de escritorio deben responder (true) inmediatamente como preparación para un reinicio. Las aplicaciones de consola pueden llamar a [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para recibir la notificación de cierre. Los servicios pueden llamar a [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para recibir notificaciones de cierre en una rutina de controlador.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *lParam*  =  **ENDSESSION \_ CLOSEAPP**(0x1): las aplicaciones deben devolver un valor 0 en 30 segundos y cerrarse. Como mínimo, las aplicaciones se deben preparar guardando los datos de usuario y el estado de la información que se necesita después de un reinicio.
    -   Las aplicaciones de consola que reciben la notificación de **\_ \_ eventos Ctrl C** deben cerrarse inmediatamente. Los controladores no deben vetar un evento de cierre del sistema.
    -   **Nota:** Las aplicaciones que deben bloquear el cierre debido a una operación que no se puede interrumpir deben usar [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) para registrar una cadena que explica el motivo para el usuario. Una vez completada la operación, la aplicación debe llamar a [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) para indicar que se puede apagar el sistema.

## <a name="safe-mode-test"></a>Prueba de modo seguro

Comprueba si el controlador o el servicio están configurados para iniciarse en modo seguro.

-   Información previa
    -   El modo seguro permite a los usuarios diagnosticar y solucionar problemas con Windows. Solo los controladores y servicios que son necesarios para el funcionamiento básico del sistema operativo o proporcionan servicios de diagnóstico y recuperación deben cargarse en modo seguro. Cargar otros archivos en modo seguro dificulta la solución de problemas con el sistema operativo.
    -   De forma predeterminada, solo los controladores y servicios que se instalan previamente con Windows se inician en modo seguro. Todos los demás controladores y servicios deben estar deshabilitados a menos que el sistema los requiera para operaciones básicas o para fines de diagnóstico y recuperación.
-   Detalles de las pruebas
    -   Los controladores instalados por la aplicación no deben marcarse para cargarse en modo seguro.
-   Acciones correctivas
    -   Si el controlador o el servicio no deben iniciarse en modo seguro, quite las entradas de la aplicación de las claves del registro.
-   Excepciones y exenciones
    -   Los controladores y servicios que deben iniciarse en modo seguro requieren la certificación de una renuncia. La solicitud de exención debe incluir todos los controladores y servicios que se van a agregar a las claves del registro de SafeBoot y describir los motivos técnicos por los que el controlador o el servicio deben ejecutarse en modo seguro. El instalador de la aplicación debe registrar todos estos controladores y servicios en estas claves del registro:
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Nota:** Debe probar los controladores y servicios que desea iniciar en modo seguro para asegurarse de que funcionan en modo seguro sin errores.

## <a name="multiuser-session-test"></a>Prueba de sesión multiusuario

Probar cómo se comporta la aplicación cuando se ejecuta en varias sesiones al mismo tiempo.

-   Información previa
    -   Los usuarios de Windows deben ser capaces de ejecutar sesiones simultáneas. Las aplicaciones deben asegurarse de que, cuando se ejecutan en varias sesiones, ya sea de forma local o remota, la funcionalidad normal de la aplicación no se ve afectada negativamente. La configuración de la aplicación y los archivos de datos deben ser específicos del usuario y la privacidad y las preferencias del usuario deben estar restringidas a la sesión del usuario.
-   Detalles de las pruebas
    -   Ejecuta varias instancias simultáneas de la aplicación para probar lo siguiente:
        -   Varias instancias de una aplicación que se ejecutan al mismo tiempo están aisladas entre sí.
    -   Esto significa que los datos de usuario de una instancia de no son visibles para otra instancia de. El sonido de una sesión de usuario inactiva no debe escucharse en una sesión de usuario activa. En los casos en que varias instancias de la aplicación usan recursos compartidos, la aplicación debe asegurarse de que no haya ningún conflicto.
        -   Si la aplicación se instaló para varios usuarios, almacena los datos en las carpetas correctas y en las ubicaciones del registro.
        -   La aplicación se puede ejecutar en varias sesiones de usuario (cambio rápido de usuario) para el acceso local y remoto.
    -   Para asegurarse de ello, la aplicación debe comprobar otras sesiones de Terminal Services (TS) para las instancias existentes de la aplicación. Si la aplicación no admite varias sesiones de usuario o acceso remoto, debe indicarlo claramente al usuario cuando se inicia desde dicha sesión.
-   Acción correctiva
    -   Asegúrese de que la aplicación no almacena los archivos de datos de todo el sistema o la configuración en almacenes de datos específicos del usuario, como el perfil de usuario o HKCU. Si es así, esa información no estará disponible para otros usuarios.
    -   La aplicación debe instalar los archivos de datos y de configuración de todo el sistema durante la instalación y crear los archivos específicos del usuario y la configuración después de la instalación cuando un usuario lo ejecute.
    -   Asegúrese de que la aplicación no bloquea varias sesiones simultáneas, ya sea de forma local o remota. La aplicación no debe depender de las exclusiones mutuas globales u otros objetos con nombre para comprobar o bloquear varias sesiones simultáneas.
    -   Si la aplicación no puede permitir varias sesiones simultáneas por usuario, use espacios de nombres por usuario o por sesión para las exclusiones mutuas y otros objetos con nombre.

## <a name="crashes-and-hangs-test"></a>Prueba de bloqueos y bloqueos

Supervisa la aplicación durante la prueba de certificación para registrar cuándo se bloquea o se cuelga.

-   Información previa
    -   Los errores de aplicación, como bloqueos y bloqueos, son una interrupción importante para los usuarios y causan frustración. La eliminación de estos errores mejora la estabilidad y la confiabilidad de la aplicación y, en general, proporciona a los usuarios una mejor experiencia de la aplicación. Las aplicaciones que dejan de responder o se bloquean pueden originar pérdidas de datos al usuario y que su experiencia no sea buena.
-   Detalles de las pruebas
    -   Probamos la estabilidad y resistencia de la aplicación durante las pruebas de certificación.
    -   El kit para la certificación de aplicaciones de Windows llama a [**IApplicationActivationManager:: ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) para iniciar aplicaciones de la tienda Windows. Para que **ActivateApplication** inicie una aplicación, el Control de cuentas de usuario (UAC) debe estar habilitado y la pantalla debe tener una resolución de al menos 1024 x 768 o 768 x 1024. Si alguna de estas condiciones no se cumple, tu aplicación no pasará esta prueba.
-   Acciones correctivas
    -   Asegúrate de que UAC esté habilitado en el equipo de prueba.
    -   Asegúrate de ejecutar la prueba en un equipo que tenga una pantalla lo suficientemente amplia.
    -   Si tu aplicación no puede iniciarse aun cuando la plataforma de prueba cumple con los requisitos de [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication), puedes solucionar el problema revisando el registro de eventos de activación. Para encontrar estas entradas en el registro de eventos:
        1.  Abra eventvwr.exe y navegue hasta el \\ nodo de la aplicación registros de Windows \\ .
        2.  Filtra la vista para que se muestren los identificadores de eventos: 5900-6000.
        3.  Revisa las entradas del registro para encontrar información que pueda explicar por qué la aplicación no se inicia.
    -   Soluciona los problemas del archivo mediante identificación y corrección. Recompila y vuelve a probar la aplicación.
-   Recursos adicionales
    -   [Usar comprobador de aplicaciones dentro del ciclo de vida de desarrollo de software](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Comprobador de aplicación]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Usar comprobador de aplicaciones](https://www.microsoft.com/?ref=go)
    -   [Archivos dll de AppInit](https://www.microsoft.com/?ref=go)
    -   [  Minimizar el tiempo de inicio (aplicaciones de la Tienda Windows con C#/VB/C++ y XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Prueba de compatibilidad y resistencia

-   Información previa
    -   Esta comprobación validará dos aspectos de una aplicación, es decir, el archivo ejecutable principal de la aplicación, por ejemplo, el punto de entrada de la aplicación orientado al usuario debe manifestarse por compatibilidad, así como declarar el GUID derecho. Para admitir esta nueva prueba, el informe tendrá un subnodo bajo ' Compatibility & Resiliency '. Se producirá un error en la aplicación si faltan una o ambas condiciones.
-   Detalles de las pruebas
    -   **Compatibilidad:** Las aplicaciones deben ser totalmente funcionales sin usar los modos de compatibilidad de Windows, los mensajes de AppHelp u otras correcciones de compatibilidad. Un manifiesto de compatibilidad permite que Windows proporcione a la aplicación el comportamiento de compatibilidad adecuado en las distintas versiones del sistema operativo.
    -   **AppInit:** Las aplicaciones no deben enumerar las DLL para cargarlas en la \_ \_ \\ clave del registro HKEY local Machine software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit \_ dll.
    -   **Switchback:** La aplicación debe proporcionar el manifiesto de Switchback. Si falta el manifiesto, el kit para la certificación de aplicaciones de Windows proporciona un mensaje de advertencia. El kit para la certificación de aplicaciones de Windows también comprobará que el manifiesto contiene un GUID de sistema operativo válido.
-   Acciones correctivas
    -   Corrija el componente de la aplicación que usa la corrección de compatibilidad.
    -   Asegúrese de que la aplicación no depende de las correcciones de compatibilidad para su funcionalidad.
    -   Asegúrese de que la aplicación está en manifiesto y que la sección de compatibilidad incluye los valores adecuados.
-   Información adicional
    -   Consulte [archivos dll de Appinit](/previous-versions/windows/apps/hh994639(v=win.10)) para obtener más información.

## <a name="windows-security-best-practices-test"></a>Prueba de prácticas recomendadas de seguridad de Windows

-   Información previa
    -   Una aplicación no debe cambiar la configuración de seguridad de Windows predeterminada
-   Detalles de las pruebas
    -   Prueba la seguridad de la aplicación mediante la ejecución del analizador de la superficie expuesta a ataques. El enfoque será agregar categorías de error por cada prueba. Por ejemplo, algunas categorías de pruebas de seguridad pueden incluir:
        -   Error de inicialización
        -   Error de arquitectura de seguridad
        -   Posible error de desbordamiento de búfer
        -   Error de bloqueo
    -   Para obtener más información, consulte [aquí](/previous-versions/windows/hh920280(v=win.10)).
-   Acciones correctivas
    -   Solucione los problemas y solucione el problema identificado por las pruebas. Recompila y vuelve a probar la aplicación.

## <a name="windows-security-features-test"></a>Prueba de características de seguridad de Windows

-   Información previa
    -   Las aplicaciones deben participar en las características de seguridad de Windows. Cambiar las protecciones de seguridad de Windows predeterminadas puede causar grandes riesgos a los clientes.
-   Detalles de las pruebas
    -   Prueba la seguridad de la aplicación ejecutando el analizador binario BinScope. Para obtener más información, consulte [aquí](/previous-versions/windows/hh920280(v=win.10)).
-   Acciones correctivas
    -   Solucione los problemas y solucione el problema identificado por las pruebas. Recompila y vuelve a probar la aplicación.

## <a name="high-dpi-test"></a>Prueba de PPP alta

Se recomienda encarecidamente que las aplicaciones Win32 tengan reconocimiento de PPP. Es la clave para hacer que la interfaz de usuario de la aplicación tenga un aspecto coherente en una amplia variedad de valores de pantalla de alta ppp. Una aplicación no compatible con PPP que se ejecuta en una configuración de pantalla de PPP alta puede tener problemas como el escalado incorrecto de elementos de la interfaz de usuario, texto recortado e imágenes borrosas. Hay dos maneras de declarar una aplicación con reconocimiento de PPP. Uno es declarar ppp.

-   Información previa
    -   Esta comprobación validará dos aspectos de una aplicación, los archivos ejecutables principales, por ejemplo, los puntos de entrada de la aplicación orientada al usuario se deben manifestar para un reconocimiento de PPP alto y que se llame a las API adecuadas para admitir un valor de PPP alto. Se producirá un error en la aplicación si faltan una o ambas condiciones. Esta comprobación presentará una nueva sección en el informe de escritorio, vea el ejemplo siguiente.
-   Detalles de las pruebas
    -   La prueba generará una advertencia cuando se detecten algunas de las siguientes opciones:
        -   El archivo EXE principal no declara el reconocimiento de PPP en su manifiesto y no llama a la API de SetProcessDPIAware. (Avise al desarrollador si olvida agregar el manifiesto de reconocimiento de PPP).
        -   El archivo EXE principal no declara el reconocimiento de PPP en su manifiesto, pero llama a la API SetProcessDPIAware (avise al desarrollador de que debe usar el manifiesto para declarar el reconocimiento de PPP en lugar de llamar a la API).
        -   MainEXE declara el reconocimiento de PPP en su manifiesto, pero también llama a la API de SetProcessDPIAware (advertir al desarrollador que llama a esa API no es necesario).
        -   En el caso de los archivos binarios que no son exe principales, si llaman a la API, se ofrece una advertencia (no se recomienda llamar a la API).
-   Acciones correctivas
    -   No se recomienda el uso de la función SetProcessDPIAware (). Si un archivo DLL almacena en memoria caché los valores de PPP durante su inicialización, la invocación de SetProcessDPIAware () en la aplicación puede generar una condición de carrera. La llamada a la función SetProcessDPIAware () en un archivo DLL no es una buena práctica.
-   Información adicional
    -   [Escribir aplicaciones de alta PPP](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 