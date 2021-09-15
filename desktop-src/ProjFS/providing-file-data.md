---
title: Aprovisionamiento de datos de archivo
description: Describe cómo un proveedor proporciona información de marcador de posición y datos de archivo.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/01/2018
ms.topic: article
ms.openlocfilehash: 341a0f1c477b605b2a437edf311c380910744ac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473636"
---
# <a name="providing-file-data"></a>Aprovisionamiento de datos de archivo

Cuando un proveedor crea por primera vez una raíz de virtualización, está vacío en el sistema local. Es decir, ninguno de los elementos del almacén de datos de respaldo todavía se ha almacenado en caché en el disco. A medida que se abren los elementos, ProjFS solicita información al proveedor para permitir que los marcadores de posición de esos elementos se puedan crear en el sistema de archivos local.  A medida que se accede al contenido del elemento, ProjFS solicita ese contenido al proveedor.  El resultado es que, desde la perspectiva del usuario, los archivos y directorios virtualizados son similares a los archivos y directorios normales que ya residen en el sistema de archivos local.

## <a name="placeholder-creation"></a>Creación de marcadores de posición

Cuando una aplicación intenta abrir un identificador en un archivo virtualizado, ProjFS llama a la devolución de llamada **[PRJ_GET_PLACEHOLDER_INFO_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb)** para cada elemento de la ruta de acceso que aún no existe en el disco.  Por ejemplo, si una aplicación intenta abrir , pero solo la ruta de acceso existe en el disco, el proveedor recibirá una devolución de llamada `C:\virtRoot\dir1\dir2\file.txt` `C:\virtRoot\dir1` para , a `C:\virtRoot\dir1\dir2` continuación, para `C:\virtRoot\dir1\dir2\file.txt` .

Cuando ProjFS llama a la devolución **de** llamada PRJ_GET_PLACEHOLDER_INFO_CB del proveedor, el proveedor realiza las siguientes acciones:

1. El proveedor determina si el nombre solicitado existe en su almacén de respaldo.  El proveedor debe usar **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** como rutina de comparación al buscar en su almacén de respaldo para determinar si el nombre solicitado existe en el almacén de respaldo.  Si no es así, el proveedor devuelve HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND) de la devolución de llamada.

