---
title: Pruebas del Kit para la certificación de aplicaciones en Windows
description: A continuación se muestran los detalles de las pruebas para certificar las aplicaciones de dekstop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b251104418e8eeff88d4d0188e34628b5ec1bf3b54015550084d4a0e9df567e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086568"
---
# <a name="windows-app-certification-kit-tests"></a>Pruebas del Kit para la certificación de aplicaciones en Windows

A continuación se muestran los detalles de las pruebas para certificar las aplicaciones de dekstop. Para obtener información, consulte Uso [del kit de certificación Windows aplicaciones.](using-the-windows-app-certification-kit.md)

-   [Instalación reversible limpia](#clean-reversible-install)
-   [Instalación en la prueba de carpetas correcta](#install-to-the-correct-folders-test)
-   [Prueba de archivos firmados digitalmente](#digitally-signed-file-test)
-   [Compatibilidad con la prueba Windows x64](#support-x64-windows-test)
-   [Prueba de comprobación de versiones del sistema operativo](#os-version-checking-test)
-   [Prueba de control de cuentas de usuario (UAC)](#user-account-control-uac-test)
-   [Cumplimiento de los mensajes del administrador de reinicio del sistema](#adhere-to-system-restart-manager-messages)
-   [Caja fuerte de modo de recuperación](#safe-mode-test)
-   [Prueba de sesión multiusuario](#multiuser-session-test)
-   [Prueba de bloqueos y bloqueos](#crashes-and-hangs-test)
-   [Prueba de compatibilidad y resistencia](#compatibility-and-resiliency-test)
-   [Seguridad de Windows de procedimientos recomendados](#windows-security-best-practices-test)
-   [Prueba de características de seguridad de Windows](#windows-security-features-test)
-   [Prueba de valores altos de PPP](#high-dpi-test)

## <a name="clean-reversible-install"></a>Instalación reversible limpia

Instala y desinstala la aplicación y comprueba si hay archivos residuales y entradas del Registro.

-   Información previa
    -   Una instalación limpia y reversible permite a los usuarios implementar y quitar aplicaciones. Para superar esta prueba, la aplicación debe hacer lo siguiente:
        -   La aplicación no obliga al sistema a reiniciarse inmediatamente después de instalar o desinstalar la aplicación. *El proceso de instalación o desinstalación de una aplicación nunca debe requerir un reinicio del sistema justo después de que se complete. Si esto requiere que se reinicie el sistema, los usuarios deben poder reiniciar el sistema a su comodidad.*
        -   La aplicación no depende de los nombres de archivo cortos (SFN) de la versión 8.3. *Los procesos de instalación y desinstalación de la aplicación deben poder usar nombres de archivo largos y rutas de acceso de carpeta.*
        -   La aplicación no bloquea la instalación o desinstalación silenciosas
        -   La aplicación realiza las entradas necesarias en el registro del sistema. *Windows herramientas de inventario y herramientas de telemetría requieren información completa sobre las aplicaciones instaladas. Los instaladores de aplicaciones deben crear las entradas del Registro correctas para permitir la detección y desinstalación correctas.*
    -   Si usa un instalador basado en MSI, MSI crea automáticamente las entradas del Registro siguientes. Si no usa un instalador MSI, el módulo de instalación debe crear las siguientes entradas del Registro durante la instalación:
        -   DisplayName
        -   InstallLocation
        -   Publisher
        -   UninstallString
        -   VersionMajor o MajorVersion
        -   VersionMinor o MinorVersion
    -   La aplicación debe quitar todas sus entradas en Agregar o quitar programas.
-   Detalles de las pruebas
    -   Esta prueba comprueba los procesos de instalación y desinstalación de la aplicación para ver el comportamiento necesario.
-   Acción correctora
    -   Revise el diseño y el comportamiento de la aplicación con los requisitos descritos anteriormente.

## <a name="install-to-the-correct-folders-test"></a>Instalación en la prueba de carpetas correcta

Comprueba que la aplicación escribe sus archivos de programa y datos en las carpetas correctas.

-   Información previa
    -   Las aplicaciones deben tener el sistema de usuario y las carpetas por usuario correctamente para que puedan acceder a los datos y la configuración que necesita, a la vez que protegen los datos y la configuración del usuario frente al acceso no autorizado.
-   Carpetas de archivos de programa
    -   La aplicación debe instalarse en la carpeta Archivos de programa de forma predeterminada (%ProgramFiles% para aplicaciones nativas de 32 y 64 bits, y %ProgramFiles(x86)% para aplicaciones de 32 bits que se ejecutan en x64).
    -   **Nota:** La aplicación no debe almacenar datos de usuario ni datos de aplicación en una carpeta Archivos de programa debido a los permisos de seguridad configurados para esta carpeta.
    -   Las ACL de Windows carpetas del sistema solo permiten a las cuentas de administrador leerlas y escribir en ellas. Como resultado, las cuentas de usuario estándar no tendrán acceso a estas carpetas. Sin embargo, la virtualización de archivos permite a las aplicaciones almacenar un archivo, como un archivo de configuración, en una ubicación del sistema que normalmente solo pueden escribir los administradores. La ejecución de programas como un usuario estándar en esta situación podría producir un error si no puede acceder a un archivo necesario.
    -   Las aplicaciones deben [usar Carpetas conocidas](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) para asegurarse de que podrán acceder a sus datos.
    -   **Nota:** Windows virtualización de archivos para mejorar la compatibilidad de aplicaciones y eliminar problemas cuando las aplicaciones se ejecutan como un usuario estándar en Windows. La aplicación no debe confiar en que la virtualización esté presente en versiones futuras de Windows.
-   Carpetas de datos de aplicación específicas del usuario
    -   En las instalaciones "por máquina", la aplicación no debe escribir datos específicos del usuario durante la instalación. Los datos de instalación específicos del usuario solo se deben escribir cuando un usuario inicia la aplicación por primera vez. Esto se debe a que no hay ninguna ubicación de usuario correcta en la que almacenar los datos en el momento de la instalación. Los intentos de una aplicación de modificar los comportamientos de asociación predeterminados en el nivel de equipo después de la instalación no se realizarán correctamente. En su lugar, los valores predeterminados se deben reclamar en un nivel por usuario, lo que impide que varios usuarios sobrescriban los valores predeterminados de los demás.
    -   Todos los datos de aplicación exclusivos de un usuario específico y que no se compartan con otros usuarios del equipo deben almacenarse en \\ <username> \\ Users AppData.
    -   Todos los datos de la aplicación que deben compartirse entre los usuarios del equipo deben almacenarse en ProgramData.
-   Otras carpetas del sistema y claves del Registro
    -   La aplicación nunca debe escribir directamente en el directorio Windows y subdirectorios o . Use los métodos correctos para instalar archivos, como fuentes o controladores, en estos directorios.
    -   Las aplicaciones no se deben iniciar automáticamente al iniciarse, por ejemplo, agregando una entrada a una o varias de estas ubicaciones:
        -   Las claves de ejecución del Registro HKLM o HKCU en Software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Claves de ejecución del Registro HKLM o HKCU en Software \\ Wow6432Node \\ Microsoft \\ windows \\ CurrentVersion
        -   Menú Inicio Todos los programas > INICIO
-   Detalles de las pruebas
    -   Esta prueba comprueba que la aplicación usa las ubicaciones específicas del sistema de archivos que Windows proporciona para almacenar programas y componentes de software, datos de aplicación compartidos y datos de aplicación específicos de un usuario.
-   Acciones correctivas
    -   Revise cómo la aplicación usa las carpetas del sistema y asegúrese de que las usa correctamente.
-   Excepciones y excepciones
    -   Se requiere una exención para las aplicaciones de escritorio que escriben en la caché global de ensamblados (GAC) (las aplicaciones .NET deben mantener las dependencias de ensamblado privadas y almacenarla en el directorio de la aplicación a menos que se requiera explícitamente compartir un ensamblado).
    -   La instalación en la carpeta Archivos de programas no es un requisito para que los paquetes sw de escritorio logre el logotipo de SW, solo en la categoría Aspectos básicos de SW.

## <a name="digitally-signed-file-test"></a>Prueba de archivos firmados digitalmente

Prueba los archivos ejecutables y los controladores de dispositivo para comprobar que tienen una firma digital válida.

-   Información previa
    -   Los archivos firmados digitalmente hacen posible comprobar que el archivo es original y detectar si el archivo se ha alterado.
    -   El cumplimiento de la firma de código en modo kernel es Windows característica que también se conoce como integridad de código (CI). CI mejora la seguridad de los Windows comprobando la integridad de un archivo cada vez que se carga en la memoria. Ci detecta si el código malintencionado ha modificado un archivo binario del sistema y genera un evento de registro de diagnóstico y auditoría del sistema cuando la firma de un módulo de kernel no se puede comprobar correctamente.
    -   Si la aplicación requiere permisos elevados, el símbolo del sistema de elevación muestra información contextual sobre el archivo ejecutable que solicita acceso con privilegios elevados. Dependiendo de si la aplicación está firmada por Authenticode, es posible que el usuario vea el aviso de consentimiento o el símbolo del sistema de credenciales.
    -   Los nombres seguros impiden que terceros suplante el código, siempre y cuando mantenga la clave privada segura. El .NET Framework comprueba la firma digital cuando carga el ensamblado o lo instala en la GAC. Sin acceso a la clave privada, un usuario malintencionado no puede modificar el código y volver a firmarlo.
-   Detalles de las pruebas
    -   Todos los archivos ejecutables, como los que tienen extensiones de archivo de .exe, .dll, .ocx, .sys, .cpl, .drv y .scr, deben estar firmados con un certificado Authenticode.
    -   Todos los controladores de modo kernel instalados por la aplicación deben tener una firma de Microsoft obtenida a través del programa WHQL o DRS. Todos los controladores de filtro del sistema de archivos deben estar firmados por WHQL.
-   Acción correctora
    -   Firmar los archivos ejecutables de la aplicación.
    -   Use makecert.exe para generar un certificado u obtener una clave de firma de código de una de las entidades de certificación comerciales (CA), como VeriSign, Thawte o una entidad de certificación de Microsoft.
-   Excepciones y excepciones
    -   Las exenciones solo se considerarán para redistribuibles de terceros sin firmar. Se requiere una prueba de comunicación que solicite una versión firmada de los redistribuibles para que se conceda esta exención.
    -   Los paquetes de software de valor agregado del dispositivo están exentos de la certificación del controlador en modo kernel, ya que los controladores deben estar certificados Windows de hardware.

## <a name="support-x64-windows-test"></a>Compatibilidad con la prueba Windows x64

Pruebe la aplicación para asegurarse de que el .exe se ha creado para la arquitectura de plataforma en la que se instalará.

-   Información previa
    -   El archivo ejecutable debe crearse para la arquitectura del procesador en la que está instalado. Algunos archivos ejecutables pueden ejecutarse en una arquitectura de procesador diferente, pero esto no es confiable.
    -   La compatibilidad de la arquitectura es importante porque los procesos de 32 bits no pueden cargar archivos DLL de 64 bits y los procesos de 64 bits no pueden cargar archivos DLL de 32 bits. Del mismo modo, las versiones de 64 bits de Windows no admiten la ejecución de aplicaciones basadas en Windows de 16 bits porque los identificadores tienen 32 bits significativos en Windows de 64 bits para que no se puedan pasar a aplicaciones de 16 bits. Por lo tanto, al intentar iniciar una aplicación de 16 bits se producirá un error en las versiones de 64 bits de Windows.
    -   Los controladores de dispositivos de 32 bits no se pueden ejecutar en versiones de 64 bits de Windows y, por lo tanto, se deben porte a la arquitectura de 64 bits.
    -   Para las aplicaciones en modo de usuario, Windows de 64 bits incluye WOW64, que permite que las aplicaciones de Windows de 32 bits se ejecuten en sistemas que ejecutan Windows de 64 bits, aunque con cierta pérdida de rendimiento. No existe ninguna capa de traducción equivalente para los controladores de dispositivos.
    -   Para mantener la compatibilidad con versiones de 64 bits de Windows, las aplicaciones deben admitir de forma nativa 64 bits o, como mínimo, las aplicaciones basadas en Windows de 32 bits deben ejecutarse sin problemas en sistemas de 64 bits:
        -   Las aplicaciones y sus instaladores no deben contener ningún código de 16 bits ni depender de ningún componente de 16 bits.
        -   El programa de instalación de la aplicación debe detectar e instalar los controladores y componentes adecuados en versiones de 64 bits de Windows.
        -   Los complementos de shell deben ejecutarse en versiones de 64 bits de Windows.
        -   Las aplicaciones que se ejecutan en el emulador de WoW64 no deben intentar omitir los mecanismos de virtualización Wow64. Si hay escenarios específicos en los que las aplicaciones necesitan detectar si se ejecutan en un emulador de WoW64, deben hacerlo llamando a [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Detalles de las pruebas
    -   La aplicación no debe instalar archivos binarios de 16 bits. La aplicación no debe instalar un controlador de modo kernel de 32 bits si se supone que se ejecuta en un equipo de 64 bits.
-   Acciones correctivas
    -   Compile los archivos ejecutables y los controladores para la arquitectura del procesador para la que desea instalarlos.

## <a name="os-version-checking-test"></a>Prueba de comprobación de versiones del sistema operativo

Comprueba cómo la aplicación comprueba la versión de Windows en la que se ejecuta.

-   Información previa
    -   Las aplicaciones comprueban la versión del sistema operativo probando una versión que sea mayor o igual que la versión necesaria para garantizar la compatibilidad con versiones futuras de Windows.
-   Detalles de las pruebas
    -   Simula la ejecución de la aplicación en diferentes versiones de Windows para ver cómo reacciona.
-   Acciones correctivas
    -   Pruebe la versión correcta de Windows probando si la versión actual es mayor o igual que la versión que necesita la aplicación, el servicio o el controlador.
    -   Los instaladores de controladores y los módulos de desinstalación nunca deben comprobar la versión del sistema operativo.
-   Excepciones y excepciones
    -   Se considerarán las exenciones para las aplicaciones que cumplan los siguientes criterios: (solo se aplica a *la certificación de aplicaciones de escritorio).*
        -   Las aplicaciones que se entregan como un paquete que se ejecuta en Windows XP, Windows Vista y Windows 7 y necesitan comprobar la versión del sistema operativo para determinar qué componentes instalar en un sistema operativo determinado.
        -   Aplicaciones que comprueban solo la versión mínima del sistema operativo (solo durante la instalación, no en tiempo de ejecución) mediante el uso solo de las llamadas API aprobadas y enumeran el requisito de versión mínima en el manifiesto de aplicación según sea necesario.
        -   Aplicaciones de seguridad como aplicaciones de firewall y antivirus, utilidades del sistema como utilidades de desfragmentación y aplicaciones de copia de seguridad, y herramientas de diagnóstico que comprueban la versión del sistema operativo mediante solo las llamadas API aprobadas.

## <a name="user-account-control-uac-test"></a>Prueba de control de cuentas de usuario (UAC)

Prueba la aplicación para comprobar que no necesita permisos innecesariamente elevados para ejecutarse.

-   Información previa
    -   Una aplicación que funciona o se instala solo cuando el usuario es administrador obliga a los usuarios a ejecutar la aplicación con permisos innecesariamente elevados, lo que puede permitir que el malware entre en el equipo del usuario.
    -   Cuando los usuarios siempre se ven obligados a ejecutar aplicaciones con tokens de acceso elevados, la aplicación puede servidor como punto de entrada para código malintencionado o engañoso. Este malware puede modificar fácilmente el sistema operativo o, lo que es peor, afectar a otros usuarios. Es casi imposible controlar un usuario que tiene acceso de administrador completo, ya que los administradores pueden instalar aplicaciones y ejecutar cualquier aplicación o script en el equipo. Los administradores de TI siempre buscan formas de crear "escritorios estándar" en los que los usuarios inician sesión como usuarios estándar. Los escritorios estándar reducen considerablemente los costos del departamento de ayuda y reducen la sobrecarga de TI.
    -   La mayoría de las aplicaciones no requieren privilegios de administrador en tiempo de ejecución. Una cuenta de usuario estándar debe poder ejecutarla. Windows aplicaciones deben tener un manifiesto (incrustado o externo) para definir su nivel de ejecución que indique al sistema operativo los privilegios necesarios para ejecutar la aplicación. El manifiesto de aplicación solo se aplica a .exe archivos, no .dll archivos. El Control de cuentas de usuario (UAC) no inspecciona los archivos DLL durante la creación del proceso. Las reglas de UAC no se aplican a servicios Microsoft. El manifiesto de aplicación se puede incrustar o externo.
    -   Para crear un manifiesto, cree un archivo con el nombre <nombre de la aplicación>.exe.manifest y almacénelo en el mismo directorio \_ que el exe. Tenga en cuenta que cualquier manifiesto externo se omite si la aplicación tiene un manifiesto interno.
        -   Por ejemplo, <requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess="true \| false""/>
        -   El proceso principal de la aplicación debe ejecutarse como un usuario estándar (**asInvoker**). Las características administrativas deben moverse a un proceso independiente que se ejecute con privilegios administrativos.
        -   Las aplicaciones orientadas al usuario que requieren privilegios elevados deben estar firmadas por Authenticode.
-   Detalles de las pruebas
    -   Todos los archivos exe orientados al usuario deben marcarse con el atributo asInvoker. Si se marcan como highestAvailable o requireAdministrator, deben estar correctamente firmados por authenticode. Cualquier aplicación exe no debe tener el atributo uiAccess establecido en true. Cualquier archivo exe que se ejecute como servicio se excluye de esta comprobación concreta.
-   Acciones correctivas
    -   Revise el archivo de manifiesto de la aplicación para obtener las entradas y los niveles de permiso correctos.
-   Excepciones y excepciones
    -   Se requiere una exención para las aplicaciones que ejecutan su proceso principal con privilegios elevados **(requireAdministrator** o **highestAvailable).** El proceso principal es el proceso que proporciona el punto de entrada del usuario a la aplicación.
    -   Se tendrán en cuenta las exenciones para los escenarios siguientes:
        -   Herramientas administrativas o del sistema con el nivel de ejecución establecido en **highestAvailable**, **requireAdministrator** o ambos.
        -   Solo la aplicación de marco de automatización de la interfaz de usuario o accesibilidad establece la marca uiAccess en TRUE para omitir el aislamiento de privilegios de la interfaz de usuario (UIPI). Para iniciar correctamente el uso de la aplicación, esta marca debe estar firmada por Authenticode y debe residir en una ubicación protegida en el sistema de archivos, como Archivos de programa.

## <a name="adhere-to-system-restart-manager-messages"></a>Cumplimiento de los mensajes del administrador de reinicio del sistema

Comprueba cómo responde la aplicación a los mensajes de apagado y reinicio del sistema.

-   Información previa
    -   Las aplicaciones deben salir lo antes posible cuando se les notifique que el sistema se está apagando para proporcionar una experiencia de apagado o apagado con capacidad de respuesta para el usuario.
    -   En un apagado crítico, las aplicaciones que devuelven FALSE a [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) se enviarán **a WM \_ ENDSESSION** y se cerrarán, mientras que las que se aloden en respuesta a WM QUERYENDSESSION se terminarán forzadamente. \_
-   Detalles de las pruebas
    -   Examina cómo responde la aplicación a los mensajes de apagado y salida.
-   Acciones correctivas
    -   Si la aplicación no se realiza esta prueba, revise cómo controla estos Windows mensajes:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): las aplicaciones de escritorio deben responder (TRUE) inmediatamente como preparación para un reinicio. Las aplicaciones de consola pueden [**llamar a SetConsoleCtrlHandler para**](/windows/console/setconsolectrlhandler) recibir la notificación de apagado. Los servicios pueden llamar [**a RegisterServiceCtrlHandlerEx para**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) recibir notificaciones de cierre en una rutina de controlador.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) con *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): las aplicaciones deben devolver un valor 0 en 30 segundos y apagarse. Como mínimo, las aplicaciones deben prepararse guardando los datos de usuario y el estado de la información necesaria después de un reinicio.
    -   Las aplicaciones de consola que reciben la **notificación CTRL \_ C \_ EVENT** deben cerrarse inmediatamente. Los controladores no deben vetar un evento de apagado del sistema.
    -   **Nota:** Las aplicaciones que deben bloquear el apagado debido a una operación que no se puede interrumpir deben usar [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) para registrar una cadena que explique el motivo para el usuario. Una vez completada la operación, la aplicación debe llamar [**a ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) para indicar que el sistema se puede apagar.

## <a name="safe-mode-test"></a>Caja fuerte de modo de recuperación

Comprueba si el controlador o servicio está configurado para iniciarse en modo seguro.

-   Información previa
    -   Caja fuerte modo permite a los usuarios diagnosticar y solucionar problemas con Windows. Solo los controladores y servicios necesarios para el funcionamiento básico del sistema operativo o que proporcionan servicios de diagnóstico y recuperación deben cargarse en modo seguro. La carga de otros archivos en modo seguro dificulta la solución de problemas con el sistema operativo.
    -   De forma predeterminada, solo los controladores y servicios que vienen preinstalados con Windows se inician en modo seguro. Todos los demás controladores y servicios deben deshabilitarse a menos que el sistema los requiera para operaciones básicas o con fines de diagnóstico y recuperación.
-   Detalles de las pruebas
    -   Los controladores instalados por la aplicación no deben marcarse para cargarse en modo seguro.
-   Acciones correctivas
    -   Si el controlador o servicio no debe iniciarse en modo seguro, quite las entradas de la aplicación de las claves del Registro.
-   Excepciones y exenciones
    -   Los controladores y servicios que deben comenzar en modo seguro requieren una exención para estar certificados. La solicitud de anulación debe incluir cada controlador y servicio para agregar a las claves del Registro SafeBoot y describir los motivos técnicos por los que el controlador o el servicio deben ejecutarse en modo seguro. El instalador de la aplicación debe registrar todos estos controladores y servicios en estas claves del Registro:
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Nota:** Debe probar los controladores y servicios que desea iniciar en modo seguro para asegurarse de que funcionan en modo seguro sin errores.

## <a name="multiuser-session-test"></a>Prueba de sesión multiusuario

Pruebe cómo se comporta la aplicación cuando se ejecuta en varias sesiones al mismo tiempo.

-   Información previa
    -   Windows los usuarios deben poder ejecutar sesiones simultáneas. Las aplicaciones deben asegurarse de que, cuando se ejecutan en varias sesiones, de forma local o remota, la funcionalidad normal de la aplicación no se ve afectada negativamente. La configuración de la aplicación y los archivos de datos deben ser específicos del usuario y la privacidad y las preferencias del usuario deben restringirse a la sesión del usuario.
-   Detalles de las pruebas
    -   Ejecuta varias instancias simultáneas de la aplicación para probar lo siguiente:
        -   Varias instancias de una aplicación que se ejecutan al mismo tiempo están aisladas entre sí.
    -   Esto significa que los datos de usuario de una instancia no son visibles para otra instancia. El sonido de una sesión de usuario inactiva no debe escucharse en una sesión de usuario activa. En los casos en los que varias instancias de la aplicación usan recursos compartidos, la aplicación debe asegurarse de que no haya ningún conflicto.
        -   Si la aplicación se instaló para varios usuarios, almacena los datos en las carpetas y ubicaciones del Registro correctas.
        -   La aplicación se puede ejecutar en varias sesiones de usuario (conmutación rápida de usuarios) para el acceso local y remoto.
    -   Para asegurarse de esto, la aplicación debe comprobar otras sesiones de Terminal Service (TS) para las instancias existentes de la aplicación. Si la aplicación no admite varias sesiones de usuario o acceso remoto, debe decir claramente esto al usuario cuando se inicia desde dicha sesión.
-   Acción correctiva
    -   Asegúrese de que la aplicación no almacena los archivos de datos de todo el sistema ni la configuración en almacenes de datos específicos del usuario, como Perfil de usuario o HKCU. Si es así, esa información no estará disponible para otros usuarios.
    -   La aplicación debe instalar archivos de configuración y datos de todo el sistema durante la instalación y crear los archivos y la configuración específicos del usuario después de la instalación cuando un usuario la ejecuta.
    -   Asegúrese de que la aplicación no bloquea varias sesiones simultáneas, ya sea de forma local o remota. La aplicación no debe depender de exclusiones mutuas globales u otros objetos con nombre para buscar o bloquear varias sesiones simultáneas.
    -   Si la aplicación no puede permitir varias sesiones simultáneas por usuario, use espacios de nombres por usuario o por sesión para exclusiones mutuas y otros objetos con nombre.

## <a name="crashes-and-hangs-test"></a>Prueba de bloqueos y bloqueos

Supervisa la aplicación durante la prueba de certificación para registrar cuándo se bloquea o se cuelga.

-   Segundo plano
    -   Los errores de la aplicación, como bloqueos y bloqueos, son una interrupción importante para los usuarios y causan frustración. La eliminación de estos errores mejora la estabilidad y la confiabilidad de la aplicación y, en general, proporciona a los usuarios una mejor experiencia de aplicación. Las aplicaciones que dejan de responder o se bloquean pueden originar pérdidas de datos al usuario y que su experiencia no sea buena.
-   Detalles de las pruebas
    -   Probamos la estabilidad y resistencia de la aplicación durante las pruebas de certificación.
    -   El kit Windows de certificación de aplicaciones llama [**a IApplicationActivationManager::ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) para iniciar Windows store. Para que **ActivateApplication** inicie una aplicación, el Control de cuentas de usuario (UAC) debe estar habilitado y la pantalla debe tener una resolución de al menos 1024 x 768 o 768 x 1024. Si alguna de estas condiciones no se cumple, tu aplicación no pasará esta prueba.
-   Acciones correctivas
    -   Asegúrate de que UAC esté habilitado en el equipo de prueba.
    -   Asegúrate de ejecutar la prueba en un equipo que tenga una pantalla lo suficientemente amplia.
    -   Si tu aplicación no puede iniciarse aun cuando la plataforma de prueba cumple con los requisitos de [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication), puedes solucionar el problema revisando el registro de eventos de activación. Para encontrar estas entradas en el registro de eventos:
        1.  Abra eventvwr.exe y vaya al nodo \\ Windows aplicación \\ de registros.
        2.  Filtra la vista para que se muestren los identificadores de eventos: 5900-6000.
        3.  Revisa las entradas del registro para encontrar información que pueda explicar por qué la aplicación no se inicia.
    -   Soluciona los problemas del archivo mediante identificación y corrección. Recompila y vuelve a probar la aplicación.
-   Recursos adicionales
    -   [Uso de Application Verifier dentro del ciclo de vida de desarrollo de software](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Comprobador de aplicación]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Uso de Application Verifier](https://www.microsoft.com/?ref=go)
    -   [Archivos DLL de AppInit](https://www.microsoft.com/?ref=go)
    -   [  Minimizar el tiempo de inicio (aplicaciones de la Tienda Windows con C#/VB/C++ y XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Prueba de compatibilidad y resistencia

-   Información previa
    -   Esta comprobación validará dos aspectos de una aplicación, los ejecutables principales de la aplicación, por ejemplo, el punto de entrada de la aplicación orientado al usuario se debe manifiesto por compatibilidad, así como declarar el GUID correcto. Para admitir esta nueva prueba, el informe tendrá un subnódo en "Compatibilidad & resistencia". Se producirá un error en la aplicación si falta una o ambas condiciones.
-   Detalles de las pruebas
    -   **Compatibilidad:** Las aplicaciones deben ser totalmente funcionales sin usar Windows de compatibilidad, mensajes de AppHelp u otras correcciones de compatibilidad. Un manifiesto de compatibilidad Windows proporcionar a la aplicación el comportamiento de compatibilidad adecuado en las distintas versiones del sistema operativo.
    -   **AppInit:** Las aplicaciones no deben enumerar los archivos DLL que se cargarán en la clave del Registro HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion Windows archivos DLL de \\ \\ \_ AppInit.
    -   **Conmutación por recuperación:** La aplicación debe proporcionar el manifiesto de conmutación por recuperación. Si falta el manifiesto, Windows App Certification Kit proporciona un mensaje de advertencia. Windows El Kit de certificación de aplicaciones también comprobará que el manifiesto contiene un GUID de sistema operativo válido.
-   Acciones correctivas
    -   Corrija el componente de la aplicación que usa la corrección de compatibilidad.
    -   Asegúrese de que la aplicación no se basa en correcciones de compatibilidad para su funcionalidad.
    -   Asegúrese de que la aplicación está manifestada y que la sección de compatibilidad incluye los valores adecuados.
-   Información adicional
    -   Consulte [Archivos DLL de AppInit](/previous-versions/windows/apps/hh994639(v=win.10)) para obtener más información.

## <a name="windows-security-best-practices-test"></a>Seguridad de Windows de procedimientos recomendados

-   Información previa
    -   Una aplicación no debe cambiar la configuración predeterminada Windows seguridad
-   Detalles de las pruebas
    -   Prueba la seguridad de la aplicación mediante la ejecución del Analizador de superficie de ataque. El enfoque será agregar categorías de error por prueba. Por ejemplo, algunas categorías para la prueba de seguridad pueden incluir:
        -   Error de inicialización
        -   Error de arquitectura de seguridad
        -   Posible error de desbordamiento de búfer
        -   Error de bloqueo
    -   Para obtener más información, [consulte aquí](/previous-versions/windows/hh920280(v=win.10)).
-   Acciones correctivas
    -   Solucione y corrija el problema identificado por las pruebas. Recompila y vuelve a probar la aplicación.

## <a name="windows-security-features-test"></a>Windows prueba de características de seguridad

-   Información previa
    -   Las aplicaciones deben participar en Windows de seguridad. Cambiar las protecciones de seguridad de Windows predeterminadas puede causar grandes riesgos a los clientes.
-   Detalles de las pruebas
    -   Prueba la seguridad de la aplicación ejecutando el analizador binario BinScope. Para obtener más información, [consulte aquí](/previous-versions/windows/hh920280(v=win.10)).
-   Acciones correctivas
    -   Solucione y corrija el problema identificado por las pruebas. Recompila y vuelve a probar la aplicación.

## <a name="high-dpi-test"></a>Prueba de valores altos de PPP

Se recomienda encarecidamente que las aplicaciones Win32 sean compatibles con PPP. Es la clave para que la interfaz de usuario de la aplicación se vea correctamente en una amplia variedad de configuraciones de pantalla de valores altos de PPP. Una aplicación sin reconocimiento de PPP que se ejecuta en una configuración de pantalla con valores altos de PPP puede tener problemas, como el escalado incorrecto de elementos de la interfaz de usuario, el texto recortado y las imágenes desenfoque. Hay dos maneras de declarar que una aplicación es compatible con PPP. Una es declarar PPP.

-   Información previa
    -   Esta comprobación validará dos aspectos de una aplicación, los ejecutables principales, por ejemplo, los puntos de entrada de la aplicación orientados al usuario se deben manifiesto para el reconocimiento de VALORES ALTOS DE PPP y que se llama a las API adecuadas para admitir VALORES ALTOS DE PPP. Se producirá un error en la aplicación si falta una o ambas condiciones. Esta comprobación introducirá una nueva sección en el informe de escritorio; vea el ejemplo siguiente.
-   Detalles de las pruebas
    -   La prueba generará una advertencia cuando detectemos cualquiera de las siguientes opciones:
        -   El archivo EXE principal no declara el reconocimiento de PPP en su manifiesto y no llama a setProcessDPIAware API. (Advertir al desarrollador si se olvida de agregar el manifiesto de reconocimiento de PPP).
        -   El exe principal no declara el reconocimiento de PPP en su manifiesto, pero llama a setProcessDPIAware API (advertir al desarrollador de que debe usar el manifiesto para declarar el reconocimiento de PPP en lugar de llamar a la API).
        -   MainEXE declara el reconocimiento de PPP en su manifiesto, pero también llama a setProcessDPIAware API (advertir al desarrollador de que no es necesario llamar a esa API).
        -   En el caso de los archivos binarios que no son exe principales, si llaman a la API, se muestra una advertencia (no se recomienda llamar a la API).
-   Acciones correctivas
    -   No se recomienda el uso de la función SetProcessDPIAware(). Si un archivo DLL almacena en caché la configuración de PPP durante su inicialización, invocar SetProcessDPIAware() en la aplicación puede generar una condición de carrera. Llamar a la función SetProcessDPIAware() en un archivo DLL tampoco es un procedimiento recomendado.
-   Información adicional
    -   [Escritura de aplicaciones con valores altos de PPP](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 