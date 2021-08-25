---
Description: Los atributos de archivo son valores de metadatos almacenados por el sistema de archivos en disco y los usa el sistema y están disponibles para los desarrolladores a través de varias API de E/S de archivos.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Constantes de atributo de archivo (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: 1dbb3d8e5eb091c47635f78eba9558a0d2262caeb5ce482c7b5bccdc3b237169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050875"
---
# <a name="file-attribute-constants"></a>Constantes de atributo de archivo

Los atributos de archivo son valores de metadatos almacenados por el sistema de archivos en disco y los usa el sistema y están disponibles para los desarrolladores a través de varias API de E/S de archivos. Para obtener una lista de api y temas relacionados, consulte la sección También.

## <a name="example"></a>Ejemplo
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

Ejemplo tomado de un ejemplo [Windows clásico en](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) GitHub.



| Constante o valor                                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**FILE \_ ARCHIVO \_ DE ATRIBUTOS**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Un archivo o directorio que es un archivo o directorio de archivo. Normalmente, las aplicaciones usan este atributo para marcar los archivos de copia de seguridad o eliminación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ COMPRESSED**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Un archivo o directorio comprimido. Para un archivo, se comprimen todos los datos del archivo. Para un directorio, la compresión es el valor predeterminado para los archivos y subdirectorios recién creados.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**FILE \_ DISPOSITIVO \_ DE ATRIBUTO**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Este valor está reservado para uso del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**FILE \_ DIRECTORIO \_ DE ATRIBUTO**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Identificador que identifica un directorio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ ENCRYPTED**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Un archivo o directorio cifrado. Para un archivo, se cifran todos los flujos de datos del archivo. Para un directorio, el cifrado es el valor predeterminado para los archivos y subdirectorios recién creados.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ HIDDEN**</dt> <dt>2 (0x2)</dt> </dl>                                                            | El archivo o directorio está oculto. No se incluye en una lista de directorios normal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**FILE \_ FLUJO \_ DE \_ INTEGRIDAD DE**</dt> ATRIBUTOS <dt>32768 (0x8000)</dt> </dl>                      | El flujo de datos de directorio o usuario se configura con integridad (solo se admite en volúmenes ReFS). No se incluye en una lista de directorios normal. La configuración de integridad se conserva con el archivo si se cambia el nombre. Si se copia un archivo, el archivo de destino tendrá la integridad establecida si el archivo de origen o el directorio de destino tienen establecida la integridad.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca no se admite hasta Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Archivo que no tiene otros atributos establecidos. Este atributo solo es válido cuando se usa por sí solo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED**</dt> <dt>8192 (0x2000)</dt> </dl>             | El servicio de indexación de contenido no indexa el archivo o directorio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NO \_ SCRUB \_ DATA**</dt> <dt>131072 (0x20000)</dt> </dl>                            | El flujo de datos de usuario no se leerá mediante el escáner de integridad de datos en segundo plano (también conocido como limpieza). Cuando se establece en un directorio, solo proporciona herencia. Esta marca solo se admite en volúmenes Espacios de almacenamiento y ReFS. No se incluye en una lista de directorios normal.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca no se admite hasta Windows 8 y Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Los datos de un archivo no están disponibles inmediatamente. Este atributo indica que los datos de archivo se mueven físicamente al almacenamiento sin conexión. Este atributo lo usa Remote Storage, que es el software de administración de almacenamiento jerárquico. Las aplicaciones no deben cambiar arbitrariamente este atributo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ READONLY**</dt> <dt>1 (0x1)</dt> </dl>                                                      | Un archivo que es de solo lectura. Las aplicaciones pueden leer el archivo, pero no escribir en él ni eliminarlo. Este atributo no se respeta en los directorios. Para obtener más información, vea No se pueden ver ni cambiar los atributos de solo lectura o sistema de carpetas en [Windows Server 2003, en Windows XP, en Windows Vista](https://support.microsoft.com/kb/326549)o en Windows 7 .<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**FILE \_ RECUPERACIÓN \_ DE ATRIBUTOS EN EL ACCESO \_ \_ \_ 4194304**</dt> <dt>DATOS (0x400000)</dt> </dl> | Cuando se establece este atributo, significa que el archivo o directorio no está totalmente presente localmente. Para un archivo que significa que no todos sus datos están en almacenamiento local (por ejemplo, pueden estar dispersos con algunos datos todavía en el almacenamiento remoto). Para un directorio, significa que parte del contenido del directorio se virtualiza desde otra ubicación. Leer el archivo o enumerar el directorio será más costoso de lo normal; por ejemplo, hará que al menos parte del contenido del archivo o directorio se obtenga de un almacén remoto. Solo los llamadores en modo kernel pueden establecer este bit.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**FILE \_ RECUPERACIÓN \_ DE \_ ATRIBUTOS EN \_ 262144**</dt> <dt>ABIERTO (0x40000)</dt> </dl>                         | Este atributo solo aparece en las clases de enumeración de directorios (FILE \_ DIRECTORY \_ INFORMATION, FILE \_ BOTH DIR \_ \_ INFORMATION, etc.). Cuando se establece este atributo, significa que el archivo o directorio no tiene ninguna representación física en el sistema local; el elemento es virtual. Abrir el elemento será más costoso de lo normal, por ejemplo, hará que al menos parte de él se obtenga de un almacén remoto.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ REPARSE \_ POINT**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Un archivo o directorio que tiene un punto de reanción asociado o un archivo que es un vínculo simbólico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**FILE \_ ARCHIVO \_ DISPERSO \_ DE ATRIBUTOS**</dt> <dt>512 (0x200)</dt> </dl>                                        | Un archivo que es un archivo disperso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**FILE \_ SISTEMA \_ DE ATRIBUTOS**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Un archivo o directorio del que el sistema operativo usa una parte o que usa exclusivamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ TEMPORARY**</dt> <dt>256 (0x100)</dt> </dl>                                               | Archivo que se usa para el almacenamiento temporal. Los sistemas de archivos evitan la escritura de datos en el almacenamiento masivo si hay suficiente memoria caché disponible, ya que, normalmente, una aplicación elimina un archivo temporal después de cerrar el identificador. En ese escenario, el sistema puede evitar completamente escribir los datos. De lo contrario, los datos se escriben después de cerrar el identificador.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Este valor está reservado para uso del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributo de compresión](compression-attribute.md)
</dt> <dt>

[Crear y abrir archivos](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




