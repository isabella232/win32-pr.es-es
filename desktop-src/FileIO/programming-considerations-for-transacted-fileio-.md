---
description: Describe varias consideraciones de programación para NTFS transaccional.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Consideraciones de programación para NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3150746b1cb34495178cc8318805587f3d08f17e04cb8227e95a9c52ddce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047945"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Consideraciones de programación para NTFS transaccional

Para obtener una descripción de las diversas consideraciones de programación para NTFS transaccional, vea las secciones siguientes:

-   [Qué cambios de archivo se realizan](#which-file-changes-are-transacted)
-   [Compresión](#compression)
-   [Crear un archivo o directorio](#creating-a-file-or-directory)
-   [Eliminar un archivo](#deleting-a-file)
-   [Eliminación de un directorio](#deleting-a-directory)
-   [Problemas de bloqueo de directorios](#directory-locking-issues)
-   [Enumeración de directorios](#directory-enumeration)
-   [Archivos asignados a memoria](#memory-mapped-files)
-   [Flujos con nombre](#named-streams)
-   [Cambiar el nombre de un archivo o directorio](#renaming-a-file-or-directory)
-   [Puntos de análisis](#reparse-points)
-   [Códigos de error](#error-codes)
-   [Sistema de archivos cifrado](#encrypted-file-system)
-   [Funciones de E/S de archivo y NTFS transaccional](#file-io-functions-and-transactional-ntfs)
    -   [Funciones con transacciones](#transacted-functions)
    -   [Funciones de E/S de archivo modificadas por Txf](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Qué cambios de archivo se realizan

La mayoría de los cambios de archivo, como los cambios en el contenido del archivo, las secuencias, los puntos de análisis, los atributos y el espacio de nombres del sistema de archivos, se realizan con transacciones. Cuando se realiza uno de estos cambios en un identificador de archivo de transacción, el cambio se aísla de otras transacciones y el cambio se deshace si se revierte la transacción.

Los cambios que no afectan al contenido del archivo, los metadatos o el espacio de nombres del sistema de archivos, como los cambios en la compresión o la desfragmentación, no se realizan. Estos cambios no están aislados de otras transacciones y no se deshace si se revierte la transacción.

## <a name="compression"></a>Compresión

No se puede cambiar el estado de compresión de un archivo abierto en una transacción.

## <a name="creating-a-file-or-directory"></a>Crear un archivo o directorio

Un archivo o directorio que se crea en una transacción no es visible para nada fuera de la transacción actual. Fuera de esta transacción, cualquier intento de crear un archivo con el mismo nombre produce el error **ERROR \_ TRANSACTIONAL \_ CONFLICT**, reservando eficazmente el nombre de archivo para cuando la transacción se confirma o se revierte.

## <a name="deleting-a-file"></a>Eliminar un archivo

Un archivo o directorio que se elimina mediante una llamada a [**la función DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) permanece visible para todos los lectores externos.

> [!Note]  
> Todos los identificadores de transacción del archivo deben cerrarse antes del final de la transacción. Si los identificadores no están correctamente cerrados, no se produce la eliminación. Todos los identificadores abiertos del archivo deben cerrarse antes de realizar la confirmación para que la operación de eliminación se considere parte de la transacción. Esto se debe a que el sistema no elimina realmente un archivo hasta que se cierra el último identificador de este, incluso cuando no se realiza la transacción de la operación, como parte del subsistema de E/S de archivos de Windows.

 

## <a name="deleting-a-directory"></a>Eliminación de un directorio

Un directorio que se elimina mediante una llamada a [**la función RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) permanece visible para todos los lectores externos.

> [!Note]  
> Existen las mismas restricciones para los identificadores abiertos en las operaciones de directorio con transacciones que en los archivos. Para obtener más información, [vea Eliminar un archivo](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Problemas de bloqueo de directorios

Si un archivo se modifica en una transacción, todos los componentes  de directorio de la ruta de acceso al archivo se conocen como anclados al cambio de nombre hasta que finaliza la transacción. Es decir, el sistema impide cambiar su nombre hasta que se confirma o se revierte la transacción. Un intento de cambiar el nombre de un directorio que es antecesor a un archivo que se ha modificado en una transacción en curso producirá el **error ERROR \_ CANT BREAK \_ \_ TRANSACTIONAL \_ DEPENDENCY**.

## <a name="directory-enumeration"></a>Enumeración de directorios

El contenido de un directorio se puede cambiar mientras una enumeración está en curso como resultado del uso de API que enumeran, por ejemplo, las funciones [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) y [**FindNextFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)

Los cambios en un directorio fuera de una transacción no están aislados de la transacción y son visibles inmediatamente dentro de la transacción. Por ejemplo, si un escritor sin transacciones agrega un archivo a un directorio, el nuevo archivo se ve inmediatamente dentro de la transacción, de modo que al llamar a la función [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) o [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) se devolverá el nuevo archivo.

Los cambios realizados en un directorio dentro de una transacción se aíslan hasta que se confirma la transacción. Por ejemplo, un archivo creado en el directorio como parte de la transacción. Un lector sin transacciones que llame a la función [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) o [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) no verá el archivo recién creado hasta que se confirme la transacción.

## <a name="memory-mapped-files"></a>Archivos asignados a memoria

El cliente debe llamar a la función [**FlushViewOfFile,**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) cerrar el objeto de asignación de archivos y cerrar el identificador de archivo antes de confirmar la transacción asociada en un archivo asignado a memoria.

## <a name="named-streams"></a>Flujos con nombre

Las secuencias con nombre son completamente transaccionales, pero el bloqueo se realiza en el nivel de archivo, no en el nivel de secuencia. Los escritores de fuera de una transacción que intentan modificar cualquier secuencia dentro de un archivo bloqueado reciben el error **ERROR \_ SHARING \_ VIOLATION**.

No se puede cambiar el nombre de una secuencia secundaria en una transacción.

## <a name="renaming-a-file-or-directory"></a>Cambiar el nombre de un archivo o directorio

Para cambiar el nombre de un archivo como una operación de transacción, llame a [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) para mover el archivo.

## <a name="reparse-points"></a>Puntos de análisis

Los cambios en los puntos de análisis se realizan de forma transaccional, lo que significa que si un nuevo punto de análisis se asigna a un archivo de una transacción, no es visible para las demás transacciones. Del mismo modo, los cambios o la eliminación de un punto de reanquiso existente no son visibles hasta la confirmación.

## <a name="error-codes"></a>Códigos de error

Kernel Transaction Manager (KTM) usa los códigos de error del sistema en el intervalo de 6700 a 6799. NTFS transaccional (TxF) usa Windows de error en el intervalo de 6800 a 6899. Para obtener más información, vea WinError.h y Códigos de error del sistema (6000-8199).

## <a name="encrypted-file-system"></a>Sistema de archivos cifrado

TxF no admite operaciones en archivos EFS. No se puede abrir un archivo cifrado con EFS para las transacciones. Al llamar [**a la función CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) en un archivo EFS se producirá el **error ERROR \_ EFS NOT ALLOWED \_ IN \_ \_ \_ TRANSACTION**. De forma similar, al llamar a [**la función EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) en un archivo de una transacción se producirá el **error ERROR \_ EFS NOT ALLOWED IN \_ \_ \_ \_ TRANSACTION**.

## <a name="file-io-functions-and-transactional-ntfs"></a>Funciones de E/S de archivo y NTFS transaccional

TxF proporciona nuevas funciones de transacción que toman un nombre de archivo y cambia el comportamiento de las funciones de API de E/S de archivo existentes que toman un identificador de archivo.

### <a name="transacted-functions"></a>Funciones con transacciones

Si no llama a una de las siguientes funciones de transacción en lugar de su versión sin transacciones, la operación no se realizará:

-   [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**CreateSymbolicLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**FindFirstFileNameTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**FindFirstStreamTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**GetFullPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**GetLongPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Por ejemplo, la [**función CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ahora tiene una versión de transacción: [**CreateFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)

### <a name="file-io-functions-changed-by-txf"></a>Funciones de E/S de archivo modificadas por Txf

En la tabla siguiente se enumeran las funciones cuyo comportamiento se ve afectado por NTFS transaccional. Por ejemplo, el comportamiento de la función [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) variará en función de si la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) o [**la función CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) crearon el parámetro *hFile.*



| Función                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Las aplicaciones deben cerrar todos los identificadores enlazados a una transacción antes de que se confirma la transacción. Una aplicación debe cerrar un identificador de transacción abierto con **FILE FLAG DELETE ON \_ \_ \_ \_ CLOSE** antes de confirmar la transacción para que se produzca la operación de eliminación.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Si hay una transacción asociada a *hFile*, el objeto de asignación de archivos que crea esta función se asociará a la misma transacción. Se realizan transacciones de las modificaciones realizadas a través de vistas de este objeto de asignación de archivos. Las aplicaciones deben llamar [**a FlushViewOfFile,**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile)desa asignar todas las vistas y cerrar todos los identificadores al objeto de asignación de archivos antes de confirmar los cambios de transacción.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Si hay una transacción enlazada al identificador de enumeración de archivos, los archivos que se devuelven están sujetos a reglas de aislamiento de transacciones.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | No se puede cambiar el estado de compresión de un archivo abierto [**por CreateFileTransacted.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) y [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Si hay una transacción enlazada al identificador de archivo, la función devuelve información para la vista de archivo aislado.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize y**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Si hay una transacción enlazada al identificador de archivo, la función devuelve información para la vista de archivo aislado.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Si el volumen admite transacciones del sistema de archivos, la función devuelve **FILE \_ SUPPORTS \_ TRANSACTIONS** en *lpFileSystemFlags*.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile y**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Si hay una transacción asociada al identificador de archivo utilizado para crear el objeto de asignación de archivos que se está asignando, se realiza la transacción de la vista asociada. Si la vista se usa para realizar cambios de transacción en un archivo, el usuario debe llamar a [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), cerrar el objeto de asignación de archivos y cerrar el identificador de archivo antes de confirmar la transacción asociada.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Si hay una transacción enlazada al identificador de directorio, las notificaciones reflejan la vista aislada del directorio. Los cambios en los archivos fuera de la vista con transacciones del directorio no se incluyen en las notificaciones.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile,**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)y [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | Si hay una transacción enlazada al identificador de archivo, la función devuelve datos de la vista con transacciones del archivo. Se garantiza que un identificador de lectura con transacciones muestre la misma vista de un archivo mientras dure el identificador.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Si hay una transacción enlazada al identificador, se realiza la transacción del cambio en la posición de fin de archivo.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Si hay una transacción enlazada al identificador, los cambios realizados se realizarán para las clases de información **FileBasicInfo**, **FileRenameInfo,** **FileAllocationInfo,** **FileEndOfFileInfo** y **FileDispositionInfo**.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Si hay una transacción enlazada al identificador, se realiza la transacción del cambio en el nombre corto del archivo.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Si hay una transacción enlazada al identificador, se realiza la transacción del cambio en el tiempo del archivo.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile,**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)y [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Si hay una transacción enlazada al identificador de archivo, se realiza la transacción de la escritura del archivo.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