1. Si el nombre solicitado existe en el almacén de respaldo, el proveedor rellena una estructura PRJ_PLACEHOLDER_INFO con los metadatos del sistema de archivos del elemento y llama a **[PrjWritePlaceholderInfo](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para enviar los datos [a](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) ProjFS.  ProjFS usará esa información para crear un marcador de posición en el sistema de archivos local para el elemento.

    > ProjFS usará cualquier FILE_ATTRIBUTE marca los conjuntos de proveedores en el miembro **FileBasicInfo.FileAttributes** de PRJ_PLACEHOLDER_INFO excepto FILE_ATTRIBUTE_DIRECTORY; establecerá el valor correcto para FILE_ATTRIBUTE_DIRECTORY en el miembro **FileBasicInfo.FileAttributes** según el valor proporcionado del **miembro FileBasicInfo.IsDirectory.**

    > Si el almacén de respaldo admite vínculos simbólicos, el proveedor debe usar **[PrjWritePlaceholderInfo2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2)** para enviar los datos del marcador de posición a ProjFS.  **PrjWritePlaceholderInfo2** admite una entrada de búfer adicional que permite al proveedor especificar que el marcador de posición es un vínculo simbólico y cuál es su destino.  De lo contrario, se comporta como se describió anteriormente para **PrjWritePlaceholderInfo**.  En el ejemplo siguiente se muestra cómo usar **PrjWritePlaceholderInfo2** para proporcionar compatibilidad con vínculos simbólicos.
    >
    > Tenga en **cuenta que PrjWritePlaceholderInfo2** se admite a partir Windows 10, versión 2004.  Un proveedor debe sondear la existencia de **PrjWritePlaceholderInfo2,** por ejemplo mediante **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

```C++
HRESULT
MyGetPlaceholderInfoCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
    )
{
    // MyGetItemInfo is a routine the provider might implement to get
    // information from its backing store for a given file path.  The first
    // parameter is an _In_ parameter that supplies the name to look for.
    // If the item exists the routine provides the file information in the
    // remaining parameters, all of which are annotated _Out_:
    // * 2nd parameter: the name as it appears in the backing store
    // * 3rd-9th parameters: basic file info
    // * 10th parameter: if the item is a symbolic link, a pointer to a 
    //   NULL-terminated string identifying the link's target
    //
    // Note that the routine returns the name that is in the backing
    // store.  This is because the input file path may not be in the same
    // case as what is in the backing store.  The provider should create
    // the placeholder with the name it has in the backing store.
    //
    // Note also that this example does not provide anything beyond basic
    // file information and a possible symbolic link target.
    HRESULT hr;
    WCHAR* backingStoreName = NULL;
    WCHAR* symlinkTarget = NULL;
    PRJ_PLACEHOLDER_INFO placeholderInfo = {};
    hr = MyGetItemInfo(callbackData->FilePathName,
                       &backingStoreName,
                       &placeholderInfo.FileBasicInfo.IsDirectory,
                       &placeholderInfo.FileBasicInfo.FileSize,
                       &placeholderInfo.FileBasicInfo.CreationTime,
                       &placeholderInfo.FileBasicInfo.LastAccessTime,
                       &placeholderInfo.FileBasicInfo.LastWriteTime,
                       &placeholderInfo.FileBasicInfo.ChangeTime,
                       &placeholderInfo.FileBasicInfo.FileAttributes,
                       &symlinkTarget);

    if (FAILED(hr))
    {
        // If callbackData->FilePathName doesn't exist in our backing store then
        // MyGetItemInfo should HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND).
        // If this is some other error, e.g. E_OUTOFMEMORY because MyGetItemInfo
        // couldn't allocate space for backingStoreName, we return that.
        return hr;
    }

    // If the file path is for a symbolic link, pass that in with the placeholder info.
    if (symlinkTarget != NULL)
    {
        PRJ_EXTENDED_INFO extraInfo = {};

        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
        extraInfo.Symlink.TargetName = symlinkTarget;

        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo2(callbackData->NamespaceVirtualizationContext,
                                      backingStoreName,
                                      &placeholderInfo,
                                      sizeof(placeholderInfo),
                                      &extraInfo);
    }
    else
    {
        // If this returns an error we'll want to return that error from the callback.
        hr = PrjWritePlaceholderInfo(callbackData->NamespaceVirtualizationContext,
                                     backingStoreName,
                                     &placeholderInfo,
                                     sizeof(placeholderInfo));
    }

    free(backingStoreName);

    if (symlinkTarget != NULL)
    {
        free(symlinkTarget);
    }

    return hr;
}
```

## <a name="providing-file-contents"></a>Proporcionar contenido del archivo

Cuando ProjFS necesita asegurarse de que un archivo virtualizado contiene datos, como cuando una aplicación intenta leer del archivo, ProjFS llama a la devolución de llamada **[PRJ_GET_FILE_DATA_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** de ese elemento para solicitar que el proveedor proporcione el contenido del archivo.  El proveedor recupera los datos del archivo de su almacén de respaldo y usa **[PrjWriteFileData](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata)** para enviar los datos al sistema de archivos local.

> Cuando ProjFS llama a esta devolución de llamada, el miembro **FilePathName** del parámetro _callbackData_ proporciona el nombre que tenía el archivo cuando se creó su marcador de posición.  Es decir, si se ha cambiado el nombre del archivo desde que se creó su marcador de posición, la devolución de llamada proporciona el nombre original (anterior al cambio de nombre), no el nombre actual (posterior al cambio de nombre).  Si es necesario, el proveedor puede usar el **miembro VersionInfo** del parámetro _callbackData_ para determinar qué datos de archivo se solicitan.
>
> Para obtener más información sobre cómo se puede usar el miembro **VersionInfo** de PRJ_CALLBACK_DATA, vea la documentación [de PRJ_PLACEHOLDER_VERSION_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) y el tema Control de cambios [de vista.](handling-view-changes.md)

El proveedor puede dividir el intervalo de datos solicitado en la devolución de **llamada de PRJ_GET_FILE_DATA_CB** en varias llamadas a **PrjWriteFileData**, cada una de las que proporciona una parte del intervalo solicitado.  Sin embargo, el proveedor debe proporcionar todo el intervalo solicitado antes de completar la devolución de llamada.  Por ejemplo, si la devolución de llamada solicita 10 MB de datos de _byteOffset_ 0 para una longitud _de_ 10 485 760, el proveedor puede optar por proporcionar los datos en 10 llamadas a **PrjWriteFileData,** cada una con un envío de 1 MB.

El proveedor también es libre de proporcionar más que el intervalo solicitado, hasta la longitud del archivo.  El intervalo que proporciona el proveedor debe cubrir el intervalo solicitado.  Por ejemplo, si la devolución de llamada solicita 1 MB de  datos de _byteOffset_ 4096 para la longitud 1052 672 y el archivo tiene un tamaño total de 10 MB, el proveedor podría optar por devolver 2 MB de datos a partir del desplazamiento 0.

### <a name="buffer-alignment-considerations"></a>Consideraciones sobre la alineación del búfer

ProjFS usa la [FILE_OBJECT](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) del autor de la llamada que requiere que los datos escriban los datos en el sistema de archivos local.  Sin embargo, ProjFS no puede controlar si ese FILE_OBJECT se abrió para E/S almacenada en búfer o no almacenada en búfer.  Si el FILE_OBJECT se abrió para E/S no almacenada en búfer, las lecturas y escrituras en el archivo deben cumplir determinados requisitos de alineación.  El proveedor puede cumplir esos requisitos de alineación haciendo dos cosas:

1. Use **[PrjAllocateAlignedBuffer para asignar](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer)** el búfer para pasar el  parámetro buffer de **PrjWriteFileData.**
1. Asegúrese de que los parámetros _byteOffset_ y _length_ de **PrjWriteFileData** son múltiplo enteros del requisito de alineación del dispositivo de almacenamiento (tenga en cuenta que el parámetro _length_ no tiene que cumplir este requisito si _byteOffset_ length es igual al final del  +   archivo).  El proveedor puede usar **[PrjGetVirtualizationInstanceInfo para](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo)** recuperar el requisito de alineación del dispositivo de almacenamiento.

ProjFS deja que el proveedor calcule la alineación adecuada.  Esto se debe **a** que, al procesar una devolución de llamada PRJ_GET_FILE_DATA_CB, el proveedor puede optar por devolver los datos solicitados a través de varias llamadas **PrjWriteFileData,** cada una de las que devuelve parte del total de datos solicitados, antes de completar la devolución de llamada.

> Si el proveedor va a usar una sola llamada a **PrjWriteFileData** para escribir todo el archivo, es decir, de _byteOffset_ = 0 a _length_ = size del archivo, o para devolver el intervalo exacto solicitado en la devolución de llamada **de PRJ_GET_FILE_DATA_CB,** el proveedor no tiene que realizar ningún cálculo de alineación.  Sin embargo, debe seguir utilizando **PrjAllocateAlignedBuffer para** asegurarse de que el _búfer_ cumple los requisitos de alineación del dispositivo de almacenamiento.

Vea el tema [Almacenamiento en búfer de archivos](/windows/desktop/FileIO/file-buffering) para obtener más información sobre E/S almacenadas en búfer frente a E/S no almacenadas en búfer.

```C++
//  BlockAlignTruncate(): Aligns P on the previous V boundary (V must be != 0).
#define BlockAlignTruncate(P,V) ((P) & (0-((UINT64)(V))))

// This sample illustrates both returning the entire requested range in a
// single call to PrjWriteFileData(), and splitting it up into smaller 
// units.  Note that the provider must return all the requested data before
// completing the PRJ_GET_FILE_DATA_CB callback with S_OK.
HRESULT
MyGetFileDataCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ UINT64 byteOffset,
    _In_ UINT32 length
    )
{
    HRESULT hr;

    // For the purposes of this sample our provider has a 1 MB limit to how
    // much data it can return at once (perhaps its backing store imposes such
    // a limit).
    UINT64 writeStartOffset;
    UINT32 writeLength;
    if (length <= 1024*1024)
    {
        // The range requested in the callback is less than 1MB, so we can return
        // the data in a single call, without doing any alignment calculations.
        writeStartOffset = byteOffset;
        writeLength = length;
    }
    else
    {
        // The range requested is more than 1MB.  Retrieve the device alignment
        // and calculate a transfer size that conforms to the device alignment and
        // is <= 1MB.
        PRJ_VIRTUALIZATION_INSTANCE_INFO instanceInfo;
        UINT32 infoSize = sizeof(instanceInfo);
        hr = PrjGetVirtualizationInstanceInfo(callbackData->NamespaceVirtualizationContext,
                                              &infoSize,
                                              &instanceInfo);

        if (FAILED(hr))
        {
            return hr;
        }

        // The first transfer will start at the beginning of the requested range,
        // which is guaranteed to have the correct alignment.
        writeStartOffset = byteOffset;

        // Ensure our transfer size is aligned to the device alignment, and is
        // no larger than 1 MB (note this assumes the device alignment is less
        // than 1 MB).
        UINT64 writeEndOffset = BlockAlignTruncate(writeStartOffset + 1024*1024,
                                                   instanceInfo->WriteAlignment);
        assert(writeEndOffset > 0);
        assert(writeEndOffset > writeStartOffset);

        writeLength = writeEndOffset - writeStartOffset;
    }

    // Allocate a buffer that adheres to the needed memory alignment.
    void* writeBuffer = NULL;
    writeBuffer = PrjAllocateAlignedBuffer(callbackData->NamespaceVirtualizationContext,
                                           writeLength);

    if (writeBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    do
    {
        // MyGetFileDataFromStore is a routine the provider might implement to copy
        // data for the specified file from the provider's backing store to a
        // buffer.  The routine finds the file located at callbackData->FilePathName
        // and copies writeLength bytes of its data, starting at writeStartOffset,
        // to the buffer pointed to by writeBuffer.
        hr = MyGetFileDataFromStore(callbackData->FilePathName,
                                    writeStartOffset,
                                    writeLength,
                                    writeBuffer);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // Write the data to the file in the local file system.
        hr = PrjWriteFileData(callbackData->NamespaceVirtualizationContext,
                              callbackData->DataStreamId,
                              writeBuffer,
                              writeStartOffset,
                              writeLength);

        if (FAILED(hr))
        {
            PrjFreeAlignedBuffer(writeBuffer);
            return hr;
        }

        // The length parameter to the callback is guaranteed to be either
        // correctly aligned or to result in a write to the end of the file.
        length -= writeLength;
        if (length < writeLength)
        {
            writeLength = length;
        }
    }
    while (writeLength > 0);

    PrjFreeAlignedBuffer(writeBuffer);
    return hr;
}
```