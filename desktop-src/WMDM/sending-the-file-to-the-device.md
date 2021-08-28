---
title: Envío del archivo al dispositivo
description: Envío del archivo al dispositivo
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Archivos Administrador de dispositivos, envío de archivos a dispositivos
- Administrador de dispositivos, enviar archivos a dispositivos
- guía de programación, envío de archivos a dispositivos
- aplicaciones de escritorio, envío de archivos a dispositivos
- crear Windows aplicaciones Administrador de dispositivos multimedia, enviar archivos a dispositivos
- escribir archivos en dispositivos, enviar archivos a dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a47de872d03d42701ff6e95516a9ead59f1206729ae9ca70d6dd9e5f1260f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124145"
---
# <a name="sending-the-file-to-the-device"></a>Envío del archivo al dispositivo

Una vez transcodificado el archivo si es necesario y se han establecido todos los metadatos, incluido el formato, la aplicación puede enviar el archivo al dispositivo. Para ello, primero debe obtener una interfaz **IWMDMStorageControl** (o una versión posterior) para una ubicación de destino en el dispositivo. Las **marcas Insert** especifican si el nuevo almacenamiento debe ser del mismo nivel o secundario del destino. Una vez que haya obtenido el destino, puede llamar a [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para transferir el archivo. La aplicación puede controlar la lectura de los datos del archivo mediante la implementación de [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), o puede permitir que el método **Insert** lea y transfiera el archivo automáticamente al no proporcionar un puntero a una **IWMDMOperation** implementada por la aplicación.

El siguiente código de C++ muestra cómo llamar a **Insert3** para escribir un archivo en un dispositivo. Si el *puntero pOperation* pasado a **Insert3** es **NULL,** el archivo se enviará en un paso; Si este puntero es un puntero de interfaz válido, Windows media Administrador de dispositivos llamará al método de devolución de llamada para obtener datos en bloques. Para obtener más información sobre cómo implementar **IWMDMOperation**, vea Controlar las [transferencias de archivos manualmente.](handling-file-transfers-manually.md)


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




