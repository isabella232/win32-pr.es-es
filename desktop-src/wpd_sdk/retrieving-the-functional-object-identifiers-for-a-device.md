---
description: Recuperación de los identificadores de objetos funcionales de un dispositivo
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Recuperación de los identificadores de objetos funcionales de un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716386"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a><span data-ttu-id="8ed4b-103">Recuperación de los identificadores de objetos funcionales de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="8ed4b-103">Retrieving the Functional Object Identifiers for a Device</span></span>

<span data-ttu-id="8ed4b-104">Como se indicó en el tema [recuperación de las categorías funcionales compatibles con un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) , los dispositivos portátiles de Windows pueden admitir una o varias categorías funcionales.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-104">As noted in the [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic, Windows Portable Devices may support one or more functional categories.</span></span> <span data-ttu-id="8ed4b-105">Cualquier categoría funcional determinada puede admitir uno o más objetos funcionales.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-105">Any given functional category may support one or more functional objects.</span></span> <span data-ttu-id="8ed4b-106">Por ejemplo, la categoría de almacenamiento puede admitir tres objetos de almacenamiento funcional, cada uno de los cuales se identifica mediante una cadena de identificador único.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-106">For example, the storage category may support three functional storage objects, each of which is identified by a unique identifier string.</span></span> <span data-ttu-id="8ed4b-107">Después, el primer objeto de almacenamiento se puede identificar mediante la cadena "Storage1", la segunda por la cadena "Storage2" y la tercera por la cadena "Storage3".</span><span class="sxs-lookup"><span data-stu-id="8ed4b-107">The first storage object may then be identified by the string "Storage1", the second by the string "Storage2", and the third by the string "Storage3".</span></span>

<span data-ttu-id="8ed4b-108">La función ListFunctionalObjects del módulo DeviceCapabilities. cpp muestra la recuperación de tipos de contenido para las categorías funcionales admitidas por un dispositivo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-108">The ListFunctionalObjects function in the DeviceCapabilities.cpp module demonstrates the retrieval of content types for the functional categories supported by a selected device.</span></span>

<span data-ttu-id="8ed4b-109">La aplicación puede recuperar las categorías funcionales admitidas por un dispositivo mediante las interfaces descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-109">Your application can retrieve the functional categories supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="8ed4b-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="8ed4b-110">Interface</span></span>                                                                                      | <span data-ttu-id="8ed4b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ed4b-111">Description</span></span>                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="8ed4b-112">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8ed4b-112">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="8ed4b-113">Proporciona acceso a los métodos de recuperación de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-113">Provides access to the functional-category retrieval methods.</span></span> |
| [<span data-ttu-id="8ed4b-114">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="8ed4b-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="8ed4b-115">Se utiliza para enumerar y almacenar datos de categoría funcional.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-115">Used to enumerate and store functional-category data.</span></span>         |



 

<span data-ttu-id="8ed4b-116">El código que se encuentra en la función ListFunctionalObjects es casi idéntico al código que se encuentra en la función ListFunctionalCategories.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-116">The code found in the ListFunctionalObjects function is almost identical to the code found in the ListFunctionalCategories function.</span></span> <span data-ttu-id="8ed4b-117">(Consulte el tema recuperación de las [categorías funcionales compatibles con un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md) ). La única diferencia es la llamada al método [**IPortableDeviceCapabilities:: GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , que aparece dentro del bucle que recorre en iteración las categorías funcionales.</span><span class="sxs-lookup"><span data-stu-id="8ed4b-117">(See the [Retrieving Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md) topic.) The one difference is the call to the [**IPortableDeviceCapabilities::GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) method, which appears within the loop that iterates through the functional categories.</span></span>


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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



## <a name="related-topics"></a><span data-ttu-id="8ed4b-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ed4b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ed4b-119">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="8ed4b-119">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="8ed4b-120">**Interfaz IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8ed4b-120">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="8ed4b-121">**Interfaz IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="8ed4b-121">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="8ed4b-122">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="8ed4b-122">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



