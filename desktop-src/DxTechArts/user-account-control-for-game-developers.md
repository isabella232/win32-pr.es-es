---
title: Control de cuentas de usuario para desarrolladores de juegos
description: En este artículo se describen las instrucciones y los procedimientos recomendados para que los desarrolladores de juegos puedan trabajar de forma eficaz con la característica de seguridad de control de cuentas de usuario (UAC) que se presentó en Windows Vista.
ms.assetid: dbac1c07-73dd-f2bc-3c5c-d6160368a88f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d5533a3fbdd349cc25dfde501a234bbd7b05b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421022"
---
# <a name="user-account-control-for-game-developers"></a>Control de cuentas de usuario para desarrolladores de juegos

En este artículo se describen las instrucciones y los procedimientos recomendados para que los desarrolladores de juegos puedan trabajar de forma eficaz con la característica de seguridad de control de cuentas de usuario (UAC) que se presentó en Windows Vista.

-   [Información general sobre el control de cuentas de usuario](#overview-of-user-account-control)
-   [Cuentas de usuario en Windows Vista](#user-accounts-in-windows-vista)
-   [Acceso a archivos como usuario estándar](#file-access-as-a-standard-user)
-   [Acceso al registro como usuario estándar](#registry-access-as-a-standard-user)
-   [Elevación de privilegios](#privilege-elevation)
-   [Implicaciones de UAC con CreateProcess ()](#uac-implications-with-createprocess)
-   [Establecer el nivel de ejecución en el manifiesto de aplicación](#setting-the-execution-level-in-the-application-manifest)
-   [Incrustar un manifiesto en Visual Studio](#embedding-a-manifest-in-visual-studio)
-   [Compatibilidad de UAC con juegos más antiguos](#uac-compatibility-with-older-games)
-   [Escenarios y manifiestos heredados](#legacy-scenarios-and-manifests)
-   [Conclusión](#conclusion)
-   [Lecturas adicionales](#further-reading)

## <a name="overview-of-user-account-control"></a>Información general sobre el control de cuentas de usuario

El control de cuentas de usuario (UAC), introducido en Windows Vista, es una característica de seguridad diseñada para evitar que los atacantes malintencionados usen puntos débiles o errores detectados en aplicaciones ampliamente usadas para modificar el sistema operativo u otros programas instalados. Esto se consigue mediante la ejecución de la inmensa mayoría de programas y procesos como un usuario estándar (también conocido como usuario limitado, usuario restringido o Least-Privileged usuario), incluso si la cuenta del usuario actual tiene credenciales administrativas. Un proceso con privilegios de usuario estándar tiene muchas restricciones inherentes que impiden realizar cambios en todo el sistema.

UAC también es responsable de la elevación de privilegios de un proceso mediante el uso de un esquema de autenticación basado en un cuadro de diálogo que se inicia tras la ejecución de determinados procesos que se designan como que requieren privilegios administrativos. La elevación de privilegios permite que los administradores ejecuten la mayoría de sus aplicaciones con un nivel de privilegios seguro (igual que con cualquier otro usuario estándar), pero también permiten procesos y operaciones que requieren privilegios administrativos. UAC admite la autenticación por encima del hombro para que un administrador pueda conceder privilegios elevados a un programa mientras un usuario estándar ha iniciado sesión actualmente en el sistema.

La característica UAC está habilitada de forma predeterminada. Aunque es posible que un administrador deshabilite UAC en todo el sistema, hacer esto tiene varias ramificaciones negativas. En primer lugar, esto debilita la seguridad de todas las cuentas administrativas, ya que todos los procesos se ejecutarían con credenciales administrativas, incluso cuando la mayoría de las aplicaciones no las necesiten realmente. Con UAC deshabilitado, una aplicación de usuario estándar que exponga una vulnerabilidad explotable en seguridad puede usarse potencialmente para robar información privada, instalar rootkits o spyware, destruir la integridad del sistema o hospedar ataques Zombie en otros sistemas. Mientras que con UAC habilitado, la mayor parte del software como usuario estándar limita considerablemente el daño potencial de este error. En segundo lugar, al desactivar UAC, se deshabilitan muchas de las soluciones alternativas para la compatibilidad de aplicaciones que permiten a los usuarios estándar verdaderos ejecutar correctamente una amplia gama de aplicaciones. No se recomienda deshabilitar UAC nunca como solución de compatibilidad.

Es importante tener en cuenta que las aplicaciones deben esforzarse por usar solo los derechos de usuario estándar si es posible. Aunque los administradores pueden elevar fácilmente los privilegios de un proceso, la elevación todavía requiere la interacción del usuario y la confirmación cada vez que se ejecuta una aplicación que requiere credenciales administrativas. Esta elevación también debe realizarse en el momento en que se inicia el programa, por lo que requerir credenciales administrativas incluso para una única operación requiere exponer el sistema a un riesgo mayor para todo el tiempo de ejecución de la aplicación. Los usuarios estándar sin la capacidad de elevar sus privilegios también son comunes en la configuración de la familia y el negocio. "Ejecutar como administrador" no es una buena solución para la compatibilidad, expone al usuario y al sistema a un mayor riesgo de seguridad y crea frustración para los usuarios en muchas situaciones.

> [!Note]  
> La característica de control de cuentas de usuario incluida en Windows Vista también está presente en Windows 7. Aunque la experiencia del usuario que trabaja con las distintas características del sistema se ha mejorado con respecto al control de cuentas de usuario, el impacto en las aplicaciones es básicamente el mismo. Todas las recomendaciones de Windows Vista de este artículo se aplican también a Windows 7. Para obtener más información sobre los cambios de la interfaz de usuario de UAC para Windows 7, consulte la [interfaz de usuario: actualizaciones del cuadro de diálogo control de cuentas de usuario](../win7appqual/user-interface---user-account-control-dialog-updates.md).

 

## <a name="user-accounts-in-windows-vista"></a>Cuentas de usuario en Windows Vista

Windows Vista clasifica cada usuario en dos tipos de cuenta de usuario: administradores y usuarios estándar.

Una cuenta de usuario estándar es similar a una cuenta de usuario limitado en Windows XP. Al igual que en Windows XP, un usuario estándar no puede escribir en la carpeta archivos de programa, no puede escribir en la \_ \_ parte de la máquina local HKEY del registro y no puede realizar tareas que modifiquen el sistema, como la instalación de un controlador en modo kernel o el acceso a los espacios de proceso de nivel de sistema.

La cuenta Administrador ha cambiado significativamente desde que se lanzó Windows XP. Anteriormente, todos los procesos iniciados por un miembro del grupo administradores tenían privilegios administrativos. Con UAC habilitado, todos los procesos se ejecutan con privilegios de usuario estándar, a menos que un administrador los haya elevado de forma específica. Esta diferencia hace que las cuentas del grupo de administradores sean más seguras reduciendo el riesgo de seguridad que plantean los posibles errores en la mayoría de los programas.

Es importante que todas las aplicaciones, especialmente los juegos, funcionen de forma eficaz y responsable cuando se ejecutan como un proceso de usuario estándar. Todas las operaciones que requieren privilegios administrativos deben realizarse en el momento de la instalación o mediante programas auxiliares que soliciten explícitamente credenciales administrativas. Aunque la elevación de privilegios es bastante trivial para un miembro del grupo de administradores, los usuarios estándar deben aplazar a alguien con credenciales administrativas para introducir físicamente su contraseña para elevar los privilegios. Como las cuentas protegidas por controles parentales deben ser usuarios estándar, se trata de una situación muy común para los jugadores que usan Windows Vista.

Si el juego ya está trabajando en Windows XP con cuentas de usuario limitado, el cambio a control de cuentas de usuario en Windows Vista debe ser muy sencillo. La mayoría de estas aplicaciones funcionará tal cual, aunque es muy recomendable agregar un manifiesto de aplicación. (Los manifiestos se describen más adelante en este tema para [establecer el nivel de ejecución en el manifiesto de aplicación](#setting-the-execution-level-in-the-application-manifest)).

## <a name="file-access-as-a-standard-user"></a>Acceso a archivos como usuario estándar

El aspecto del juego más afectado por las restricciones de usuario estándar es la organización del sistema de archivos y la accesibilidad. Nunca debe asumir que el juego puede escribir archivos en la carpeta donde está instalado el juego. En Windows Vista, por ejemplo, el sistema operativo debe elevar los privilegios de usuario antes de que una aplicación pueda escribir en la carpeta archivos de programa. Para evitar esto, debe clasificar los archivos de datos de juegos por ámbito y accesibilidad, y usar la función [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) , junto con las constantes CSIDL proporcionadas por el shell de Windows, para generar las rutas de acceso de archivo adecuadas. Las constantes CSIDL se corresponden con las carpetas conocidas del sistema de archivos que el sistema operativo utiliza y promueve para particionar archivos globales y específicos del usuario.

Si intenta crear o escribir un archivo o un directorio en una carpeta que no conceda permiso de escritura en el proceso, se producirá un error en Windows Vista si la aplicación no tiene privilegios administrativos. Si el ejecutable del juego de 32 bits se está ejecutando en el modo heredado, porque no declaraba un nivel de ejecución solicitado, sus operaciones de escritura se realizarán correctamente, pero se someterán a la virtualización, tal y como se describe en la sección "compatibilidad de UAC con juegos más antiguos", más adelante en este artículo.

**Tabla 1. Carpetas conocidas**



| CSIDL nombre             | Ruta de acceso típica (Windows Vista)                                                   | Derechos de usuario estándar | Derechos de administrador | Ámbito de acceso | Descripción                                                                                                                      | Ejemplos                                                          |
|------------------------|--------------------------------------------------------------------------------|----------------------|----------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| CSIDL \_ personal        | C: \\ usuarios \\ nombre de usuario \\ documentos                                                | Lectura/Escritura           | Lectura/Escritura           | Per-User     | Archivos de juegos específicos del usuario que se leen y modifican y que se pueden manipular fuera del contexto del juego.                          | Capturas de pantalla. Archivos de juego guardados con una asociación de extensión de archivo. |
| la \_ AppData local de CSIDL \_  | C: \\ usuarios \\ nombre de usuario \\ AppData \\ local                                           | Lectura/Escritura           | Lectura/Escritura           | Per-User     | Archivos de juegos específicos del usuario que se leen y modifican y que solo se usan en el contexto del juego.                                 | Archivos de caché de juego. Configuraciones del reproductor.                          |
| \_AppData comunes de CSIDL \_ | C: \\ ProgramData                                                                | Lectura/escritura si es propietario  | Lectura/Escritura           | Todos los usuarios    | Archivos de juego que pueden ser creados por un usuario y leídos por todos los usuarios. El acceso de escritura solo se concede al creador del archivo (propietario). | Perfiles de usuario                                                     |
| \_archivos de programa CSIDL \_  | C: \\ archivos de programa<br/> or<br/> C: \\ archivos de programa (x86) <br/> | Solo lectura            | Lectura/Escritura           | Todos los usuarios    | Archivos de juego estáticos escritos por el instalador del juego s que leen todos los usuarios.                                                    | Recursos de juegos, como materiales y mallas.                        |



 

El juego se instalará normalmente en una carpeta en la carpeta representada por la \_ constante de archivos de programa CSIDL \_ . Sin embargo, este no siempre es el caso. En su lugar, debe usar una ruta de acceso relativa desde el archivo ejecutable al generar cadenas de ruta de acceso a archivos o directorios ubicados en la carpeta de instalación.

También debe abstenerse de supuestos codificados de forma rígida sobre las rutas de acceso de carpeta conocidas. Por ejemplo, en Windows XP Professional 64-bit Edition y Windows Vista x64, la ruta de acceso a los archivos de programa es C: \\ archivos de programa (x86) para programas de 32 bits y C: \\ archivos de programa para programas de 64 bits. Estas rutas de acceso conocidas se cambian desde Windows XP y los usuarios pueden volver a configurar la ubicación de muchas de estas carpetas e incluso localizarlas en unidades distintas. Por lo tanto, use siempre las constantes CSIDL para evitar confusiones y posibles problemas. Programa de instalación de Windows entiende estas ubicaciones de carpeta conocidas y moverá los datos al actualizar el sistema operativo desde Windows XP; por el contrario, el uso de ubicaciones no estándar o rutas de acceso codificadas de forma rígida puede producir un error después de una actualización del sistema operativo.

Se debe prestar atención a las diferencias de facilidad de uso entre las carpetas específicas del usuario especificadas por CSIDL \_ personal y CSIDL \_ local \_ appdata. La práctica recomendada para seleccionar la constante CSIDL que se va a usar para escribir un archivo consiste en usar CSIDL \_ personal si se espera que el usuario interactúe con el archivo, como hacer doble clic en él para abrirlo en una herramienta o aplicación, y usar la opción de la \_ \_ AppData local de CSIDL para otros archivos. La aplicación puede aprovechar ambas carpetas para almacenar y organizar archivos de datos específicos del usuario, ya que no hay ninguna diferencia en su ámbito de acceso o nivel de privilegios. Se debe tener cuidado para crear nombres de ruta de acceso que sean lo suficientemente únicos como para no entrar en conflicto con otras aplicaciones, pero lo suficientemente corto como para mantener el número de caracteres de la ruta de acceso completa menos que el valor de la \_ ruta de acceso máxima, 260.

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

## <a name="registry-access-as-a-standard-user"></a>Acceso al registro como usuario estándar

El acceso al registro por parte de un usuario estándar está restringido de manera similar al sistema de archivos. A un usuario estándar se le permite el acceso de lectura a todas las claves del registro. sin embargo, el acceso de escritura solo se concede \_ al \_ subárbol HKEY current user (HKCU), que se asigna internamente a la subclave específica del usuario HKEY \_ ID. \\ de seguridad (SID) del usuario actual. Una aplicación que necesita escribir en cualquier ubicación del registro que no sea el \_ usuario actual de HKEY \_ requiere privilegios administrativos.

Si la aplicación de 32 bits no contiene un nivel de ejecución solicitado en su manifiesto, se virtualizarán todas las escrituras en el \_ software de máquina local HKEY \_ \\ , mientras que las escrituras en otras ubicaciones fuera del \_ usuario actual de HKEY no se realizarán \_ correctamente.

No se recomienda almacenar datos persistentes en el registro, como la configuración de un usuario. El método preferido para almacenar datos persistentes desde el juego es escribir los datos en el sistema de archivos llamando a [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) y obtener el valor de una constante CSIDL, que se describe en la sección anterior.

## <a name="privilege-elevation"></a>Elevación de privilegios

En Windows Vista, todas las aplicaciones que requieran privilegios administrativos deben declarar una solicitud para un nivel de ejecución administrativo en su manifiesto (que se describe en la sección siguiente, [estableciendo el nivel de ejecución en el manifiesto de aplicación](#setting-the-execution-level-in-the-application-manifest)).

La elevación, como se conoce, es el procedimiento controlado por UAC para promover un proceso a un proceso administrativo. Los privilegios de un proceso solo se pueden elevar en el momento de la creación. Una vez creado, un proceso nunca se promoverá a un nivel de privilegios superior. Por esta razón. las operaciones que requieren credenciales administrativas deben aislarse en instaladores independientes y otros programas auxiliares.

Tras la ejecución de un programa, UAC inspecciona el nivel de ejecución solicitado en el manifiesto y, si se requieren privilegios elevados, solicita al usuario actual uno de dos cuadros de diálogo estándar: uno para un usuario estándar y otro para un administrador.

Si el usuario actual es un usuario estándar, UAC solicita al usuario las credenciales de un administrador antes de permitir que se ejecute el programa.

**Figura 1. Pedir a un usuario estándar que escriba las credenciales para una cuenta administrativa**

![pedir a un usuario estándar que escriba las credenciales para una cuenta administrativa](images/uac-prompt-elevation.jpg)

Si el usuario actual es un administrador, UAC solicita permiso al usuario antes de permitir que se ejecute el programa.

**Figura 2. Pedir a un administrador que autorice cambios en el equipo**

![pedir a un administrador que autorice cambios en el equipo](images/uac-prompt-authorization.jpg)

A la aplicación solo se le concederán privilegios administrativos si un usuario estándar proporciona las credenciales administrativas adecuadas o un usuario administrativo proporciona confirmación; todo lo demás hará que la aplicación finalice.

Es importante tener en cuenta que un proceso con privilegios elevados se ejecuta como el usuario administrativo que especificó las credenciales en el símbolo del sistema de UAC en lugar de como el usuario estándar que ha iniciado sesión actualmente. Esto es similar a **runas** en Windows XP. el proceso elevado obtiene la carpeta del administrador y las claves del registro al obtener acceso a los datos de cada usuario, y todos los programas que inicia el proceso elevado también heredan los derechos administrativos y las ubicaciones de las cuentas de usuario. En el caso de los administradores a los que se les pida confirmación (**continuar** o **Cancelar**), estas ubicaciones coincidirán con las ubicaciones del usuario actual. En general, sin embargo, los procesos que requieren elevación no deben funcionar en los datos por usuario. Tenga en cuenta que esto puede afectar de forma significativa a cómo debe funcionar el instalador. Si el instalador, que se ejecuta como administrador, escribe en HKCU o en el perfil de un usuario, es posible que pueda escribir en la ubicación equivocada. Considere la posibilidad de crear estos valores por usuario en la primera ejecución del juego.

## <a name="uac-implications-with-createprocess"></a>Implicaciones de UAC con CreateProcess ()

El mecanismo de elevación de UAC no se invocará desde una llamada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)() de Win32 para iniciar un ejecutable que esté configurado para requerir un nivel de ejecución más alto que el proceso actual. Como resultado, se producirá un error en la llamada a **CreateProcess**() con [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)() que devuelve la elevación de errores \_ \_ necesaria. **CreateProcess**() solo se realizará correctamente cuando el nivel de ejecución del destinatario sea igual o menor que el del llamador. Un proceso no elevado que debe generar procesos elevados debe hacerlo mediante la función [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)(), lo que hará que el mecanismo de elevación de UAC se desencadene por medio del shell.

## <a name="setting-the-execution-level-in-the-application-manifest"></a>Establecer el nivel de ejecución en el manifiesto de aplicación

Para declarar el nivel de ejecución solicitado del juego, agregue una extensión al manifiesto de la aplicación. El siguiente código XML muestra la configuración mínima necesaria para establecer el nivel de ejecución de una aplicación:

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

En el código anterior, se informa al sistema operativo de que el juego solo requiere privilegios de usuario estándar mediante la siguiente etiqueta:

``` syntax
<ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
```

Al establecer de forma explícita el valor de requestedExecutionLevel en "AsInvoker", este ejemplo afirma al sistema operativo que el juego se comportará correctamente sin privilegios administrativos. Como resultado, UAC deshabilita la virtualización y ejecuta el juego con los mismos privilegios que el invocador, que suele tener privilegios de usuario estándar, ya que el explorador de Windows se ejecuta como usuario estándar.

Se puede informar al sistema operativo de que un juego requiere la elevación de privilegios administrativos mediante la sustitución de "AsInvoker" por "requireAdministrator", para crear la siguiente etiqueta:

``` syntax
<ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
```

Con esta configuración, el sistema operativo solicita al usuario actual uno de los cuadros de diálogo de elevación de UAC estándar cada vez que se ejecuta el juego. Se recomienda encarecidamente que ningún juego requiera privilegios de administrador para ejecutarse, porque no solo este cuadro de diálogo se vuelve tan molesto, sino que también hace que el juego no sea compatible con el control parental. Piense muy detenidamente antes de agregar este requisito a cualquier archivo ejecutable.

Una idea equivocada habitual es que agregar un manifiesto que establezca requestedExecutionLevel en "requireAdministrator" omite la necesidad de una solicitud de elevación. Esto no es cierto. Simplemente impide que el sistema operativo adivine si su aplicación de instalación o actualización necesita privilegios administrativos. Todavía se solicita al usuario que autorice la elevación.

Windows comprueba la firma de cualquier aplicación marcada para elevación antes de mostrar el símbolo del sistema de UAC. Un archivo ejecutable grande marcado para elevación tarda más tiempo en comprobarse que un archivo ejecutable pequeño y más largo que un archivo ejecutable marcado como "AsInvoker". Los ejecutables de instalación que se extraen automáticamente deberían estar marcados como "AsInvoker" y cualquier parte que deba marcarse como "requireAdministrator" debe colocarse en un ejecutable auxiliar independiente.

El atributo uiAccess, que se muestra en los ejemplos anteriores, siempre debe ser FALSE para los juegos. Este atributo especifica si los clientes de automatización de la interfaz de usuario tienen acceso a la interfaz de usuario del sistema protegida y tiene implicaciones de seguridad especiales si se establece en TRUE.

## <a name="embedding-a-manifest-in-visual-studio"></a>Incrustar un manifiesto en Visual Studio

La compatibilidad con manifiestos se agregó por primera vez a Visual Studio a partir de VS2005. De forma predeterminada, un archivo ejecutable compilado en Visual Studio 2005 (o posterior) tendrá un manifiesto generado automáticamente incrustado como parte del proceso de compilación. El contenido del manifiesto generado automáticamente depende de ciertas configuraciones de proyecto que se especifiquen en el cuadro de diálogo Propiedades del proyecto.

El manifiesto generado automáticamente por Visual Studio 2005 no contendrá un <trustInfo> bloque, ya que no hay forma de configurar el nivel de ejecución de UAC en las propiedades del proyecto. La mejor manera de agregar esta información es dejar que VS2005 combine un manifiesto definido por el usuario que contenga el <trustInfo> bloque con el manifiesto generado automáticamente. Esto es tan sencillo como agregar un \* archivo. manifest a la solución que contiene el XML que se muestra en la sección anterior. Cuando Visual Studio encuentra un archivo. manifest en la solución, invocará automáticamente la herramienta manifiesto (mt.exe) para combinar los archivos. manifest con el generado automáticamente.

> [!Note]  
> Existe un error en la herramienta de manifiesto (mt.exe) proporcionada por Visual Studio 2005 que genera un manifiesto combinado e incrustado que puede causar problemas cuando el archivo ejecutable se ejecuta en Windows XP anterior a SP3. El error es el resultado de la forma en que la herramienta vuelve a definir el espacio de nombres predeterminado al declarar el <trustInfo> bloque. Afortunadamente, es fácil omitir completamente el problema declarando explícitamente un espacio de nombres diferente en el <trustInfo> bloque y estableciendo el ámbito de los nodos secundarios en el nuevo espacio de nombres. El XML proporcionado en la sección anterior muestra esta corrección.

 

Una advertencia en el uso de la herramienta mt.exe que se incluye en Visual Studio 2005 es que generará una advertencia al procesar el <trustInfo> bloque, ya que la herramienta no contiene un esquema actualizado con el que validar el XML. Para solucionar esta advertencia, se recomienda reemplazar todos los archivos mt.exe en el directorio de instalación de Visual Studio 2005 (hay varias instancias) con las mt.exe proporcionadas en la Windows SDK más reciente.

A partir de Visual Studio 2008, ahora puede especificar el nivel de ejecución de una aplicación desde el cuadro de diálogo Propiedades del proyecto (Figura 3) o mediante la marca del enlazador/MANIFESTUAC. La configuración de estas opciones hará que Visual Studio 2008 genere automáticamente e inserte un manifiesto con el <trustInfo> bloque adecuado en el archivo ejecutable.

**Figura 3. Establecer el nivel de ejecución en Visual Studio 2008**

![establecer el nivel de ejecución en Visual Studio 2008](images/setting-execution-level-in-vs2008.jpg)

Todavía es posible incrustar un manifiesto en versiones anteriores de Visual Studio sin la compatibilidad con el manifiesto, pero requiere más trabajo del desarrollador. Para ver un ejemplo de cómo hacerlo, examine el proyecto de Visual Studio 2003 incluido en cualquier ejemplo del SDK de DirectX antes de la versión de marzo de 2008.

## <a name="uac-compatibility-with-older-games"></a>Compatibilidad de UAC con juegos más antiguos

Si parece que el juego está guardando y cargando un archivo correctamente en el directorio de archivos de programa, pero no hay evidencia de la ión de archivos Windows Vista, cualquier aplicación de 32 bits que no contenga un nivel de ejecución solicitado en su manifiesto se considera una aplicación heredada. Antes de Windows Vista, la mayoría de las aplicaciones se ejecutaban normalmente por usuarios con privilegios administrativos. Como resultado, estas aplicaciones pueden leer y escribir libremente archivos del sistema y claves del registro, y muchos desarrolladores no realizaron los cambios necesarios para funcionar correctamente en cuentas de usuario limitadas en Windows XP. Sin embargo, en Windows Vista, estas mismas aplicaciones no funcionarán correctamente debido a privilegios de acceso insuficientes en el nuevo modelo de seguridad, que aplica la ejecución de usuarios estándar para aplicaciones heredadas. Para mitigar el impacto de esto, la virtualización también se agregó a Windows Vista. La virtualización mantendrá las miles de aplicaciones heredadas que funcionan bien en Windows Vista sin necesidad de que esas aplicaciones tengan privilegios elevados en todo momento, simplemente con el fin de que se realicen correctamente con unas pocas operaciones menores. Si se encuentra, lo más probable es que el juego se esté ejecutando en modo heredado y se haya sometido a la virtualización.

La virtualización afecta al sistema de archivos y al registro redirigiendo las escrituras que distinguen el sistema (y las operaciones posteriores del registro o de archivos) a una ubicación por usuario en el perfil del usuario actual. Por ejemplo, si una aplicación intenta escribir en el siguiente archivo:

<dl> C: \\ archivos de programa nombre de la \\ compañía \\ título \\config.ini  
</dl>

la escritura se redirige automáticamente a:

<dl> C: \\ usuarios \\ nombre de usuario \\ AppData \\ local \\ VirtualStore archivo de programa nombre de la \\ \\ compañía \\ title \\config.ini  
</dl>

Del mismo modo, si una aplicación intenta escribir un valor del registro como el siguiente:

<dl> HKEY \_ local \_ Machine \\ software \\ nombre de la compañía \\ title  
</dl>

en su lugar, se redirigirá a:

<dl> HKEY \_ Current \_ User \\ \\ classes \\ VirtualStore \\ Machine \\ software \\ Company name \\ title  
</dl>

Solo se puede tener acceso a los archivos y las claves del registro afectados por la virtualización mediante operaciones de archivo y registro desde aplicaciones virtualizadas que se ejecutan como el usuario actual.

Sin embargo, hay muchas restricciones en la virtualización. Una es que las aplicaciones de 64 bits nunca se ejecutan en el modo heredado para las operaciones de compatibilidad que se someten a la virtualización en las aplicaciones de 32 bits producirán un error en 64 bits. Además, si una aplicación heredada que se ejecuta como un usuario estándar intenta escribir cualquier tipo de archivo ejecutable en una ubicación que requiera credenciales administrativas, no se realizará la virtualización y se producirá un error en la escritura.

**Figura 4. Proceso de virtualización**

![proceso de virtualización](images/uac-virtualization-process.jpg)

Cuando una aplicación heredada intenta realizar una operación de lectura en ubicaciones sensibles del sistema en el sistema de archivos o en el registro, primero se busca en las ubicaciones virtuales. Si no se encuentra el archivo o la clave del registro, el sistema operativo tiene acceso a las ubicaciones predeterminadas del sistema.

La virtualización se quitará de las versiones posteriores de Windows, por lo que es importante no confiar en esta característica. En su lugar, debe configurar explícitamente el manifiesto de aplicación para los privilegios de usuario estándar o de administrador, ya que esto deshabilitará la virtualización. La virtualización tampoco es obvia para los usuarios finales, por lo que, aunque la virtualización puede permitir que la aplicación se ejecute, puede generar llamadas de soporte técnico y dificultar la toma de problemas para estos clientes.

Tenga en cuenta que si UAC está deshabilitado, la virtualización también está deshabilitada. Si la virtualización está deshabilitada, las cuentas de usuario estándar se comportan exactamente igual que las cuentas de usuario limitadas en Windows XP, y es posible que las aplicaciones heredadas no funcionen correctamente para los usuarios estándar que, de otro modo, se habrían ejecutado correctamente debido

## <a name="legacy-scenarios-and-manifests"></a>Escenarios y manifiestos heredados

Para la mayoría de los escenarios de uso, basta con marcar el archivo. exe con los elementos de manifiesto de UAC correctos y asegurarse de que la aplicación funciona correctamente, ya que un usuario estándar es suficiente para una excelente compatibilidad con UAC. La mayoría de los jugadores ejecutan Windows Vista o Windows 7 con el control de cuentas de usuario habilitado. En Windows XP y los usuarios de Windows Vista o Windows7 con la característica control de cuentas de usuario deshabilitada, normalmente se ejecutan con cuentas de administrador. Aunque se trata de un modo de funcionamiento menos seguro, normalmente no se encontrará en ningún problema de compatibilidad adicional, aunque como se indicó anteriormente, al deshabilitar UAC se deshabilita también la virtualización.

Hay un caso especial que merece la pena tener en cuenta cuando el programa se marca como "requireAdministrator" en el manifiesto de UAC. En Windows XP y en Windows Vista o Windows 7 con el control de cuentas de usuario deshabilitado, el sistema omite los elementos de manifiesto de UAC. En esta situación, los usuarios con cuentas de administrador siempre ejecutarán todos los programas con derechos de administrador completos y, por tanto, estos programas funcionarán según lo previsto. Los usuarios restringidos de Windows XP y los usuarios estándar que se ejecutan en Windows Vista o Windows 7, sin embargo, siempre ejecutarán estos programas con derechos restringidos y se producirá un error en todas las operaciones de nivel de administrador. Por lo tanto, se recomienda que los programas marcados como "requiretAdministrator" llamen a [**IsUserAnAdmin**](/windows/win32/api/shlobj_core/nf-shlobj_core-isuseranadmin) en el inicio y que aparezca un mensaje de error irrecuperable si devuelve false. En el caso anterior, esto siempre se realizará correctamente, pero proporciona una mejor experiencia de usuario y un mensaje de error claro para esta situación excepcional.

## <a name="conclusion"></a>Conclusión

Como desarrollador de juegos dirigido al entorno multiusuario de Windows, es imperativo diseñar su juego para que funcione de forma eficaz y responsable. El archivo ejecutable principal del juego no debe depender de los privilegios administrativos. Esto no solo evita la aparición de mensajes de elevación cada vez que se ejecuta el juego, lo que puede afectar negativamente a la experiencia global del usuario, pero también permite que el juego aproveche otras características que requieren la ejecución con privilegios de usuario estándar, como el control parental.

Las aplicaciones que están diseñadas correctamente para funcionar como con las credenciales de un usuario estándar (o un usuario limitado) en versiones anteriores de Windows no se verán afectadas por UAC y se ejecutarán sin elevación. Sin embargo, deben incluir un manifiesto con el nivel de ejecución solicitado establecido en "AsInvoker" para cumplir con los estándares de aplicación de vista.

## <a name="further-reading"></a>Lecturas adicionales

Para obtener ayuda con el diseño de aplicaciones para Windows Vista que son compatibles con el control de cuentas de usuario, descargue las notas del producto siguientes: [requisitos de desarrollo de aplicaciones de Windows Vista para la compatibilidad con el control de cuentas de usuario](/previous-versions/dotnet/articles/bb530410(v=msdn.10)).

En estas notas del producto se proporcionan pasos detallados sobre el proceso de diseño, junto con ejemplos de código, requisitos y prácticas recomendadas. En este documento también se detallan las actualizaciones técnicas y los cambios en la experiencia del usuario en Windows Vista.

Para obtener más información acerca del control de cuentas de usuario, visite [Windows Vista: control de cuentas de usuario](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) en [Microsoft TechNet](https://www.microsoft.com/technet/).

Otro recurso útil es el artículo [que enseña a las aplicaciones a jugar bien con el control de cuentas de usuario de Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control), desde [MSDN Magazine](/archive/msdn-magazine/msdn-magazine-issues), el 2007 de enero. En este artículo se describen los problemas generales de compatibilidad de aplicaciones, así como las ventajas y los problemas del uso de paquetes de Windows Installer en Windows Vista.

Para obtener más información sobre el error y la corrección de mt.exe, la herramienta usada por Visual Studio 2005 para combinar e incrustar automáticamente un manifiesto en un archivo ejecutable, vea [explorar manifiestos, parte 2: espacios de nombres predeterminados y manifiestos de UAC en Windows Vista](https://techcommunity.microsoft.com/t5/Windows-Blog-Archive/bg-p/Windows-Blog-Archive/2006/09/08/exploring-manifests-part-2-default-namespaces-and-uac-manifests-in-windows-vista/) en el blog de Chris Jackson en [MSDN](/archive/blogs/).

 

