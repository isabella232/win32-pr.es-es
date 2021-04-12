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
# <a name="reading-files-from-the-device"></a><span data-ttu-id="30dcb-109">Lectura de archivos desde el dispositivo</span><span class="sxs-lookup"><span data-stu-id="30dcb-109">Reading Files from the Device</span></span>

<span data-ttu-id="30dcb-110">Cuando haya encontrado un archivo que le gustaría copiar desde el dispositivo, puede copiar el archivo del dispositivo en una sola llamada, o bien usar una devolución de llamada para que los bytes de archivo se lean directamente en la aplicación, lo que puede procesar o almacenar los datos tal como se ven ajustados.</span><span class="sxs-lookup"><span data-stu-id="30dcb-110">When you have found a file you would like to copy from the device, you can then copy the file from the device to the computer in a single call, or use a callback to have the file bytes read directly to your application, which can then process or store the data as it sees fits.</span></span>

<span data-ttu-id="30dcb-111">En los pasos siguientes se muestra la forma básica de copiar un archivo desde un dispositivo en una sola llamada:</span><span class="sxs-lookup"><span data-stu-id="30dcb-111">The following steps show the basic way to copy a file from a device in a single call:</span></span>

1.  <span data-ttu-id="30dcb-112">Obtiene un identificador para el archivo en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30dcb-112">Get a handle to the file on the device.</span></span> <span data-ttu-id="30dcb-113">Puede obtener el identificador mediante una búsqueda de archivos recursiva o, si conoce el identificador persistente del almacenamiento, mediante una llamada a [**IWMDMDevice3:: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span><span class="sxs-lookup"><span data-stu-id="30dcb-113">You might obtain the handle by using a recursive file search or, if you know the persistent ID of the storage, by calling [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span></span> <span data-ttu-id="30dcb-114">En cualquier caso, necesita la interfaz [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) del objeto.</span><span class="sxs-lookup"><span data-stu-id="30dcb-114">In either case, you need the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface of the object.</span></span>
2.  <span data-ttu-id="30dcb-115">Determine si el almacenamiento es un archivo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="30dcb-115">Determine whether the storage is a file or a folder.</span></span> <span data-ttu-id="30dcb-116">Solo se pueden copiar archivos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30dcb-116">Only files can be copied from the device.</span></span> <span data-ttu-id="30dcb-117">Llame a [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para obtener los atributos de almacenamiento, que le indicará si el almacenamiento es un archivo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="30dcb-117">Call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to get storage attributes, which will tell you whether the storage is a file or a folder.</span></span>
3.  <span data-ttu-id="30dcb-118">Consulte **IWMDMStorage** para [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)y llame a [**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) para leer el archivo del dispositivo y guardarlo en una ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="30dcb-118">Query **IWMDMStorage** for [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol), and call [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) to read the file from the device and save it to a specified location.</span></span>

<span data-ttu-id="30dcb-119">Si, en su lugar, desea leer el bloque File Block by del dispositivo, debe implementar la interfaz de devolución de llamada [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) .</span><span class="sxs-lookup"><span data-stu-id="30dcb-119">If, instead, you want to read the file block by block from the device, you must implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) callback interface.</span></span> <span data-ttu-id="30dcb-120">Pase esta interfaz a la llamada **IWMDMStorageControl:: Read** y Windows Media administrador de dispositivos enviará fragmentos de datos de archivo secuencialmente a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="30dcb-120">Pass this interface into the **IWMDMStorageControl::Read** call, and Windows Media Device Manager will send chunks of file data sequentially to your callback.</span></span> <span data-ttu-id="30dcb-121">En los pasos siguientes se muestra cómo leer un bloque bloque de archivos de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="30dcb-121">The following steps show how to read a device file block by block:</span></span>

1.  <span data-ttu-id="30dcb-122">Obtenga la interfaz **IWMDMStorage** para el almacenamiento y determine si se trata de un archivo, tal y como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="30dcb-122">Get the **IWMDMStorage** interface for the storage and determine whether it is a file, as described previously.</span></span>
2.  <span data-ttu-id="30dcb-123">Prepare los identificadores de archivo u otros identificadores que necesite para almacenar los datos recibidos.</span><span class="sxs-lookup"><span data-stu-id="30dcb-123">Prepare any file handles or other handles you need to hold the received data.</span></span>
3.  <span data-ttu-id="30dcb-124">Consulta de la interfaz **IWMDMStorageControl** del almacenamiento</span><span class="sxs-lookup"><span data-stu-id="30dcb-124">Query for the storage's **IWMDMStorageControl** interface</span></span>
4.  <span data-ttu-id="30dcb-125">Llame a **IWMDMStorageControl:: Read** para comenzar la operación de lectura, pasando la interfaz **IWMDMOperation** que ha implementado.</span><span class="sxs-lookup"><span data-stu-id="30dcb-125">Call **IWMDMStorageControl::Read** to begin the read operation, passing in the **IWMDMOperation** interface you have implemented.</span></span>
5.  <span data-ttu-id="30dcb-126">Windows Media Administrador de dispositivos enviará el bloque de datos por bloque al dispositivo, tal y como se describe en control de las [transferencias de archivos manualmente](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="30dcb-126">Windows Media Device Manager will send the data block by block to your device as described in [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>

<span data-ttu-id="30dcb-127">La siguiente función de ejemplo de C++ lee un objeto de almacenamiento desde un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30dcb-127">The following C++ example function reads a storage object from a device.</span></span> <span data-ttu-id="30dcb-128">La función acepta un puntero de interfaz **IWMDMOperation** opcional; Si se envía, la función creará un archivo explícitamente y controlará la escritura de los datos en el archivo en su implementación de **IWMDMOperation:: TransferObjectData**; Si no es así, leerá el archivo y lo guardará en el destino especificado por *pwszDestName*.</span><span class="sxs-lookup"><span data-stu-id="30dcb-128">The function accepts an optional **IWMDMOperation** interface pointer; if submitted, the function will create a file explicitly and handle writing the data to file on its implementation of **IWMDMOperation::TransferObjectData**; if not, it will read the file and save to the destination specified by *pwszDestName*.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="30dcb-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30dcb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30dcb-130">**Crear una aplicación de Windows Media Administrador de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="30dcb-130">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




