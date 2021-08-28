---
title: Control de cuentas de usuario para desarrolladores de juegos
description: En este artículo se describen las directrices y los procedimientos recomendados para que los desarrolladores de juegos trabajen de forma eficaz con la característica de seguridad control de cuentas de usuario (UAC) introducida en Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb8b6ac31ef13e3ace4d439c82f4708673aeffb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886067"
---
# <a name="user-account-control-for-game-developers"></a>Control de cuentas de usuario para desarrolladores de juegos

En este artículo se describen las directrices y los procedimientos recomendados para que los desarrolladores de juegos trabajen de forma eficaz con la característica de seguridad control de cuentas de usuario (UAC) introducida en Windows Vista.

-   [Información general sobre el control de cuentas de usuario](#overview-of-user-account-control)
-   [Cuentas de usuario en Windows Vista](#user-accounts-in-windows-vista)
-   [Acceso a archivos como usuario estándar](#file-access-as-a-standard-user)
-   [Acceso al Registro como usuario estándar](#registry-access-as-a-standard-user)
-   [Elevación de privilegios](#privilege-elevation)
-   [Implicaciones de UAC con CreateProcess()](#uac-implications-with-createprocess)
-   [Establecer el nivel de ejecución en el manifiesto de aplicación](#setting-the-execution-level-in-the-application-manifest)
-   [Insertar un manifiesto en Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilidad de UAC con juegos antiguos](#uac-compatibility-with-older-games)
-   [Escenarios y manifiestos heredados](#legacy-scenarios-and-manifests)
-   [Conclusión](#conclusion)
-   [Lecturas adicionales](#further-reading)

## <a name="overview-of-user-account-control"></a>Información general sobre el control de cuentas de usuario

Control de cuentas de usuario (UAC), introducido en Windows Vista, es una característica de seguridad diseñada para ayudar a evitar que atacantes malintencionados usen puntos débiles o errores encontrados en aplicaciones de uso general para modificar el sistema operativo u otros programas instalados. Esto se logra mediante la ejecución de la gran mayoría de los programas y procesos como un usuario estándar (también conocido como usuario limitado, usuario restringido o usuario Least-Privileged) incluso si la cuenta del usuario actual tiene credenciales administrativas. Un proceso con privilegios de usuario estándar tiene muchas restricciones inherentes que le impiden realizar cambios en todo el sistema.

UAC también es responsable de la elevación de privilegios de un proceso mediante el uso de un esquema de autenticación basado en diálogos iniciado tras la ejecución de determinados procesos que se designan como que requieren privilegios administrativos. La elevación de privilegios permite a los administradores ejecutar la mayoría de sus aplicaciones en un nivel de privilegios seguro (el mismo que cualquier otro usuario estándar), pero también permite procesos y operaciones que requieren privilegios administrativos. UAC admite la autenticación por encima del final para que un administrador pueda conceder privilegios elevados a un programa mientras un usuario estándar está conectado actualmente al sistema.

La característica UAC está habilitada de forma predeterminada. Aunque es posible que un administrador deshabilite UAC en todo el sistema, esto tiene una serie de ramificaciones negativas. En primer lugar, esto debilite la seguridad de todas las cuentas administrativas, ya que todos los procesos se ejecutarían con credenciales administrativas, incluso cuando la mayoría de las aplicaciones no las requieren realmente. Con UAC deshabilitado, una aplicación de usuario estándar que expone una vulnerabilidad de seguridad que se puede aprovechar puede usarse para robar información privada, instalar rootkits o spyware, destruir la integridad del sistema o hospedar ataques de virus en otros sistemas. Mientras que con UAC habilitado, la ejecución de la mayoría del software como usuario estándar limita en gran medida los posibles daños de este tipo de error. En segundo lugar, desactivar UAC deshabilita muchas de las soluciones alternativas para la compatibilidad de aplicaciones que permiten a los verdaderos usuarios estándar ejecutar correctamente una amplia gama de aplicaciones. La deshabilitación de UAC nunca debe recomendarse como solución alternativa de compatibilidad.

Es importante tener en cuenta que las aplicaciones deben procurar usar solo los derechos de usuario estándar si es posible. Aunque los administradores pueden elevar fácilmente los privilegios de un proceso, la elevación todavía requiere la interacción del usuario y la confirmación cada vez que se ejecuta una aplicación que requiere credenciales administrativas. Esta elevación también debe realizarse en el momento en que se inicia el programa, por lo que requerir credenciales administrativas incluso para una sola operación requiere exponer el sistema a un mayor riesgo durante todo el tiempo de ejecución de la aplicación. Los usuarios estándar sin ninguna capacidad para elevar sus privilegios también son comunes en la configuración familiar y empresarial. "Ejecutar como administrador" no es una buena solución alternativa para la compatibilidad, expone al usuario y al sistema a un mayor riesgo de seguridad y crea frustración para los usuarios en muchas situaciones.

> [!Note]  
> La característica Control de cuentas de usuario introducida en Windows Vista también está presente en Windows 7. Aunque la experiencia del usuario al trabajar con las distintas características del sistema se ha mejorado con respecto al control de cuentas de usuario, el impacto en las aplicaciones es básicamente el mismo. Todas las recomendaciones Windows Vista de este artículo también se aplican a Windows 7. Para obtener más información sobre los cambios en la interfaz de usuario de UAC Windows 7, vea Interfaz de usuario : Actualizaciones del cuadro de [diálogo Control de cuentas de usuario](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>Cuentas de usuario en Windows Vista

Windows Vista clasifica cada usuario en dos tipos de cuenta de usuario: administradores y usuarios estándar.

Una cuenta de usuario estándar es similar a una cuenta de usuario limitado en Windows XP. Al igual que en Windows XP, un usuario estándar no puede escribir en la carpeta Archivos de programa, no puede escribir en la parte HKEY LOCAL MACHINE del Registro y no puede realizar tareas que modifiquen el sistema, como instalar un controlador en modo kernel o acceder a espacios de proceso de nivel de \_ \_ sistema.

La cuenta de administrador ha cambiado significativamente desde Windows xp se publicó. Anteriormente, todos los procesos iniciados por un miembro del grupo Administradores tenían privilegios administrativos. Con UAC habilitado, todos los procesos se ejecutan con privilegios de usuario estándar, a menos que un administrador lo eleva específicamente. Esta diferencia hace que las cuentas del grupo Administradores sea más seguras al reducir el riesgo de seguridad que suponen los posibles errores en la mayoría de los programas.

Es importante que todas las aplicaciones, especialmente los juegos, funcionen de forma eficaz y responsable cuando se ejecutan como un proceso de usuario estándar. Todas las operaciones que requieren privilegios administrativos deben realizarse en el momento de la instalación o mediante programas auxiliares que soliciten explícitamente credenciales administrativas. Aunque la elevación de privilegios es bastante trivial para un miembro del grupo Administradores, los usuarios estándar deben aplazar a alguien con credenciales administrativas para escribir físicamente su contraseña para elevar los privilegios. Dado que las cuentas protegidas por controles parentales deben ser usuarios estándar, esta será una situación muy común para los jugadores que usan Windows Vista.

Si el juego ya está trabajando en Windows XP con cuentas de usuario limitado, el paso a Control de cuentas de usuario en Windows Vista debería ser muy sencillo. La mayoría de estas aplicaciones funcionarán tal y como están, aunque se recomienda encarecidamente agregar un manifiesto de aplicación. (Los manifiestos se describen más adelante en este tema en [Establecer el nivel de ejecución en el manifiesto de aplicación).](#setting-the-execution-level-in-the-application-manifest)

## <a name="file-access-as-a-standard-user"></a>Acceso a archivos como usuario estándar

El aspecto del juego más afectado por las restricciones de usuario estándar es la organización del sistema de archivos y la accesibilidad. Nunca debe suponer que el juego puede escribir archivos en la carpeta donde está instalado el juego. En Windows Vista, por ejemplo, el sistema operativo debe elevar los privilegios de un usuario para que una aplicación pueda escribir en la carpeta Archivos de programa. Para evitar esto, debe clasificar los archivos de datos del juego por ámbito y accesibilidad, y usar la función [**SHGetFolderPath,**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) junto con las constantes CSIDL proporcionadas por el shell de Windows, para generar las rutas de acceso de archivo adecuadas. Las constantes CSIDL corresponden a carpetas conocidas del sistema de archivos que el sistema operativo usa y promueve para crear particiones de archivos globales y específicos del usuario.

Si se intenta crear o escribir un archivo o directorio en una carpeta que no concede permiso de escritura al proceso, se producirá un error en Windows Vista si la aplicación no tiene privilegios administrativos. Si el ejecutable de juego de 32 bits se ejecuta en modo heredado, dado que no declaró un nivel de ejecución solicitado, sus operaciones de escritura se realizarán correctamente, pero estarán sujetas a la virtualización, como se describe en la sección "Compatibilidad de UAC con juegos anteriores" más adelante en este artículo.

**Tabla 1. Carpetas conocidas**



| Nombre de CSIDL             | Ruta de acceso típica (Windows Vista)                                                   | Derechos de usuario estándar | Derechos de administrador | Ámbito de acceso | Descripción                                                                                                                      | Ejemplos                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ PERSONAL        | C: Documentos \\ de nombre de usuario de \\ \\ usuarios                                                | Lectura/Escritura           | Lectura/Escritura           | Per-User     | Archivos de juego específicos del usuario que se leen y modifican y se pueden manipular fuera del contexto del juego.                          | Capturas de pantalla. Archivos de juegos guardados con una asociación de extensión de archivo. |
| CSIDL \_ LOCAL \_ APPDATA  | C: Nombre \\ de usuario de los usuarios \\ \\ AppData \\ Local                                           | Lectura/Escritura           | Lectura/Escritura           | Per-User     | Archivos de juego específicos del usuario que se leen y modifican y que solo se usan dentro del contexto del juego.                                 | Archivos de caché de juegos. Configuraciones del reproductor.                          |
| CSIDL \_ COMMON \_ APPDATA | C: \\ ProgramData                                                                | Lectura y escritura si es propietario  | Lectura/Escritura           | Todos los usuarios    | Archivos de juego que un usuario puede crear y leer todos los usuarios. El acceso de escritura solo se concede al creador del archivo (propietario). | Perfiles de usuario                                                     |
| ARCHIVOS DE PROGRAMA CSIDL \_ \_  | C: Archivos \\ de programa<br/> o<br/> C: \\ Archivos de programa (x86) <br/> | Solo lectura            | Lectura/Escritura           | Todos los usuarios    | Archivos de juegos estáticos escritos por el instalador del juego leídos por todos los usuarios.                                                    | Recursos de juego, como materiales y mallas.                        |



 

Normalmente, el juego se instalará en una carpeta de la carpeta representada por la constante ARCHIVOS DE PROGRAMA \_ CSIDL. \_ Sin embargo, este no siempre es el caso. En su lugar, debe usar una ruta de acceso relativa del archivo ejecutable al generar cadenas de ruta de acceso a archivos o directorios ubicados en la carpeta de instalación.

También debe evitar las suposiciones codificadas de forma fuerte sobre las rutas de acceso de carpeta conocidas. Por ejemplo, en Windows XP Professional edición de 64 bits y Windows Vista x64, la ruta de acceso de los archivos de programa es C: Archivos de programa (x86) para programas de 32 bits y C: Archivos de programa para programas de \\ \\ 64 bits. Estas rutas de acceso conocidas se cambian de Windows XP y los usuarios pueden volver a configurar la ubicación de muchas de estas carpetas e incluso localizarlas en diferentes unidades. Por lo tanto, use siempre las constantes CSIDL para evitar confusiones y posibles problemas. Windows El programa de instalación comprende estas ubicaciones de carpeta conocidas y moverá los datos al actualizar el sistema operativo desde Windows XP; Por el contrario, el uso de ubicaciones no estándar o rutas de acceso codificadas de forma automática puede producir errores después de una actualización del sistema operativo.

Se debe prestar atención a las sutiles diferencias de facilidad de uso entre las carpetas específicas del usuario especificadas por CSIDL PERSONAL y \_ CSIDL \_ LOCAL \_ APPDATA. La práctica recomendada para seleccionar la constante CSIDL que se va a usar para escribir un archivo es usar CSIDL PERSONAL si se espera que el usuario interactúe con el archivo, como hacer doble clic en él para abrirlo en una herramienta o aplicación, y usar \_ CSIDL LOCAL APPDATA para otros \_ \_ archivos. La aplicación puede aprovechar ambas carpetas para almacenar y organizar archivos de datos específicos del usuario, ya que no hay ninguna diferencia en su ámbito de acceso o nivel de privilegios. Se debe tener cuidado para crear nombres de ruta de acceso que sean lo suficientemente únicos como para no colisionar con otras aplicaciones, pero lo suficientemente corto como para mantener el número de caracteres en la ruta de acceso completa menos que el valor de MAX \_ PATH, 260.

El código siguiente proporciona un ejemplo de cómo escribir un archivo en una carpeta conocida:

``` syntax
#include <windows.h>
#include <shlobj.h>
#include <shlwapi.h>
        ...
        ...
        ...
        TCHAR strPath[MAX_PATH];
        if( SUCCEEDED(
        SHGetFolderPath( NULL, CSIDL_PERSONAL, NULL, SHGFP_TYPE_CURRENT, strPath ) ) )
        {
        PathAppend( strPath, TEXT( "Company Name\\Title" ) );

        if( !PathFileExists( strPath ) )
        {
        if( ERROR_SUCCESS != SHCreateDirectoryEx( NULL, strPath, NULL ) )
        return E_FAIL;
        }

        PathAppend( strPath, TEXT( "gamefile.txt" ) );

        // strPath is now something like:
        // C:\Users\<current user>\Documents\Company Name\Title\gamefile.txt
        // Open the file for writing
        HANDLE hFile = CreateFile(strPath, GENERIC_WRITE, NULL, NULL, CREATE_ALWAYS, FILE_ATTRIBUTE_NORMAL, NULL);

        if( INVALID_HANDLE_VALUE != hFile )
        {
        // TODO: Write to file
        CloseHandle(hFile);
        }
        }
```

## <a name="registry-access-as-a-standard-user"></a>Acceso al Registro como usuario estándar

El acceso al Registro por parte de un usuario estándar está restringido de forma similar a la del sistema de archivos. A un usuario estándar se le permite el acceso de lectura a todas las claves del Registro. Sin embargo, el acceso de escritura solo se concede al subárbol HKEY CURRENT USER (HKCU), que se asigna internamente a la subclave específica del usuario \_ \_ HKEY \_ USERS Security ID (SID) del usuario \\ actual. Una aplicación que necesita escribir en cualquier ubicación del Registro que no sea HKEY \_ CURRENT \_ USER requiere privilegios administrativos.

Si la aplicación de 32 bits no contiene un nivel de ejecución solicitado en su manifiesto, todas las escrituras en HKEY LOCAL MACHINE Software se \_ \_ \\ virtualizarán, mientras que las escrituras en otras ubicaciones fuera de HKEY CURRENT USER producirán un \_ \_ error.

No se recomienda almacenar datos persistentes en el Registro, como la configuración de un usuario. El método preferido para almacenar datos persistentes del juego es escribir los datos en el sistema de archivos mediante una llamada a [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) y obtener el valor de una constante CSIDL, descrita en la sección anterior.

## <a name="privilege-elevation"></a>Elevación de privilegios

En Windows Vista, cualquier aplicación que requiera privilegios administrativos debe declarar una solicitud para un nivel de ejecución administrativo en su manifiesto (descrito en la sección siguiente, Establecer el nivel de ejecución en el manifiesto de [aplicación).](#setting-the-execution-level-in-the-application-manifest)

La elevación, como se conoce, es el procedimiento controlado por UAC para promover un proceso a un proceso administrativo. Los privilegios de un proceso solo se pueden elevar en el momento de la creación. Una vez creado, un proceso nunca se promoverá a un nivel de privilegios superior. Por este motivo. Las operaciones que requieren credenciales administrativas deben aislarse para separar instaladores y otros programas auxiliares.

Tras la ejecución de un programa, UAC inspecciona el nivel de ejecución solicitado en el manifiesto y, si se requieren privilegios elevados, solicita al usuario actual uno de los dos cuadros de diálogo estándar: uno para un usuario estándar y otro para un administrador.

Si el usuario actual es un usuario estándar, UAC solicita al usuario las credenciales de un administrador antes de permitir la ejecución del programa.

**Figura 1. Solicitar a un usuario estándar que escriba las credenciales de una cuenta administrativa**

![solicitar a un usuario estándar que escriba las credenciales de una cuenta administrativa](images/uac-prompt-elevation.jpg)

Si el usuario actual es un administrador, UAC solicita permiso al usuario antes de permitir que se ejecute el programa.

**Figura 2. Pedir a un administrador que autorice los cambios en el equipo**

![solicitar a un administrador que autorice los cambios en el equipo](images/uac-prompt-authorization.jpg)

A la aplicación solo se le concederán privilegios administrativos si un usuario estándar proporciona las credenciales administrativas adecuadas o un usuario administrativo proporciona una confirmación. cualquier otra cosa hará que la aplicación finalice.

Es importante tener en cuenta que un proceso con privilegios elevados se ejecuta como el usuario administrativo que escribió las credenciales en el símbolo del sistema de UAC en lugar de como el usuario estándar que ha iniciado sesión actualmente. Esto es similar a **RunAs** en Windows XP, el proceso con privilegios elevados obtiene la carpeta y las claves del Registro del administrador al acceder a los datos por usuario, y todos los programas que inicia el proceso con privilegios elevados también heredan los derechos administrativos y las ubicaciones de las cuentas de usuario. En el caso de los administradores a los que se solicita confirmación **(Continuar** o **Cancelar),** estas ubicaciones coincidirán con las ubicaciones del usuario actual. Sin embargo, en general, los procesos que requieren elevación no deben funcionar con datos por usuario. Tenga en cuenta que esto puede afectar considerablemente a cómo debe funcionar el instalador. Si el instalador, que se ejecuta como administrador, escribe en HKCU o en el perfil de un usuario, es posible que esté escribiendo en una ubicación incorrecta. Considere la posibilidad de crear estos valores por usuario en la primera ejecución del juego.

## <a name="uac-implications-with-createprocess"></a>Implicaciones de UAC con CreateProcess()

El mecanismo de elevación de UAC no se invocará desde una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() de Win32 para iniciar un archivo ejecutable configurado para requerir un nivel de ejecución mayor que el proceso actual. Como resultado, la llamada a **CreateProcess**() producirá un error con [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() que devuelve ERROR \_ ELEVATION \_ REQUIRED. **CreateProcess**() solo se realizará correctamente cuando el nivel de ejecución del destinatario sea igual o menor que el del autor de la llamada. Un proceso sin privilegios elevados que debe generar procesos con privilegios elevados debe hacerlo mediante la función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), lo que hará que el mecanismo de elevación de UAC se desencadene mediante el shell.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Establecer el nivel de ejecución en el manifiesto de aplicación

Para declarar el nivel de ejecución solicitado del juego, agregue una extensión al manifiesto de la aplicación. El código XML siguiente muestra la configuración mínima necesaria para establecer el nivel de ejecución de una aplicación:

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
        <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
                <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
        </ms_asmv2:security>
    </ms_asmv2:trustInfo>
</assembly>
```

En el código anterior, se informa al sistema operativo de que el juego solo requiere privilegios de usuario estándar con la etiqueta siguiente:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Al establecer explícitamente requestedExecutionLevel en "asInvoker", en este ejemplo se afirma al sistema operativo que el juego se comportará correctamente sin privilegios administrativos. Como resultado, UAC deshabilita la virtualización y ejecuta el juego con los mismos privilegios que el invocador, que normalmente son privilegios de usuario estándar, ya que Windows Explorer se ejecuta como usuario estándar.

Se puede informar al sistema operativo de que un juego requiere elevación a privilegios administrativos reemplazando "asInvoker" por "requireAdministrator", para crear la etiqueta siguiente:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Con esta configuración, el sistema operativo solicita al usuario actual uno de los diálogos de elevación estándar de UAC cada vez que se ejecuta el juego. Se recomienda encarecidamente que ningún juego requiera privilegios de administrador para ejecutarse, ya que este diálogo no solo se volverá molesto rápidamente, sino que también hace que el juego sea incompatible con los controles parentales. Piense detenidamente antes de agregar este requisito a cualquier archivo ejecutable.

Un concepto erróneo común es que agregar un manifiesto que establece requestedExecutionLevel en "requireAdministrator" omite la necesidad de un símbolo del sistema de elevación. Esto no es cierto. Simplemente impide que el sistema operativo adije si la aplicación de instalación o actualización necesita privilegios administrativos. Se sigue solicitando al usuario que autorice la elevación.

Windows comprueba la firma de cualquier aplicación marcada para la elevación antes de mostrar el símbolo del sistema de UAC. Un ejecutable grande marcado para elevación tarda más tiempo en comprobarse que un ejecutable pequeño y más tiempo que un ejecutable marcado como "asInvoker". Por lo tanto, los ejecutables de instalación que se extraen de forma automática deben marcarse como "asInvoker" y cualquier parte que deba marcarse como "requireAdministrator" debe colocarse en un archivo ejecutable auxiliar independiente.

El atributo uiAccess, que se muestra en los ejemplos anteriores, siempre debe ser FALSE para juegos. Este atributo especifica si los clientes de automatización de la interfaz de usuario tienen acceso a la interfaz de usuario del sistema protegido y tiene implicaciones de seguridad especiales si se establece en TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Inserción de un manifiesto en Visual Studio

La compatibilidad con manifiestos se agregó por Visual Studio a partir de VS2005. De forma predeterminada, un ejecutable integrado en Visual Studio 2005 (o posterior) tendrá un manifiesto generado automáticamente insertado en él como parte del proceso de compilación. El contenido del manifiesto generado automáticamente depende de determinadas configuraciones de proyecto que especifique en el cuadro de diálogo de propiedades del proyecto.

El manifiesto generado automáticamente por Visual Studio 2005 no contendrá un bloque trustInfo, ya que no hay ninguna manera de configurar el nivel de ejecución de UAC en las propiedades &lt; &gt; del proyecto. La manera preferida de agregar esta información es permitir que VS2005 combine un manifiesto definido por el usuario que contiene el bloque trustInfo con el &lt; &gt; manifiesto generado automáticamente. Esto es tan sencillo como agregar un archivo .manifest a la solución \* que contiene el XML enumerado en la sección anterior. Cuando Visual Studio encuentra un archivo .manifest en la solución, invocará automáticamente la herramienta manifiesto (mt.exe) para combinar los archivos .manifest con el generado automáticamente.

> [!Note]  
> Hay un error en la herramienta manifiesto (mt.exe) proporcionado por Visual Studio 2005 que da como resultado un manifiesto combinado e incrustado que puede causar problemas cuando el archivo ejecutable se ejecuta en Windows XP antes de SP3. El error es el resultado de cómo la herramienta redefine el espacio de nombres predeterminado tras la declaración del &lt; bloque &gt; trustInfo. Afortunadamente, es fácil omitir el problema por completo mediante la declaración explícita de un espacio de nombres diferente en el bloque trustInfo y el ámbito de los nodos secundarios al nuevo espacio &lt; &gt; de nombres. El XML proporcionado en la sección anterior muestra esta corrección.

 

Una advertencia al usar la herramienta mt.exe incluida en Visual Studio 2005 es que generará una advertencia al procesar el bloque trustInfo, ya que la herramienta no contiene un esquema actualizado con el que validar el &lt; &gt; XML. Para solucionar esta advertencia, se recomienda reemplazar todos los archivos mt.exe del directorio de instalación de Visual Studio 2005 (hay varias instancias) por el mt.exe proporcionado en el SDK de Windows más reciente.

A partir de Visual Studio 2008, ahora puede especificar el nivel de ejecución de una aplicación desde el cuadro de diálogo de propiedades del proyecto (figura 3) o mediante la marca del vinculador /MANIFESTUAC. Al establecer estas opciones, Visual Studio 2008 generará e insertará automáticamente un manifiesto con el bloque trustInfo adecuado &lt; en el archivo &gt; ejecutable.

**Figura 3. Establecimiento del nivel de ejecución en Visual Studio 2008**

![establecer el nivel de ejecución en Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

La inserción de un manifiesto en versiones anteriores de Visual Studio sin compatibilidad con manifiestos sigue siendo posible, pero requiere más trabajo del desarrollador. Para obtener un ejemplo sobre cómo hacerlo, examine el proyecto Visual Studio 2003 incluido en cualquier ejemplo del SDK de DirectX antes de la versión de marzo de 2008.

## <a name="uac-compatibility-with-older-games"></a>Compatibilidad de UAC con juegos anteriores

Si parece que el juego guarda y carga correctamente un archivo en el directorio Archivos de programa, pero no hay ninguna evidencia del archivo iOn Windows Vista, cualquier aplicación de 32 bits que no contenga un nivel de ejecución solicitado en su manifiesto se considera una aplicación heredada. Antes de Windows Vista, la mayoría de las aplicaciones las ejecutaban normalmente los usuarios con privilegios administrativos. Como resultado, estas aplicaciones podrían leer y escribir libremente archivos del sistema y claves del Registro, y muchos desarrolladores no realizaron los cambios necesarios para funcionar correctamente en cuentas de usuario limitadas en Windows XP. Sin embargo, Windows Vista, estas mismas aplicaciones producirían un error debido a privilegios de acceso insuficientes en el nuevo modelo de seguridad, que exige la ejecución de usuarios estándar para las aplicaciones heredadas. Para mitigar el impacto de esto, también se agregó la virtualización a Windows Vista. La virtualización mantendrá miles de aplicaciones heredadas funcionando bien en Windows Vista sin necesidad de que esas aplicaciones tengan privilegios elevados en todo momento simplemente para realizar correctamente algunas operaciones menores. se encontró, lo más probable es que el juego se ejecute en modo heredado y esté sujeto a virtualización.

La virtualización afecta al sistema de archivos y al Registro mediante la redirección de las escrituras que distinguen del sistema (y las posteriores operaciones de archivo o registro) a una ubicación por usuario dentro del perfil del usuario actual. Por ejemplo, si una aplicación intenta escribir en el archivo siguiente:

<dl> C: \\ Nombre de la compañía de archivos de programa \\ \\ \\config.ini  
</dl>

la escritura se redirige automáticamente a:

<dl> C: Nombre \\ de usuario de los usuarios \\ \\ AppData Local \\ \\ VirtualStore Program Files Company Name \\ \\ Title \\ \\config.ini  
</dl>

Del mismo modo, si una aplicación intenta escribir un valor del Registro similar al siguiente:

<dl> HKEY \_ LOCAL \_ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

En su lugar, se le redirigirá a:

<dl> HKEY \_ CURRENT \_ USER \\ Software \\ Classes \\ VirtualStore \\ MACHINE \\ Software \\ Company Name \\ Title  
</dl>

Solo se puede acceder a los archivos y las claves del Registro afectadas por la virtualización mediante operaciones de archivo y registro desde aplicaciones virtualizadas que se ejecutan como el usuario actual.

Sin embargo, hay muchas restricciones para la virtualización. Una es que las aplicaciones de 64 bits nunca se ejecutan en modo heredado para las operaciones de compatibilidad sujetas a virtualización en aplicaciones de 32 bits que simplemente producirán un error en 64 bits. Además, si una aplicación heredada que se ejecuta como un usuario estándar intenta escribir cualquier tipo de archivo ejecutable en una ubicación que requiere credenciales administrativas, la virtualización no se producirá y se producirá un error en la escritura.

**Figura 4. Proceso de virtualización**

![proceso de virtualización](images/uac-virtualization-process.jpg)

Cuando una aplicación heredada intenta una operación de lectura en ubicaciones sensibles al sistema en el registro o el sistema de archivos, primero se busca en las ubicaciones virtuales. Si no se encuentra el archivo o la clave del Registro, el sistema operativo accede a las ubicaciones predeterminadas del sistema.

La virtualización se quitará de las versiones posteriores Windows por lo que es importante no confiar en esta característica. En su lugar, debe configurar explícitamente el manifiesto de aplicación para privilegios de usuario estándar o administrativos, ya que esto deshabilitará la virtualización. La virtualización tampoco es obvia para los usuarios finales, por lo que aunque la virtualización puede permitir la ejecución de la aplicación, puede generar llamadas de soporte técnico y dificultar la tarea de dar problemas a estos clientes.

Tenga en cuenta que si UAC está deshabilitado, la virtualización también se deshabilita. Si la virtualización está deshabilitada, las cuentas de usuario estándar se comportan exactamente igual que las cuentas de usuario limitadas en Windows XP y es posible que las aplicaciones heredadas no funcionen correctamente para los usuarios estándar que, de lo contrario, se hubieran comportado correctamente debido a la virtualización.

## <a name="legacy-scenarios-and-manifests"></a>Escenarios y manifiestos heredados

En la mayoría de los escenarios de uso, basta con marcar el .exe con los elementos de manifiesto de UAC correctos y asegurarse de que la aplicación funciona correctamente como usuario estándar es suficiente para una excelente compatibilidad con UAC. La mayoría de los jugadores ejecutan Windows Vista o Windows 7 con control de cuentas de usuario habilitado. Para Windows XP y los usuarios de Windows Vista o Windows7 con la característica Control de cuentas de usuario deshabilitada, normalmente se ejecutan con cuentas de administrador. Aunque se trata de un modo de funcionamiento menos seguro, por lo general no se encontrará con ningún problema de compatibilidad adicional, aunque, como se indicó anteriormente, deshabilitar UAC también deshabilita la virtualización.

Hay un caso especial que merece la pena tener en cuenta cuando el programa está marcado como "requireAdministrator" en el manifiesto de UAC. En Windows XP y en Windows Vista o Windows 7 con control de cuentas de usuario deshabilitado, el sistema omite los elementos del manifiesto de UAC. En esta situación, los usuarios con cuentas de administrador siempre ejecutarán todos los programas con derechos de administrador completos y, por tanto, estos programas funcionarán según lo previsto. Windows Sin embargo, los usuarios restringidos de XP y los usuarios estándar que se ejecutan en Windows Vista o Windows 7 siempre ejecutarán estos programas con derechos restringidos y se producirá un error en todas las operaciones de nivel de administrador. Por lo tanto, se recomienda que los programas marcados como "requiretAdministrator" llamen a [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) en el inicio y muestren un mensaje de error irresistente si devuelve FALSE. En el escenario de mayoría anterior, esto siempre se realizará correctamente, pero proporciona una mejor experiencia de usuario y un mensaje de error claro para esta situación poco frecuente.

## <a name="conclusion"></a>Conclusión

Como desarrollador de juegos que tiene como destino Windows entorno de varios usuarios, es fundamental que diseñe el juego para que funcione de forma eficaz y responsable. El archivo ejecutable principal del juego no debe depender de privilegios administrativos. Esto no solo evita la aparición de avisos de elevación cada vez que se ejecuta el juego, lo que puede afectar negativamente a la experiencia general del usuario, sino que también permite que el juego aproveche otras características que requieren ejecución con privilegios de usuario estándar, como los controles parentales.

Las aplicaciones que están diseñadas correctamente para funcionar como con las credenciales de un usuario estándar (o usuario limitado) en versiones anteriores de Windows no se verán afectadas por el UAC que se ejecutará sin elevación. Sin embargo, deben incluir un manifiesto con el nivel de ejecución solicitado establecido en "asInvoker" para cumplir con los estándares de aplicación para Vista.

## <a name="further-reading"></a>Lecturas adicionales

Para obtener ayuda con el diseño de aplicaciones para Windows Vista que son compatibles con el control de cuentas de usuario, descargue las siguientes instrucciones: requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad con el control de cuentas [de usuario.](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

En estas white paper se proporcionan pasos detallados sobre el proceso de diseño, junto con ejemplos de código, requisitos y procedimientos recomendados. En este documento también se detallan las actualizaciones técnicas y los cambios en la experiencia del usuario en Windows Vista.

Para obtener más información sobre el control de cuentas de usuario, [visite Windows Vista: Control de cuentas de usuario](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) en Microsoft [TechNet](https://www.microsoft.com/technet/).

Otro recurso útil es el artículo [Teach Your Apps To Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control), from MSDN [Magazine](/archive/msdn-magazine/msdn-magazine-issues), January 2007. En este artículo se de abordan los problemas generales de compatibilidad de aplicaciones, así como las ventajas y los problemas del uso de Windows Installer en Windows Vista.

Para obtener más información sobre el error y la corrección de mt.exe, la herramienta que usa Visual Studio 2005 para combinar e insertar automáticamente un manifiesto en un archivo ejecutable, vea [Exploring Manifests Part 2: Default Namespaces and UAC Manifests in Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) (Exploración de manifiestos parte 2: espacios de nombres predeterminados y manifiestos de UAC en Windows Vista) en el blog de Chris Jackson en [MSDN.](/archive/blogs/)

 

