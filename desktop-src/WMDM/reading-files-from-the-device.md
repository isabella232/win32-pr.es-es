---
title: Lectura de archivos desde el dispositivo
description: Lectura de archivos desde el dispositivo
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Media Administrador de dispositivos, lectura de archivos desde dispositivos
- Administrador de dispositivos, lectura de archivos desde dispositivos
- Guía de programación, lectura de archivos desde dispositivos
- aplicaciones de escritorio, leer archivos de dispositivos
- creación de aplicaciones de Windows Media Administrador de dispositivos, lectura de archivos desde dispositivos
- lectura de archivos desde dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b80cf820e889b29e612206f90b07e1cb02c4c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268417"
---
# <a name="reading-files-from-the-device"></a>Lectura de archivos desde el dispositivo

Cuando haya encontrado un archivo que le gustaría copiar desde el dispositivo, puede copiar el archivo del dispositivo en una sola llamada, o bien usar una devolución de llamada para que los bytes de archivo se lean directamente en la aplicación, lo que puede procesar o almacenar los datos tal como se ven ajustados.

En los pasos siguientes se muestra la forma básica de copiar un archivo desde un dispositivo en una sola llamada:

1.  Obtiene un identificador para el archivo en el dispositivo. Puede obtener el identificador mediante una búsqueda de archivos recursiva o, si conoce el identificador persistente del almacenamiento, mediante una llamada a [**IWMDMDevice3:: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage). En cualquier caso, necesita la interfaz [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) del objeto.
2.  Determine si el almacenamiento es un archivo o una carpeta. Solo se pueden copiar archivos del dispositivo. Llame a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para obtener los atributos de almacenamiento, que le indicará si el almacenamiento es un archivo o una carpeta.
3.  Consulte **IWMDMStorage** para [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)y llame a [**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) para leer el archivo del dispositivo y guardarlo en una ubicación especificada.

Si, en su lugar, desea leer el bloque File Block by del dispositivo, debe implementar la interfaz de devolución de llamada [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) . Pase esta interfaz a la llamada **IWMDMStorageControl:: Read** y Windows Media administrador de dispositivos enviará fragmentos de datos de archivo secuencialmente a la devolución de llamada. En los pasos siguientes se muestra cómo leer un bloque bloque de archivos de dispositivo:

1.  Obtenga la interfaz **IWMDMStorage** para el almacenamiento y determine si se trata de un archivo, tal y como se ha descrito anteriormente.
2.  Prepare los identificadores de archivo u otros identificadores que necesite para almacenar los datos recibidos.
3.  Consulta de la interfaz **IWMDMStorageControl** del almacenamiento
4.  Llame a **IWMDMStorageControl:: Read** para comenzar la operación de lectura, pasando la interfaz **IWMDMOperation** que ha implementado.
5.  Windows Media Administrador de dispositivos enviará el bloque de datos por bloque al dispositivo, tal y como se describe en control de las [transferencias de archivos manualmente](handling-file-transfers-manually.md).

La siguiente función de ejemplo de C++ lee un objeto de almacenamiento desde un dispositivo. La función acepta un puntero de interfaz **IWMDMOperation** opcional; Si se envía, la función creará un archivo explícitamente y controlará la escritura de los datos en el archivo en su implementación de **IWMDMOperation:: TransferObjectData**; Si no es así, leerá el archivo y lo guardará en el destino especificado por *pwszDestName*.


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




