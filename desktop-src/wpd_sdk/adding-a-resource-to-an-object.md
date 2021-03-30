---
description: Agregar un recurso a un objeto
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: Agregar un recurso a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869b5cdcf172c4b8f27f7081bfce8e6f05073789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360916"
---
# <a name="adding-a-resource-to-an-object"></a><span data-ttu-id="84ed5-103">Agregar un recurso a un objeto</span><span class="sxs-lookup"><span data-stu-id="84ed5-103">Adding a Resource to an Object</span></span>

<span data-ttu-id="84ed5-104">Además de transferir objetos a un dispositivo, también es posible agregar recursos a los objetos.</span><span class="sxs-lookup"><span data-stu-id="84ed5-104">In addition to transferring objects to a device, it's also possible to add resources to objects.</span></span> <span data-ttu-id="84ed5-105">Por ejemplo, una aplicación podría agregar una foto a la información existente de un contacto determinado.</span><span class="sxs-lookup"><span data-stu-id="84ed5-105">For example, an application could add a photo to existing information for a given contact.</span></span>

<span data-ttu-id="84ed5-106">Los recursos se agregan mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="84ed5-106">Resources are added using the interfaces described in the following table.</span></span>



| <span data-ttu-id="84ed5-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="84ed5-107">Interface</span></span>                                                              | <span data-ttu-id="84ed5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="84ed5-108">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="84ed5-109">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="84ed5-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | <span data-ttu-id="84ed5-110">Proporciona acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="84ed5-110">Provides access to the content-specific methods.</span></span>                  |
| [<span data-ttu-id="84ed5-111">**Interfaz IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="84ed5-111">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | <span data-ttu-id="84ed5-112">Se usa al escribir las propiedades de los recursos y los datos en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84ed5-112">Used when writing the resource properties and data to the device.</span></span> |
| [<span data-ttu-id="84ed5-113">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="84ed5-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)       | <span data-ttu-id="84ed5-114">Se usa para escribir propiedades que describen el recurso.</span><span class="sxs-lookup"><span data-stu-id="84ed5-114">Used to write properties that describe the resource.</span></span>              |
| <span data-ttu-id="84ed5-115">IStream (interfaz)</span><span class="sxs-lookup"><span data-stu-id="84ed5-115">IStream Interface</span></span>                                                      | <span data-ttu-id="84ed5-116">Se usa para simplificar la escritura del recurso en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84ed5-116">Used to simplify writing the resource to the device.</span></span>              |



 

<span data-ttu-id="84ed5-117">La función CreateContactPhotoResourceOnDevice del módulo ContentTransfer. cpp de la aplicación de ejemplo muestra cómo una aplicación puede Agregar un recurso de fotografía a un objeto de contacto.</span><span class="sxs-lookup"><span data-stu-id="84ed5-117">The CreateContactPhotoResourceOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application could add a photo resource to a contact object.</span></span> <span data-ttu-id="84ed5-118">Esta función solicita al usuario el identificador de objeto del contacto en el dispositivo al que se agregará el recurso de fotografía.</span><span class="sxs-lookup"><span data-stu-id="84ed5-118">This function prompts the user for the object identifier of the contact on the device, to which the photo resource will be added.</span></span> <span data-ttu-id="84ed5-119">A continuación, se muestra un cuadro de diálogo FileOpen para que el usuario pueda seleccionar la imagen que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="84ed5-119">Then it displays a FileOpen dialog box so that the user can select the image to be added.</span></span> <span data-ttu-id="84ed5-120">Una vez que se recopilan estos datos, la aplicación escribe el recurso en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84ed5-120">Once this data is collected, the application writes the resource to the device.</span></span>

<span data-ttu-id="84ed5-121">La primera tarea que se realiza mediante la función CreateContactPhotoResourceOnDevice es pedir al usuario que escriba un identificador de objeto para el contacto al que se agregará la foto.</span><span class="sxs-lookup"><span data-stu-id="84ed5-121">The first task accomplished by the CreateContactPhotoResourceOnDevice function is to prompt the user to enter an object identifier for the contact to which the photo will be added.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
printf("Enter the identifer of the object to which we will add an Audio annotation.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting resource creation\n");
}do
```



<span data-ttu-id="84ed5-122">El paso siguiente es la recuperación de un objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) que, a su vez, se usa para obtener un objeto [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) .</span><span class="sxs-lookup"><span data-stu-id="84ed5-122">The next step is the retrieval of an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which in turn is used to obtain an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object.</span></span> <span data-ttu-id="84ed5-123">(La aplicación utiliza este último objeto para crear y escribir el nuevo recurso).</span><span class="sxs-lookup"><span data-stu-id="84ed5-123">(The application uses this latter object to create and write the new resource.)</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}





if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="84ed5-124">Después de esto, el ejemplo muestra el cuadro de diálogo **FileOpen** , que permite al usuario especificar el nombre del archivo de imagen que contiene la foto que desea agregar a la información de contacto.</span><span class="sxs-lookup"><span data-stu-id="84ed5-124">After this, the sample displays the **FileOpen** dialog box, which allows the user to specify the name of the image file that contains the photo they want to add to the contact information.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = wszFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(wszFilePath);
    OpenFileNameInfo.lpstrFilter    = L"JPEG (*.JPG)\0*.JPG\0JPEG (*.JPEG)\0*.JPEG\0JPG (*.JPE)\0*.JPE\0JPG (*.JFIF)\0*.JFIF\0\0";;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = L"JPG";

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was cancelled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="84ed5-125">Una vez que el ejemplo tiene un objeto [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) y el nombre del archivo de imagen, hace lo siguiente como preparación para transferir realmente los datos al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84ed5-125">Once the sample has an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object and the name of the image file, it does the following in preparation for actually transferring data to the device.</span></span>

1.  <span data-ttu-id="84ed5-126">Se abre un objeto IStream en el archivo seleccionado para las operaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="84ed5-126">It opens an IStream object on the selected file for read operations.</span></span>
2.  <span data-ttu-id="84ed5-127">Crea un objeto [**IPortableDeviceValues**](iportabledevicevalues.md) , que contendrá información como el tamaño y el formato de la imagen.</span><span class="sxs-lookup"><span data-stu-id="84ed5-127">It creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, which will contain information such as the image size and format.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(wszFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // CoCreate the IPortableDeviceValues to hold the resource attributes
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pResourceAttributes);
        if (SUCCEEDED(hr))
        {
            // Fill in the necessary information regarding this resource

            // Set the WPD_OBJECT_ID.  This informs the driver which object this request is intended for.
            hr = pResourceAttributes->SetStringValue(WPD_OBJECT_ID, wszSelection);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID when creating a resource, hr = 0x%lx\n",hr);
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetKeyValue(WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY, WPD_RESOURCE_CONTACT_PHOTO);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE by requesting the total size of the
            // data stream.
            if (SUCCEEDED(hr))
            {
                STATSTG statstg = {0};
                hr = pFileStream->Stat(&statstg, STATFLAG_NONAME);
                if (SUCCEEDED(hr))
                {
                    hr = pResourceAttributes->SetUnsignedLargeIntegerValue(WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, statstg.cbSize.QuadPart);
                    if (FAILED(hr))
                    {
                        printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to get file's total size, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF because we are
            // creating a contact photo resource with JPG image data.
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetGuidValue(WPD_RESOURCE_ATTRIBUTE_FORMAT, WPD_OBJECT_FORMAT_JFIF);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF, hr = 0x%lx\n",hr);
                }
            }
        }

    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",wszFilePath, hr);
    }
}
```



<span data-ttu-id="84ed5-128">Después de preparar los objetos IStream y [**IPortableDeviceValues**](iportabledevicevalues.md) para la operación de escritura, el ejemplo transfiere la imagen al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84ed5-128">After preparing the IStream and [**IPortableDeviceValues**](iportabledevicevalues.md) objects for the write operation, the sample transfers the image to the device.</span></span> <span data-ttu-id="84ed5-129">El ejemplo completa la transferencia en tres pasos, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="84ed5-129">The sample completes the transfer in three steps, as follows:</span></span>

1.  <span data-ttu-id="84ed5-130">Crea el recurso en el dispositivo mediante una llamada al método [**IPortableDeviceResources:: CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) .</span><span class="sxs-lookup"><span data-stu-id="84ed5-130">It creates the resource on the device by calling the [**IPortableDeviceResources::CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) method.</span></span>
2.  <span data-ttu-id="84ed5-131">Llama a una función auxiliar de StreamCopy para copiar la secuencia de origen en el flujo de destino.</span><span class="sxs-lookup"><span data-stu-id="84ed5-131">It calls a StreamCopy helper function to copy the source stream to the destination stream.</span></span>
3.  <span data-ttu-id="84ed5-132">Informa al controlador de dispositivo de que la transferencia se ha completado llamando al método IPortableDeviceDataStream:: commit.</span><span class="sxs-lookup"><span data-stu-id="84ed5-132">It informs the device driver that the transfer is complete by calling the IPortableDeviceDataStream::Commit method.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pResources->CreateResource(pResourceAttributes,    // Properties describing this resource
                                    &pResourceStream,       // Returned resource data stream (to transfer the data to)
                                    &cbOptimalTransferSize, // Returned optimal buffer size to use during transfer
                                    NULL);


    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pResourceStream,        // Destination (The resource to transfer to)
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
        hr = pResourceStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit resource to device, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="84ed5-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84ed5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84ed5-134">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="84ed5-134">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="84ed5-135">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="84ed5-135">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="84ed5-136">**Interfaz IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="84ed5-136">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[<span data-ttu-id="84ed5-137">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="84ed5-137">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="84ed5-138">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="84ed5-138">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



