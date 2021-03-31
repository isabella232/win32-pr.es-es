---
description: Recuperación de las categorías funcionales admitidas por un dispositivo
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Recuperación de las categorías funcionales admitidas por un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911361"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a><span data-ttu-id="77038-103">Recuperación de las categorías funcionales admitidas por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="77038-103">Retrieving the Functional Categories Supported by a Device</span></span>

<span data-ttu-id="77038-104">Los dispositivos portátiles de Windows pueden admitir una o varias categorías funcionales.</span><span class="sxs-lookup"><span data-stu-id="77038-104">Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="77038-105">Estas categorías se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="77038-105">These categories are described in the following table.</span></span>



| <span data-ttu-id="77038-106">Category</span><span class="sxs-lookup"><span data-stu-id="77038-106">Category</span></span>                    | <span data-ttu-id="77038-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="77038-107">Description</span></span>                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77038-108">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="77038-108">Audio capture</span></span>               | <span data-ttu-id="77038-109">El dispositivo se puede usar para grabar audio.</span><span class="sxs-lookup"><span data-stu-id="77038-109">The device can be used to record audio.</span></span>                                              |
| <span data-ttu-id="77038-110">Información de representación</span><span class="sxs-lookup"><span data-stu-id="77038-110">Rendering information</span></span>       | <span data-ttu-id="77038-111">El dispositivo proporciona datos que describen los archivos multimedia que es capaz de representar.</span><span class="sxs-lookup"><span data-stu-id="77038-111">The device provides data describing the media files that it is capable of rendering.</span></span> |
| <span data-ttu-id="77038-112">Servicio de mensajes cortos (SMS)</span><span class="sxs-lookup"><span data-stu-id="77038-112">Short message service (SMS)</span></span> | <span data-ttu-id="77038-113">El dispositivo admite la mensajería de texto.</span><span class="sxs-lookup"><span data-stu-id="77038-113">The device supports text messaging.</span></span>                                                  |
| <span data-ttu-id="77038-114">Captura de imagen fija</span><span class="sxs-lookup"><span data-stu-id="77038-114">Still image capture</span></span>         | <span data-ttu-id="77038-115">El dispositivo se puede usar para capturar imágenes fijas.</span><span class="sxs-lookup"><span data-stu-id="77038-115">The device can be used to capture still images.</span></span>                                      |
| <span data-ttu-id="77038-116">Almacenamiento</span><span class="sxs-lookup"><span data-stu-id="77038-116">Storage</span></span>                     | <span data-ttu-id="77038-117">El dispositivo se puede usar para almacenar archivos.</span><span class="sxs-lookup"><span data-stu-id="77038-117">The device can be used to store files.</span></span>                                               |



 

<span data-ttu-id="77038-118">La función ListFunctionalCategories del módulo DeviceCapabilities. cpp muestra la recuperación de las categorías funcionales de un dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="77038-118">The ListFunctionalCategories function in the DeviceCapabilities.cpp module demonstrates the retrieval of functional categories for a selected device.</span></span>

<span data-ttu-id="77038-119">La aplicación puede recuperar las categorías funcionales admitidas por un dispositivo mediante el uso de las interfaces que se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="77038-119">Your application can retrieve the functional categories supported by a device by using the interfaces described in the following table.</span></span>



| <span data-ttu-id="77038-120">Interfaz</span><span class="sxs-lookup"><span data-stu-id="77038-120">Interface</span></span>                                                                                      | <span data-ttu-id="77038-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="77038-121">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="77038-122">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="77038-122">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="77038-123">Proporciona acceso a los métodos de recuperación de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="77038-123">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="77038-124">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="77038-124">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="77038-125">Se utiliza para enumerar y almacenar datos de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="77038-125">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="77038-126">La primera tarea que se lleva a cabo mediante la aplicación de ejemplo es la recuperación de un objeto [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , que se usa para recuperar las categorías funcionales en el dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="77038-126">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the functional categories on the selected device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="77038-127">Las categorías recuperadas se almacenan en un objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="77038-127">The retrieved categories are stored in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object.</span></span>

<span data-ttu-id="77038-128">El paso siguiente es la enumeración y la visualización de las categorías admitidas.</span><span class="sxs-lookup"><span data-stu-id="77038-128">The next step is the enumeration and display of the supported categories.</span></span> <span data-ttu-id="77038-129">El primer paso que realiza la aplicación de ejemplo es recuperar el recuento de las categorías admitidas.</span><span class="sxs-lookup"><span data-stu-id="77038-129">The first step that the sample application accomplishes is to retrieve the count of supported categories.</span></span> <span data-ttu-id="77038-130">A continuación, usa este recuento para recorrer en iteración el objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contiene las categorías admitidas.</span><span class="sxs-lookup"><span data-stu-id="77038-130">It then uses this count to iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that contains the supported categories.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="77038-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77038-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77038-132">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="77038-132">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="77038-133">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="77038-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="77038-134">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="77038-134">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="77038-135">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="77038-135">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



