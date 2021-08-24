---
title: Leer archivos desde el dispositivo
description: Leer archivos desde el dispositivo
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Archivos Administrador de dispositivos, lectura de archivos de dispositivos
- Administrador de dispositivos,lectura de archivos de dispositivos
- guía de programación, lectura de archivos de dispositivos
- aplicaciones de escritorio, lectura de archivos de dispositivos
- crear Windows aplicaciones Administrador de dispositivos multimedia, leer archivos de dispositivos
- leer archivos de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904005"
---
# <a name="reading-files-from-the-device"></a>Leer archivos desde el dispositivo

Cuando haya encontrado un archivo que le gustaría copiar desde el dispositivo, puede copiar el archivo desde el dispositivo al equipo en una sola llamada o usar una devolución de llamada para que los bytes de archivo se lean directamente en la aplicación, lo que puede procesar o almacenar los datos a medida que se ajuste.

Los pasos siguientes muestran la manera básica de copiar un archivo desde un dispositivo en una sola llamada:

1.  Obtenga un identificador para el archivo en el dispositivo. Puede obtener el identificador mediante una búsqueda de archivos recursiva o, si conoce el identificador persistente del almacenamiento, llamando a [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage). En cualquier caso, necesita la [**interfaz IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) del objeto .
2.  Determine si el almacenamiento es un archivo o una carpeta. Solo se pueden copiar archivos del dispositivo. Llame [**a IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para obtener atributos de almacenamiento, lo que le indicará si el almacenamiento es un archivo o una carpeta.
3.  Consulte **IWMDMStorage** para [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)y llame a [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) para leer el archivo del dispositivo y guardarlo en una ubicación especificada.

Si, en su lugar, quiere leer el bloque de archivos bloque a bloque desde el dispositivo, debe implementar la interfaz de devolución de llamada [**IWMDMOperation.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) Pase esta interfaz a la llamada **IWMDMStorageControl::Read** y Windows Media Administrador de dispositivos enviará fragmentos de datos de archivo secuencialmente a la devolución de llamada. Los pasos siguientes muestran cómo leer un archivo de dispositivo bloque a bloque:

1.  Obtenga la **interfaz IWMDMStorage** para el almacenamiento y determine si se trata de un archivo, como se ha descrito anteriormente.
2.  Prepare los identificadores de archivo u otros identificadores que necesite para contener los datos recibidos.
3.  Consulta de la interfaz **IWMDMStorageControl** del almacenamiento
4.  Llame **a IWMDMStorageControl::Read** para comenzar la operación de lectura y pase la **interfaz IWMDMOperation** que ha implementado.
5.  Windows Los Administrador de dispositivos enviarán el bloque de datos bloque a bloque al dispositivo, tal y como se describe en Control manual [de transferencias de archivos.](handling-file-transfers-manually.md)

La siguiente función de ejemplo de C++ lee un objeto de almacenamiento de un dispositivo. La función acepta un puntero de interfaz **IWMDMOperation** opcional; si se envía, la función creará un archivo explícitamente y controlará la escritura de los datos en el archivo en su implementación de **IWMDMOperation::TransferObjectData**; Si no es así, leerá el archivo y guardará en el destino especificado por *pwszDestName*.


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

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




