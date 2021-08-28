---
description: Limitación de longitud máxima de la ruta de acceso.
title: Limitación de longitud máxima de la ruta de acceso
ms.topic: article
ms.custom: contperf-fy21q1
ms.date: 09/15/2020
ms.openlocfilehash: f57aba8d022e3b193289c8abf884e661797a0cf8585b7537fae19c171250eb12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914765"
---
# <a name="maximum-path-length-limitation"></a>Limitación de longitud máxima de la ruta de acceso

En la API Windows (con algunas excepciones analizadas en los párrafos siguientes), la longitud máxima de una ruta de acceso es **MAX \_ PATH,** que se define como 260 caracteres. Una ruta de acceso local se estructura en el orden siguiente: letra de unidad, dos puntos, barra diagonal inversa, componentes de nombre separados por barras diagonales inversas y un carácter nulo de terminación. Por ejemplo, la ruta de acceso máxima en la unidad D es "D: una cadena de ruta de acceso de \\ *256* caracteres &lt; NUL" donde &gt; &lt; "NUL" representa el carácter nulo de terminación invisible para la página de códigos del sistema &gt; actual. (Los caracteres < > se usan aquí para mayor claridad visual y no pueden formar parte de una cadena de ruta de acceso válida).

Por ejemplo, puede alcanzar esta limitación si está clonando un repositorio de Git que tiene nombres de archivo largos en una carpeta que a su vez tiene un nombre largo.


> [!Note]  
> Las funciones de E/S de archivos de la API de Windows convierten "/" en " " como parte de la conversión del nombre en un nombre de estilo NT, excepto cuando se usa el prefijo " ? " como se detalla en las secciones \\ \\ \\ \\ siguientes.

La API Windows tiene muchas funciones que también tienen versiones Unicode para permitir una ruta de acceso de longitud extendida para una longitud total máxima de ruta de acceso de 32 767 caracteres. Este tipo de ruta de acceso se compone de componentes separados por barras diagonales inversas, cada uno hasta el valor devuelto en el parámetro *lpMaximumComponentLength* de la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) (este valor normalmente tiene 255 caracteres). Para especificar una ruta de acceso de longitud extendida, use el prefijo " \\ \\ ? \\ ". Por ejemplo, " \\ \\ ? \\ D: \\ *ruta de acceso muy larga*".

> [!Note]  
> La ruta de acceso máxima de 32 767 caracteres es aproximada, porque el sistema puede expandir el prefijo " ? " a una cadena más larga en tiempo de ejecución y esta expansión se aplica a la \\ \\ \\ longitud total.

El prefijo " ? " también se puede usar con rutas de acceso construidas según \\ \\ la convención de nomenclatura \\ universal (UNC). Para especificar dicha ruta de acceso mediante UNC, use " \\ \\ ? \\ Prefijo UNC \\ ". Por ejemplo, " \\ \\ ? \\ Recurso compartido de servidor UNC", donde "servidor" es el nombre del equipo y \\ \\ "recurso compartido" es el nombre de la carpeta compartida. Estos prefijos no se usan como parte de la propia ruta de acceso. Indican que la ruta de acceso se debe pasar al sistema con una modificación mínima, lo que significa que no se pueden usar barras diagonales para representar separadores de ruta de acceso, un punto para representar el directorio actual o puntos dobles para representar el directorio primario. Dado que no se puede usar el prefijo " ? " con una ruta de acceso relativa, las rutas de acceso relativas siempre se limitan \\ \\ a un total de caracteres \\ MAX **\_ PATH.**

No es necesario realizar ninguna normalización Unicode en las cadenas de ruta de acceso y nombre de archivo para su uso por parte de las funciones de api de E/S de archivo de Windows porque el sistema de archivos trata los nombres de ruta de acceso y de archivo como una secuencia opaca de **WCHAR.** Cualquier normalización que requiera la aplicación debe realizarse con esto en mente, fuera de las llamadas a las funciones Windows API de E/S de archivos relacionados.

Cuando se usa una API para crear un directorio, la ruta de acceso especificada no puede ser tan larga que no se pueda anexar un nombre de archivo 8.3 (es decir, el nombre del directorio no puede superar **MAX \_ PATH** menos 12).

El shell y el sistema de archivos tienen requisitos diferentes. Es posible crear una ruta de acceso con la API Windows que la interfaz de usuario del shell no puede interpretar correctamente.

## <a name="enable-long-paths-in-windows-10-version-1607-and-later"></a>Habilitar rutas de acceso largas Windows 10, versión 1607 y posteriores

A partir Windows 10, versión 1607, se han quitado las limitaciones de **\_ MAX PATH** de las funciones comunes de archivos y directorios win32. Sin embargo, debe participar en el nuevo comportamiento.

Para habilitar el nuevo comportamiento de ruta de acceso larga, deben cumplirse las dos condiciones siguientes:

* La clave del `Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem\LongPathsEnabled (Type: REG_DWORD)` Registro debe existir y establecerse en 1. El sistema almacenará en caché el valor de la clave (por proceso) después de la primera llamada a una función de directorio o archivo Win32 afectada (consulte a continuación la lista de funciones). La clave del Registro no se volverá a cargar durante la vigencia del proceso. Para que todas las aplicaciones del sistema reconozcan el valor de la clave, es posible que sea necesario reiniciar porque es posible que algunos procesos se hubieran iniciado antes de establecer la clave.

También puede copiar este código en un archivo que pueda establecerlo por usted o usar el comando de PowerShell desde una ventana `.reg` de terminal con privilegios elevados:
# <a name="cmd"></a>[cmd](#tab/cmd)

```cmd
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem]
"LongPathsEnabled"=dword:00000001

```

# <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
New-ItemProperty -Path "HKLM:\SYSTEM\CurrentControlSet\Control\FileSystem" `
-Name "LongPathsEnabled" -Value 1 -PropertyType DWORD -Force

```

---

> [!NOTE]  
> Esta clave del Registro también se puede controlar mediante directiva de grupo en `Computer Configuration > Administrative Templates > System > Filesystem > Enable Win32 long paths` .

* El [manifiesto de aplicación](../sbscs/application-manifests.md) también debe incluir el elemento `longPathAware` .

    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
            <ws2:longPathAware>true</ws2:longPathAware>
        </windowsSettings>
    </application>
    ```

Estas son las funciones de administración de directorios que ya no tienen restricciones **de MAX \_ PATH** si opta por el comportamiento de ruta de acceso larga: CreateDirectoryW, CreateDirectoryExW GetCurrentDirectoryW RemoveDirectoryW SetCurrentDirectoryW.

Estas son las funciones de administración de archivos que ya no tienen restricciones **MAX \_ PATH** si opta por el comportamiento de ruta de acceso larga: CopyFileW, CopyFile2, CopyFileExW, CreateFileW, CreateFile2, CreateHardLinkW, CreateSymbolicLinkW, DeleteFileW, FindFirstFileW, FindFirstFileExW, FindNextFileW, GetFileAttributesW, GetFileAttributesExW, SetFileAttributesW, GetFullPathNameW, GetLongPathNameW, MoveFileW, MoveFileExW, MoveFileWithProgressW, ReplaceFileW, SearchPathW, FindFirstFileNameW, FindNextFileNameW, FindFirstStreamW, FindNextStreamW, GetCompressedFileSizeW, GetFinalPathNameByHandleW.
