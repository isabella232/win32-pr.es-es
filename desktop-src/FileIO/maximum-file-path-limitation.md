---
description: Límite máximo de longitud de ruta de acceso.
title: Límite máximo de longitud de ruta de acceso
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: 995cd6d973a5bab02deae3068e39e8e3f3d51f40
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "104279841"
---
# <a name="maximum-path-length-limitation"></a>Límite máximo de longitud de ruta de acceso

En la API de Windows (con algunas excepciones que se describen en los párrafos siguientes), la longitud máxima de una ruta de acceso es **Max \_ path**, que se define como 260 caracteres. Una ruta de acceso local está estructurada en el orden siguiente: letra de unidad, dos puntos, barra diagonal inversa, componentes de nombre separados por barras diagonales inversas y un carácter nulo de terminación. Por ejemplo, la ruta de acceso máxima de la unidad D es "D: \\ *some cadena de ruta de acceso de caracteres de 256* &lt; &gt; " donde " &lt; NUL &gt; " representa el carácter nulo de finalización invisible de la página de códigos del sistema actual. (Los caracteres < > se usan aquí para la claridad visual y no pueden formar parte de una cadena de ruta de acceso válida).

Por ejemplo, puede alcanzar esta limitación si va a clonar un repositorio de Git que tiene nombres de archivo largos en una carpeta que tiene un nombre largo.


> [!Note]  
> Las funciones de e/s de archivo de la API de Windows convierten "/" en " \\ " como parte de la conversión del nombre a un nombre de estilo NT, excepto cuando se usa el \\ \\ \\ prefijo "?", tal y como se detalla en las secciones siguientes.

La API de Windows tiene muchas funciones que también tienen versiones Unicode para permitir una ruta de acceso de longitud extendida para una longitud de ruta de acceso total máxima de 32.767 caracteres. Este tipo de ruta de acceso se compone de componentes separados por barras diagonales inversas, cada uno de ellos hasta el valor devuelto en el parámetro *lpMaximumComponentLength* de la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (este valor suele ser de 255 caracteres). Para especificar una ruta de acceso de longitud extendida, use el \\ \\ \\ prefijo "?". Por ejemplo, " \\ \\ ? \\ D: \\ *ruta de acceso muy larga*".

> [!Note]  
> La ruta de acceso máxima de 32.767 caracteres es aproximada, ya \\ \\ \\ que el prefijo "?" puede expandirse hasta una cadena más larga por el sistema en tiempo de ejecución, y esta expansión se aplica a la longitud total.

El \\ \\ \\ prefijo "?" también se puede usar con rutas de acceso construidas según la Convención de nomenclatura universal (UNC). Para especificar esta ruta de acceso mediante UNC, use el \\ \\ \\ Prefijo UNC \\ . Por ejemplo, " \\ \\ ? \\ \\ \\ Recurso compartido de servidor UNC ", donde" servidor "es el nombre del equipo y" recurso compartido "es el nombre de la carpeta compartida. Estos prefijos no se utilizan como parte de la propia ruta de acceso. Indican que la ruta de acceso debe pasarse al sistema con una modificación mínima, lo que significa que no se pueden usar barras diagonales para representar separadores de ruta de acceso o un punto para representar el directorio actual, o puntos dobles para representar el directorio primario. Dado que no puede usar el \\ \\ \\ prefijo "?" con una ruta de acceso relativa, las rutas de acceso relativas siempre están limitadas a un total de caracteres de **ruta de \_ acceso máxima** .

No es necesario realizar ninguna normalización Unicode en las cadenas de nombre de archivo y ruta de acceso para su uso por parte de las funciones de la API de e/s de archivos de Windows, ya que el sistema de archivos trata los nombres de archivo y ruta de acceso como una secuencia opaca de **WCHAR** s. Cualquier normalización que requiera la aplicación debe realizarse teniendo esto en cuenta, externa de cualquier llamada a las funciones de la API de e/s de archivos de Windows relacionadas.

Cuando se usa una API para crear un directorio, la ruta de acceso especificada no puede ser tan larga que no se puede anexar un nombre de archivo 8,3 (es decir, el nombre de directorio no puede superar la **\_ ruta de acceso máxima** menos 12).

El Shell y el sistema de archivos tienen requisitos diferentes. Es posible crear una ruta de acceso con la API de Windows que la interfaz de usuario de Shell no pueda interpretar correctamente.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Habilitar rutas de acceso largas en Windows 10, versión 1607 y versiones posteriores

A partir de Windows 10, versión 1607, se han quitado las limitaciones de **\_ ruta de acceso máximas** de las funciones comunes de archivos y directorios de Win32. Sin embargo, debe participar en el nuevo comportamiento.

Para habilitar el nuevo comportamiento de la ruta de acceso larga, deben cumplirse las dos condiciones siguientes:

* La clave del registro `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` debe existir y establecerse en 1. El valor de la clave se almacenará en la memoria caché del sistema (por proceso) después de la primera llamada a una función de directorio o archivo Win32 afectada (consulte a continuación la lista de funciones). La clave del registro no se recargará durante la vigencia del proceso. Para que todas las aplicaciones del sistema reconozcan el valor de la clave, puede ser necesario reiniciar porque es posible que se hayan iniciado algunos procesos antes de que se haya establecido la clave.

También puede copiar este código en un `.reg` archivo que puede establecerlo automáticamente:
```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

    > [!NOTE]  
    > This registry key can also be controlled via Group Policy at `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths`.

* El [manifiesto de aplicación](../sbscs/application-manifests.md) también debe incluir el `longPathAware` elemento.

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Estas son las funciones de administración de directorios que ya no tienen restricciones de **\_ ruta de acceso máximas** si participa en el comportamiento de la ruta de acceso larga: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Estas son las funciones de administración de archivos que ya no tienen restricciones de **\_ ruta de acceso máximas** si participa en el comportamiento de ruta larga: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW.
