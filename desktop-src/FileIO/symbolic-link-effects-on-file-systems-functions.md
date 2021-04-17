---
description: Cómo afectan los vínculos simbólicos a las funciones de archivo estándar que usan nombres de ruta de acceso para especificar uno o varios archivos.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Efectos simbólicos de los vínculos en las funciones del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668370"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Efectos simbólicos de los vínculos en las funciones del sistema de archivos

Varias funciones de archivo estándar que utilizan nombres de ruta de acceso para especificar uno o varios archivos se ven afectadas por el uso de vínculos simbólicos. En este tema se enumeran las funciones y se describen los cambios de comportamiento:

-   [CopyFile y CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile y CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink y CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile y DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile y FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [GetBinaryType](#getbinarytype)
-   [GetCompressedFileSize y GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [GetDiskFreeSpaceEx](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [Temas relacionados](#related-topics)

En las siguientes descripciones, se usan los términos siguientes:

-   Archivo de origen: el archivo original que se va a copiar.
-   Archivo de destino: la copia recién creada del archivo.
-   Destino: la entidad a la que apunta un vínculo simbólico.

> [!Note]  
> El comportamiento de las funciones que aceptan un identificador creado con la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , como la función [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , variará en función de si se llamó a la función **CreateFile** mediante la marca de **\_ \_ \_ \_ punto de reanálisis de la marca de archivo abierta** . Para obtener más información, vea [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y la siguiente sección de [CreateFile y CreateFileTransacted](#createfile-and-createfiletransacted) .

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile y CopyFileTransacted

Si el archivo de origen es un vínculo simbólico, el archivo que se ha copiado es el destino del vínculo simbólico.

Si el archivo de destino ya existe y es un vínculo simbólico, el archivo de código fuente sobrescribe el vínculo simbólico.

## <a name="copyfileex"></a>CopyFileEx

Si se especifica **Copy \_ file \_ Copy \_ SYMLINK** y:

-   Si el archivo de origen es un vínculo simbólico, se copia el vínculo simbólico, no el archivo de destino.
-   Si el archivo de origen no es un vínculo simbólico, no hay ningún cambio en el comportamiento.
-   Si el archivo de destino es un vínculo simbólico existente, se sobrescribe el vínculo simbólico, no el archivo de destino.
-   Si también se especifica la operación de **copia de \_ archivo \_ \_ si \_ existe** y el archivo de destino es un vínculo simbólico existente, se produce un error en la operación en todos los casos.

Si no se especifica **Copy \_ file \_ Copy \_ SYMLINK** y:

-   Si también se especifica la operación de **copia de \_ archivo \_ \_ si \_ existe** , y el archivo de destino es un vínculo simbólico existente, se produce un error en la operación solo si existe el destino del vínculo simbólico.
-   Si no se especifica **Copy File si no se especifica \_ \_ \_ \_ EXISTS** , no se produce ningún cambio en el comportamiento.

**Windows Server 2003 y Windows XP:** No se admite la marca de **\_ \_ \_ SYMLINK copiar archivo** . Si el archivo de origen es un vínculo simbólico, el archivo que se ha copiado es el destino del vínculo simbólico.

## <a name="createfile-and-createfiletransacted"></a>CreateFile y CreateFileTransacted

Si la llamada a esta función crea un nuevo archivo, no hay ningún cambio en el comportamiento.

Si se especifica el **marcador de archivo, abra el \_ \_ \_ \_ punto de reanálisis** y:

-   Si se abre un archivo existente y es un vínculo simbólico, el identificador devuelto es un identificador del vínculo simbólico.
-   Si **crear \_ siempre**, **truncar \_ existente** o **\_ \_ Borrar marca de archivo \_ al \_ cerrar** se especifican, el archivo afectado es un vínculo simbólico.

Si no se especifica el **marcador de archivo, abra el \_ \_ \_ \_ punto de reanálisis** y:

-   Si se abre un archivo existente y es un vínculo simbólico, el identificador devuelto es un identificador del destino.
-   Si **crear \_ siempre**, **truncar \_ existente** o **\_ \_ Borrar marca de archivo \_ al \_ cerrar** se especifican, el archivo afectado es el destino.

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink y CreateHardLinkTransacted

Si la ruta de acceso apunta a un vínculo simbólico, la función crea un vínculo físico al destino.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile y DeleteFileTransacted

Si la ruta de acceso apunta a un vínculo simbólico, se elimina el vínculo simbólico, no el destino. Para eliminar un destino, debe llamar a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y especificar **el \_ marcador \_ de archivo eliminar \_ al \_ cerrar**.

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Si la ruta de acceso apunta a un vínculo simbólico, se crea el identificador de notificación para el destino. Si una aplicación se ha registrado para recibir notificaciones de cambio para un directorio que contiene vínculos simbólicos, solo se notificará a la aplicación cuando se hayan cambiado los vínculos simbólicos, no los archivos de destino.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile y FindFirstFileTransacted

Si la ruta de acceso apunta a un vínculo simbólico, el búfer de [**\_ \_ búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene información sobre el vínculo simbólico, no el destino.

## <a name="findfirstfileex"></a>FindFirstFileEx

Si la ruta de acceso apunta a un vínculo simbólico, el búfer de [**\_ \_ búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene información sobre el vínculo simbólico, no el destino.

## <a name="findnextfile"></a>FindNextFile

Si la ruta de acceso apunta a un vínculo simbólico, el búfer de [**\_ \_ búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene información sobre el vínculo simbólico, no el destino.

## <a name="getbinarytype"></a>GetBinaryType

Si la ruta de acceso apunta a un vínculo simbólico, se utiliza el archivo de destino.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize y GetCompressedFileSizeTransacted

Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve el tamaño del archivo de destino.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Si la ruta de acceso apunta a un vínculo simbólico, la operación se realiza en el destino.

## <a name="getdiskfreespaceex"></a>GetDiskFreeSpaceEx

Si la ruta de acceso apunta a un vínculo simbólico, la operación se realiza en el destino.

## <a name="getfileattributes"></a>GetFileAttributes

Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.

## <a name="getfileattributesex"></a>GetFileAttributesEx

Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.

## <a name="getfilesecurity"></a>GetFileSecurity

Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.

## <a name="gettemppath"></a>GetTempPath

Si la ruta de acceso apunta a un vínculo simbólico, el nombre de la ruta de acceso temporal mantiene los vínculos simbólicos.

## <a name="getvolumeinformation"></a>GetVolumeInformation

Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve información del volumen para el destino.

## <a name="setfileattributes"></a>SetFileAttributes

Si la ruta de acceso apunta a un vínculo simbólico, la función recupera atributos para el vínculo simbólico.

## <a name="setfilesecurity"></a>SetFileSecurity

Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**GetBinaryType**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
