---
description: Recuperación de los tipos de contenido admitidos por un dispositivo
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Recuperación de los tipos de contenido admitidos por un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716573"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a><span data-ttu-id="431e9-103">Recuperación de los tipos de contenido admitidos por un dispositivo</span><span class="sxs-lookup"><span data-stu-id="431e9-103">Retrieving the Content Types Supported by a Device</span></span>

<span data-ttu-id="431e9-104">Como se indicó en el tema [recuperación de las categorías funcionales compatibles con un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , los dispositivos portátiles de Windows pueden admitir una o varias categorías funcionales.</span><span class="sxs-lookup"><span data-stu-id="431e9-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="431e9-105">Cualquier categoría funcional determinada puede admitir uno o varios tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="431e9-105">Any given functional category may support one or more content types.</span></span> <span data-ttu-id="431e9-106">Por ejemplo, la categoría de almacenamiento puede admitir tipos de contenido de carpeta, audio e imagen.</span><span class="sxs-lookup"><span data-stu-id="431e9-106">For example, the storage category may support content types of folder, audio, and image.</span></span>

<span data-ttu-id="431e9-107">Para obtener una descripción de los tipos de contenido admitidos por WPD, consulte el tema [**tipo de contenido de WPD \_ \_ \_ All**](wpd-content-type-all.md) .</span><span class="sxs-lookup"><span data-stu-id="431e9-107">For a description of the content types supported by WPD, see the [**WPD\_CONTENT\_TYPE\_ALL**](wpd-content-type-all.md) topic.</span></span>

<span data-ttu-id="431e9-108">La función ListSupportedContentTypes del módulo DeviceCapabilities. cpp muestra la recuperación de tipos de contenido para las categorías funcionales admitidas por un dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="431e9-108">The ListSupportedContentTypes function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="431e9-109">La aplicación puede recuperar las categorías funcionales admitidas por un dispositivo mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="431e9-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="431e9-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="431e9-110">Interface</span></span>                                                                                      | <span data-ttu-id="431e9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="431e9-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="431e9-112">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="431e9-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="431e9-113">Proporciona acceso a los métodos de recuperación de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="431e9-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="431e9-114">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="431e9-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="431e9-115">Se utiliza para enumerar y almacenar datos de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="431e9-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="431e9-116">El código que se encuentra en la función ListSupportedContentTypes es casi idéntico al código que se encuentra en la función ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="431e9-116">The code found in the ListSupportedContentTypes function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="431e9-117">(Consulte el tema recuperación de las [categorías funcionales compatibles con un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) ). La única diferencia es la llamada al método [**IPortableDeviceCapabilities:: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , que aparece dentro del bucle que recorre en iteración las categorías funcionales.</span><span class="sxs-lookup"><span data-stu-id="431e9-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) method, which appears within the loop that iterates through the functional categories.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="431e9-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="431e9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431e9-119">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="431e9-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="431e9-120">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="431e9-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="431e9-121">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="431e9-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="431e9-122">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="431e9-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



