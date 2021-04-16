---
title: Envío del archivo al dispositivo
description: Envío del archivo al dispositivo
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Media Administrador de dispositivos, enviar archivos a dispositivos
- Administrador de dispositivos, enviar archivos a dispositivos
- Guía de programación, enviar archivos a dispositivos
- aplicaciones de escritorio, enviar archivos a dispositivos
- crear aplicaciones de Windows Media Administrador de dispositivos, enviar archivos a dispositivos
- escribir archivos en dispositivos, enviar archivos a dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532188"
---
# <a name="sending-the-file-to-the-device"></a>Envío del archivo al dispositivo

Una vez que el archivo se ha transcodificado en caso necesario y se han establecido todos los metadatos que incluyen el formato, la aplicación puede enviar el archivo al dispositivo. Para ello, primero debe obtener una interfaz **IWMDMStorageControl** (o una versión posterior) para una ubicación de destino en el dispositivo. Las marcas de **inserción** especifican si el nuevo almacenamiento debe ser un elemento relacionado o secundario del destino. Una vez que haya obtenido el destino, puede llamar a [**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para transferir el archivo. La aplicación puede controlar la lectura de los datos de archivo mediante la implementación de [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), o puede permitir que el método **Insert** Lea y transfiera el archivo automáticamente si no proporciona un puntero a un **IWMDMOperation** implementado por la aplicación.

En el código de C++ siguiente se muestra la llamada a **Insert3** para escribir un archivo en un dispositivo. Si el puntero *pOperation* pasado a **Insert3** es **null**, el archivo se enviará en un paso; Si este puntero es un puntero de interfaz válido, Windows Media Administrador de dispositivos llamará al método de devolución de llamada para obtener los datos de los bloques. Para obtener más información sobre cómo implementar **IWMDMOperation**, vea [administrar las transferencias de archivos manualmente](handling-file-transfers-manually.md).


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

 

 




