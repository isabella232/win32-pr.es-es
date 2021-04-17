---
Description: Los atributos de archivo son valores de metadatos almacenados por el sistema de archivos en el disco y son utilizados por el sistema y están disponibles para los desarrolladores a través de varias API de e/s de archivos.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Constantes de atributo de archivo (Winnt. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: eae376462ae6c633be96e4434fbb782fa41c802f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670355"
---
# <a name="file-attribute-constants"></a>Constantes de atributo de archivo

Los atributos de archivo son valores de metadatos almacenados por el sistema de archivos en el disco y son utilizados por el sistema y están disponibles para los desarrolladores a través de varias API de e/s de archivos. Para obtener una lista de las API y los temas relacionados, consulte la sección Vea también.

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

Ejemplo tomado de un [ejemplo clásico de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) en github.



| Constante o valor                                                                                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**Archivo \_ de \_Archivo de atributos**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Archivo o directorio que es un archivo o directorio de almacenamiento. Normalmente, las aplicaciones usan este atributo para marcar los archivos para la copia de seguridad o la eliminación. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ comprimido**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Archivo o directorio comprimido. En el caso de un archivo, se comprimen todos los datos del archivo. Para un directorio, la compresión es el valor predeterminado para los archivos y subdirectorios recién creados.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**Archivo \_ de \_Dispositivo de atributo**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Este valor está reservado para uso del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**Archivo \_ de \_Directorio de atributos**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Identificador que identifica un directorio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ cifrado**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Archivo o directorio cifrado. Para un archivo, se cifran todas las secuencias de datos del archivo. Para un directorio, el cifrado es el valor predeterminado para los archivos y subdirectorios recién creados.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ oculto**</dt> <dt>2 (0X2)</dt> </dl>                                                            | El archivo o directorio está oculto. No se incluye en una lista de directorios normal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**Archivo \_ de \_ \_ Secuencia de integridad de atributo**</dt> <dt>32768 (0x8000)</dt> </dl>                      | El flujo de datos de usuario o directorio se configura con integridad (solo se admite en volúmenes ReFS). No se incluye en una lista de directorios normal. La configuración de integridad se conserva con el archivo si se cambia el nombre. Si se copia un archivo, el archivo de destino tendrá la integridad establecida si el archivo de origen o el directorio de destino tienen la integridad establecida.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca no se admite hasta Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Archivo que no tiene ningún otro conjunto de atributos. Este atributo solo es válido cuando se usa por sí solo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ no \_ \_ indizado de contenido**</dt> <dt>8192 (0x2000)</dt> </dl>             | El servicio de indización de contenido no va a indizar el archivo o directorio.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**Archivo \_ de \_No hay \_ \_ datos de limpieza de atributo**</dt> <dt>131072 (0x20000)</dt> </dl>                            | El flujo de datos de usuario que no leerá el escáner de integridad de datos en segundo plano (también conocido como limpiador). Cuando se establece en un directorio, solo proporciona herencia. Esta marca solo se admite en los espacios de almacenamiento y los volúmenes ReFS. No se incluye en una lista de directorios normal.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Esta marca no se admite hasta Windows 8 y Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ sin conexión**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Los datos de un archivo no están disponibles de inmediato. Este atributo indica que los datos del archivo se mueven físicamente al almacenamiento sin conexión. Este atributo lo usa el almacenamiento remoto, que es el software de administración de almacenamiento jerárquico. Las aplicaciones no deben cambiar arbitrariamente este atributo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**Archivo \_ de ATRIBUTO de \_ solo lectura**</dt> <dt>1 (0x1)</dt> </dl>                                                      | Un archivo que es de solo lectura. Las aplicaciones pueden leer el archivo, pero no pueden escribir en él ni eliminarlo. Este atributo no se respeta en los directorios. Para obtener más información, consulte [no puede ver ni cambiar los atributos de solo lectura o sistema de las carpetas en Windows Server 2003, en Windows XP, en Windows Vista o en Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**Archivo \_ de \_Recuperación \_ de atributos en el \_ \_ acceso a datos**</dt> <dt>4194304 (0x400000)</dt> </dl> | Cuando se establece este atributo, significa que el archivo o directorio no está totalmente presente de forma local. Para un archivo que significa que no todos sus datos están en el almacenamiento local (por ejemplo, puede que esté disperso con algunos datos que todavía están en el almacenamiento remoto). Para un directorio, significa que parte del contenido del directorio se virtualiza desde otra ubicación. Leer el archivo o enumerar el directorio será más caro de lo normal; por ejemplo, hará que se capture al menos parte del contenido del archivo o directorio desde un almacén remoto. Solo los llamadores de modo kernel pueden establecer este bit.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**Archivo \_ de \_Recuperación \_ de atributos en \_ Open**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Este atributo solo aparece en las clases de enumeración de directorio (información del directorio de archivos \_ \_ , archivo \_ ambos \_ \_ datos, etc.). Cuando se establece este atributo, significa que el archivo o directorio no tiene ninguna representación física en el sistema local; el elemento es virtual. Abrir el elemento será más caro de lo normal; por ejemplo, hará que se capture al menos parte de él desde un almacén remoto.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**Archivo \_ de \_ \_ Punto de reanálisis de atributo**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Archivo o directorio que tiene un punto de análisis asociado o un archivo que es un vínculo simbólico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**Archivo \_ de \_ \_ Archivo disperso de atributo**</dt> <dt>512 (0x200)</dt> </dl>                                        | Archivo que es un archivo disperso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ System**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Archivo o directorio del que el sistema operativo utiliza parte o que usa exclusivamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ temporal**</dt> <dt>256 (0x100)</dt> </dl>                                               | Archivo que se usa para el almacenamiento temporal. Los sistemas de archivos evitan la escritura de datos en el almacenamiento masivo si hay suficiente memoria caché, ya que, por lo general, una aplicación elimina un archivo temporal después de cerrar el controlador. En ese escenario, el sistema puede evitar completamente la escritura de los datos. De lo contrario, los datos se escriben después de cerrarse el identificador.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**Archivo \_ de ATRIBUTO \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Este valor está reservado para uso del sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributo Compression](compression-attribute.md)
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

 

 




