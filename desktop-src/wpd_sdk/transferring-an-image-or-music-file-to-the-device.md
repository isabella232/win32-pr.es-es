---
description: Transferencia de una imagen o un archivo de música al dispositivo
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Transferencia de una imagen o un archivo de música al dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716659"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a><span data-ttu-id="70572-103">Transferencia de una imagen o un archivo de música al dispositivo</span><span class="sxs-lookup"><span data-stu-id="70572-103">Transferring an Image or Music File to the Device</span></span>

<span data-ttu-id="70572-104">Una de las operaciones más comunes que realiza una aplicación es la transferencia de contenido a un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="70572-104">One of the most common operations accomplished by an application is the transfer of content to a connected device.</span></span>

<span data-ttu-id="70572-105">Las transferencias de contenido se realizan mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="70572-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="70572-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="70572-106">Interface</span></span>                                                                | <span data-ttu-id="70572-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="70572-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="70572-108">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="70572-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="70572-109">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="70572-109">Provides access to the content-specific methods.</span></span>               |
| [<span data-ttu-id="70572-110">**Interfaz IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="70572-110">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | <span data-ttu-id="70572-111">Se usa al escribir el contenido en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70572-111">Used when writing the content to the device.</span></span>                   |
| [<span data-ttu-id="70572-112">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="70572-112">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="70572-113">Se utiliza para recuperar las propiedades que describen el contenido.</span><span class="sxs-lookup"><span data-stu-id="70572-113">Used to retrieve properties that describe the content.</span></span>         |
| <span data-ttu-id="70572-114">IStream (interfaz)</span><span class="sxs-lookup"><span data-stu-id="70572-114">IStream Interface</span></span>                                                        | <span data-ttu-id="70572-115">Se usa para simplificar la lectura del contenido y la escritura en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70572-115">Used to simplify reading of content and writing to the device.</span></span> |



 

<span data-ttu-id="70572-116">La `TransferContentToDevice` función del módulo ContentTransfer. cpp de la aplicación de ejemplo muestra cómo una aplicación podría transferir contenido desde un equipo a un dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="70572-116">The `TransferContentToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer content from a PC to a connected device.</span></span> <span data-ttu-id="70572-117">En este ejemplo concreto, el contenido transferido puede ser un archivo que contenga una imagen, música o información de contacto.</span><span class="sxs-lookup"><span data-stu-id="70572-117">In this particular sample, the transferred content can be a file containing an image, music, or contact information.</span></span>

<span data-ttu-id="70572-118">La primera tarea que se realiza mediante la `TransferContentToDevice` función es pedir al usuario que escriba un identificador de objeto, que identifica el objeto que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="70572-118">The first task accomplished by the `TransferContentToDevice` function is to prompt the user to enter an object identifier, which identifies the object to be transferred.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="70572-119">La segunda tarea que se realiza mediante la `TransferContentToDevice` función es crear un objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) llamando al método [**IPortableDevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="70572-119">The second task accomplished by the `TransferContentToDevice` function is to create an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="70572-120">La siguiente tarea que se realiza mediante la `TransferContentToDevice` función es la creación de un cuadro de diálogo **FileOpen** con el que el usuario puede especificar la ubicación y el nombre del archivo que se va a transferir.</span><span class="sxs-lookup"><span data-stu-id="70572-120">The next task accomplished by the `TransferContentToDevice` function is the creation of a **FileOpen** dialog with which the user can specify the location and name of the file to be transferred.</span></span>


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="70572-121">La `TransferContentToDevice` función pasa una cadena de filtro ( `wszFileTypeFilter` ) al método GetOpenFileName, que determina el tipo de archivos que el usuario puede elegir.</span><span class="sxs-lookup"><span data-stu-id="70572-121">The `TransferContentToDevice` function passes a filter string (`wszFileTypeFilter`) to the GetOpenFileName method, which determines the type of files that the user can choose.</span></span> <span data-ttu-id="70572-122">Consulte la `DoMenu` función en el módulo WpdApiSample. cpp para obtener ejemplos de los tres filtros diferentes permitidos por el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="70572-122">Refer to the `DoMenu` function in the WpdApiSample.cpp module for examples of the three different filters allowed by the sample.</span></span>

<span data-ttu-id="70572-123">Una vez que el usuario identifica un archivo determinado para la transferencia al dispositivo, la `TransferContentToDevice` función abre el archivo como un objeto IStream y recupera las propiedades necesarias para completar la transferencia.</span><span class="sxs-lookup"><span data-stu-id="70572-123">After the user identifies a particular file for transfer to the device, the `TransferContentToDevice` function opens that file as an IStream object and retrieves properties that are required to complete the transfer.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



<span data-ttu-id="70572-124">Las propiedades necesarias se recuperan llamando a la `GetRequiredPropertiesForContentType` función auxiliar, que opera en el objeto IStream.</span><span class="sxs-lookup"><span data-stu-id="70572-124">The required properties are retrieved by calling the`GetRequiredPropertiesForContentType` helper-function, which operates on the IStream object.</span></span> <span data-ttu-id="70572-125">La `GetRequiredPropertiesForContentType` función auxiliar crea un objeto [**IPortableDeviceValues**](iportabledevicevalues.md) , recupera las propiedades de la lista siguiente y los agrega a este objeto.</span><span class="sxs-lookup"><span data-stu-id="70572-125">The `GetRequiredPropertiesForContentType` helper-function creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, retrieves the properties in the following list, and adds them to this object.</span></span>

-   <span data-ttu-id="70572-126">Identificador de objeto primario</span><span class="sxs-lookup"><span data-stu-id="70572-126">Parent-object identifier</span></span>
-   <span data-ttu-id="70572-127">Tamaño de flujo en bytes</span><span class="sxs-lookup"><span data-stu-id="70572-127">Stream size in bytes</span></span>
-   <span data-ttu-id="70572-128">Nombre del archivo de contenido</span><span class="sxs-lookup"><span data-stu-id="70572-128">Content file name</span></span>
-   <span data-ttu-id="70572-129">Nombre del contenido (el nombre de archivo sin la extensión)</span><span class="sxs-lookup"><span data-stu-id="70572-129">Content name (the file name without the extension)</span></span>
-   <span data-ttu-id="70572-130">Tipo de contenido (imagen, audio o contacto)</span><span class="sxs-lookup"><span data-stu-id="70572-130">Content type (image, audio, or contact)</span></span>
-   <span data-ttu-id="70572-131">Formato de contenido (JFIF, WMA o vCard2)</span><span class="sxs-lookup"><span data-stu-id="70572-131">Content format (JFIF, WMA, or vCard2)</span></span>

<span data-ttu-id="70572-132">La aplicación de ejemplo usa las propiedades recuperadas para crear el nuevo contenido en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70572-132">The sample application uses the retrieved properties to create the new content on the device.</span></span> <span data-ttu-id="70572-133">Esto se realiza en tres fases:</span><span class="sxs-lookup"><span data-stu-id="70572-133">This is done in three phases:</span></span>

1.  <span data-ttu-id="70572-134">La aplicación llama al método [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para crear un nuevo objeto IStream en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="70572-134">The application calls [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) method to create a new IStream object on the device.</span></span>
2.  <span data-ttu-id="70572-135">La aplicación usa este objeto para obtener un objeto [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) del controlador WPD.</span><span class="sxs-lookup"><span data-stu-id="70572-135">The application uses this object to obtain an [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) object from the WPD driver.</span></span>
3.  <span data-ttu-id="70572-136">La aplicación usa el nuevo objeto **IPortableDeviceDataStream** para escribir el contenido en el dispositivo (a través de la función auxiliar StreamCopy).</span><span class="sxs-lookup"><span data-stu-id="70572-136">The application uses the new **IPortableDeviceDataStream** object to write the content to the device (via the StreamCopy helper function).</span></span> <span data-ttu-id="70572-137">La función auxiliar escribe los datos del archivo de origen en la secuencia devuelta por [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="70572-137">The helper function writes the data from the source file to the stream returned by [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span>
4.  <span data-ttu-id="70572-138">La aplicación completa la operación llamando al método commit en el flujo de destino.</span><span class="sxs-lookup"><span data-stu-id="70572-138">The application completes the operation by calling the Commit method on the destination stream.</span></span>


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="70572-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70572-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70572-140">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="70572-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="70572-141">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="70572-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="70572-142">**Interfaz IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="70572-142">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[<span data-ttu-id="70572-143">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="70572-143">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="70572-144">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="70572-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



