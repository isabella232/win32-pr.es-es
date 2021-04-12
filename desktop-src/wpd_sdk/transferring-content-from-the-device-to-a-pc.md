---
description: Transferencia de contenido desde el dispositivo a un equipo
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: Transferencia de contenido desde el dispositivo a un equipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de06861ba74b4b7883c8d96e25cebe3fbb64e21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278310"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a><span data-ttu-id="0bf68-103">Transferencia de contenido desde el dispositivo a un equipo</span><span class="sxs-lookup"><span data-stu-id="0bf68-103">Transferring Content from the Device to a PC</span></span>

<span data-ttu-id="0bf68-104">Una operación común que realiza una aplicación de WPD es la transferencia de contenido desde un dispositivo conectado al equipo.</span><span class="sxs-lookup"><span data-stu-id="0bf68-104">One common operation accomplished by a WPD application is the transfer of content from a connected device to the PC.</span></span>

<span data-ttu-id="0bf68-105">Las transferencias de contenido se realizan mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0bf68-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="0bf68-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="0bf68-106">Interface</span></span>                                                                | <span data-ttu-id="0bf68-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bf68-107">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="0bf68-108">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="0bf68-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="0bf68-109">Proporciona acceso a la interfaz **IPortableDeviceProperties** .</span><span class="sxs-lookup"><span data-stu-id="0bf68-109">Provides access to the **IPortableDeviceProperties** interface.</span></span> |
| [<span data-ttu-id="0bf68-110">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="0bf68-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="0bf68-111">Proporciona acceso a los métodos específicos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0bf68-111">Provides access to property-specific methods.</span></span>                   |
| [<span data-ttu-id="0bf68-112">**Interfaz IPortableDeviceResources**</span><span class="sxs-lookup"><span data-stu-id="0bf68-112">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | <span data-ttu-id="0bf68-113">Se usa para almacenar las claves de propiedad para el perfil especificado.</span><span class="sxs-lookup"><span data-stu-id="0bf68-113">Used to store the property keys for the given profile.</span></span>          |
| <span data-ttu-id="0bf68-114">IStream (interfaz)</span><span class="sxs-lookup"><span data-stu-id="0bf68-114">IStream Interface</span></span>                                                        | <span data-ttu-id="0bf68-115">Se usa para leer y escribir los datos.</span><span class="sxs-lookup"><span data-stu-id="0bf68-115">Used to read and write the data.</span></span>                                |



 

<span data-ttu-id="0bf68-116">La `TransferContentFromDevice` función del módulo ContentTransfer. cpp de la aplicación de ejemplo muestra cómo una aplicación podría transferir información de contacto desde un dispositivo conectado a un equipo.</span><span class="sxs-lookup"><span data-stu-id="0bf68-116">The `TransferContentFromDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a connected device to a PC.</span></span>

<span data-ttu-id="0bf68-117">La primera tarea que se realiza mediante la `TransferContentFromDevice` función es solicitar al usuario que escriba un identificador de objeto para el objeto primario en el dispositivo (con el que se transferirá el contenido).</span><span class="sxs-lookup"><span data-stu-id="0bf68-117">The first task accomplished by the `TransferContentFromDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                            hr                   = S_OK;
WCHAR                              szSelection[81]      = {0};
CComPtr<IPortableDeviceContent>    pContent;
CComPtr<IPortableDeviceResources>  pResources;
CComPtr<IPortableDeviceProperties> pProperties;
CComPtr<IStream>                   pObjectDataStream;
CComPtr<IStream>                   pFinalFileStream;
DWORD                              cbOptimalTransferSize = 0;
CAtlStringW                        strOriginalFileName;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Prompt user to enter an object identifier on the device to transfer.
printf("Enter the identifer of the object you wish to transfer.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="0bf68-118">El paso siguiente es la recuperación de un objeto **IPortableDeviceContent** que el ejemplo utiliza para tener acceso a los métodos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="0bf68-118">The next step is the retrieval of an **IPortableDeviceContent** object that the sample uses to access the content-specific methods.</span></span>


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



<span data-ttu-id="0bf68-119">El paso siguiente es la recuperación de un objeto **IPortableDeviceResources** que el ejemplo utiliza para tener acceso a los métodos específicos del recurso.</span><span class="sxs-lookup"><span data-stu-id="0bf68-119">The next step is the retrieval of an **IPortableDeviceResources** object that the sample uses to access the resource-specific methods.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="0bf68-120">El paso siguiente es la recuperación de un objeto IStream que el ejemplo utiliza para leer los datos que se transfieren desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bf68-120">The next step is the retrieval of an IStream object that the sample uses to read the data it is transferring from the device.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pResources->GetStream(szSelection,             // Identifier of the object we want to transfer
                               WPD_RESOURCE_DEFAULT,    // We are transferring the default resource (which is the entire object's data)
                               STGM_READ,               // Opening a stream in READ mode, because we are reading data from the device.
                               &cbOptimalTransferSize,  // Driver supplied optimal transfer size
                               &pObjectDataStream);
    if (FAILED(hr))
    {
        printf("! Failed to get IStream (representing object data on the device) from IPortableDeviceResources, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="0bf68-121">El siguiente paso es la recuperación del nombre de archivo del objeto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0bf68-121">The next step is the retrieval of the object's file name on the device.</span></span> <span data-ttu-id="0bf68-122">Esta cadena se usa para crear el nombre de archivo correspondiente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="0bf68-122">This string is used to create the corresponding file name on the PC.</span></span> <span data-ttu-id="0bf68-123">Si el objeto no tiene un nombre de archivo en el dispositivo, el identificador del objeto se convierte en una cadena y se usa para crear el nombre de archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="0bf68-123">If the object does not have a file name on the device, the object's identifier is converted to a string and used to create the destination file name.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (SUCCEEDED(hr))
    {
        hr = GetStringValue(pProperties,
                            szSelection,
                            WPD_OBJECT_ORIGINAL_FILE_NAME,
                            strOriginalFileName);
        if (FAILED(hr))
        {
            printf("! Failed to read WPD_OBJECT_ORIGINAL_FILE_NAME on object '%ws', hr = 0x%lx\n", szSelection, hr);
            strOriginalFileName.Format(L"%ws.data", szSelection);
            printf("* Creating a filename '%ws' as a default.\n", (PWSTR)strOriginalFileName.GetString());
            // Set the HRESULT to S_OK, so we can continue with our newly generated
            // temporary file name.
            hr = S_OK;
        }
    }
    else
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="0bf68-124">Después de esto, el ejemplo crea un objeto IStream de destino.</span><span class="sxs-lookup"><span data-stu-id="0bf68-124">After this, the sample creates a destination IStream object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = SHCreateStreamOnFile(strOriginalFileName, STGM_CREATE|STGM_WRITE, &pFinalFileStream);
    if (FAILED(hr))
    {
        printf("! Failed to create a temporary file named (%ws) to transfer object (%ws), hr = 0x%lx\n",(PWSTR)strOriginalFileName.GetString(), szSelection, hr);
    }
}
```



<span data-ttu-id="0bf68-125">Por último, el objeto IStream de origen se copia en el destino del equipo.</span><span class="sxs-lookup"><span data-stu-id="0bf68-125">Finally, the source IStream object is copied to the destination on the PC.</span></span>


```C++
if (SUCCEEDED(hr))
{
    DWORD cbTotalBytesWritten = 0;

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    hr = StreamCopy(pFinalFileStream,       // Destination (The Final File to transfer to)
                    pObjectDataStream,      // Source (The Object's data to transfer from)
                    cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                    &cbTotalBytesWritten);  // The total number of bytes transferred from device to the finished file
    if (FAILED(hr))
    {
        printf("! Failed to transfer object from device, hr = 0x%lx\n",hr);
    }
    else
    {
        printf("* Transferred object '%ws' to '%ws'.\n", szSelection, (PWSTR)strOriginalFileName.GetString());
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0bf68-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0bf68-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf68-127">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="0bf68-127">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="0bf68-128">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="0bf68-128">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="0bf68-129">**Interfaz IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="0bf68-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0bf68-130">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="0bf68-130">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



