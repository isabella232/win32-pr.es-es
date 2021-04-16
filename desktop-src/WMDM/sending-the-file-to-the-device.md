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
# <a name="sending-the-file-to-the-device"></a><span data-ttu-id="13f31-109">Envío del archivo al dispositivo</span><span class="sxs-lookup"><span data-stu-id="13f31-109">Sending the File to the Device</span></span>

<span data-ttu-id="13f31-110">Una vez que el archivo se ha transcodificado en caso necesario y se han establecido todos los metadatos que incluyen el formato, la aplicación puede enviar el archivo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f31-110">After the file has been transcoded if necessary, and all metadata including the format has been set, your application can send the file to the device.</span></span> <span data-ttu-id="13f31-111">Para ello, primero debe obtener una interfaz **IWMDMStorageControl** (o una versión posterior) para una ubicación de destino en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f31-111">In order to do so, you must first get an **IWMDMStorageControl** interface (or a later version) for a target location on the device.</span></span> <span data-ttu-id="13f31-112">Las marcas de **inserción** especifican si el nuevo almacenamiento debe ser un elemento relacionado o secundario del destino.</span><span class="sxs-lookup"><span data-stu-id="13f31-112">The **Insert** flags specify whether the new storage should be a sibling or child of the target.</span></span> <span data-ttu-id="13f31-113">Una vez que haya obtenido el destino, puede llamar a [**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para transferir el archivo.</span><span class="sxs-lookup"><span data-stu-id="13f31-113">Once you have gotten the target, you can call [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to transfer the file.</span></span> <span data-ttu-id="13f31-114">La aplicación puede controlar la lectura de los datos de archivo mediante la implementación de [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), o puede permitir que el método **Insert** Lea y transfiera el archivo automáticamente si no proporciona un puntero a un **IWMDMOperation** implementado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="13f31-114">The application can handle reading the file data itself by implementing [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), or it can allow the **Insert** method to read and transfer the file automatically by not providing a pointer to an application-implemented **IWMDMOperation**.</span></span>

<span data-ttu-id="13f31-115">En el código de C++ siguiente se muestra la llamada a **Insert3** para escribir un archivo en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13f31-115">The following C++ code demonstrates calling **Insert3** to write a file to a device.</span></span> <span data-ttu-id="13f31-116">Si el puntero *pOperation* pasado a **Insert3** es **null**, el archivo se enviará en un paso; Si este puntero es un puntero de interfaz válido, Windows Media Administrador de dispositivos llamará al método de devolución de llamada para obtener los datos de los bloques.</span><span class="sxs-lookup"><span data-stu-id="13f31-116">If the *pOperation* pointer passed to **Insert3** is **NULL**, the file will be sent in one step; if this pointer is a valid interface pointer, Windows Media Device Manager will call your callback method to get data in blocks.</span></span> <span data-ttu-id="13f31-117">Para obtener más información sobre cómo implementar **IWMDMOperation**, vea [administrar las transferencias de archivos manualmente](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="13f31-117">For details on how to implement **IWMDMOperation**, see [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="13f31-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13f31-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13f31-119">**Escribir archivos en el dispositivo**</span><span class="sxs-lookup"><span data-stu-id="13f31-119">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




