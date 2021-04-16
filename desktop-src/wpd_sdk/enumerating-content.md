---
description: Enumerar contenido
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Enumerar contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666479"
---
# <a name="enumerating-content"></a><span data-ttu-id="d47c8-103">Enumerar contenido</span><span class="sxs-lookup"><span data-stu-id="d47c8-103">Enumerating Content</span></span>

<span data-ttu-id="d47c8-104">El contenido de un dispositivo (ya sea una carpeta, una libreta de teléfonos, un vídeo o una imagen fija) se denomina objeto en la API de WPD.</span><span class="sxs-lookup"><span data-stu-id="d47c8-104">The content on a device (whether that content is a folder, a phone book, a video, or a still image) is called an object in the WPD API.</span></span> <span data-ttu-id="d47c8-105">Los identificadores de objeto hacen referencia a estos objetos y se describen mediante propiedades.</span><span class="sxs-lookup"><span data-stu-id="d47c8-105">These objects are referenced by object identifiers and described by properties.</span></span> <span data-ttu-id="d47c8-106">Puede enumerar los objetos en un dispositivo mediante la llamada a métodos en la [**interfaz IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), la [**interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)y la [**interfaz IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="d47c8-106">You can enumerate the objects on a device by calling methods in the [**IPortableDevice interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), the [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent), and the [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span>

<span data-ttu-id="d47c8-107">En la aplicación de ejemplo se muestra la enumeración de contenido en la función EnumerateAllContent que se encuentra en el módulo ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="d47c8-107">The sample application demonstrates content enumeration in the EnumerateAllContent function that is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="d47c8-108">Esta función, a su vez, llama a una función RecursiveEnumerate que recorre la jerarquía de objetos encontrados en el dispositivo seleccionado y devuelve un identificador de objeto para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="d47c8-108">This function, in turn, calls a RecursiveEnumerate function that walks the hierarchy of objects found on the selected device and returns an object identifier for each object.</span></span>

<span data-ttu-id="d47c8-109">Como se indicó, la función RecursiveEnumerate recupera un identificador de objeto para cada objeto encontrado en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d47c8-109">As noted, the RecursiveEnumerate function retrieves an object identifier for each object found on the device.</span></span> <span data-ttu-id="d47c8-110">El identificador de objeto es un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="d47c8-110">The object identifier is a string value.</span></span> <span data-ttu-id="d47c8-111">Una vez que la aplicación recupera este identificador, puede obtener información más descriptiva del objeto (por ejemplo, el nombre del objeto, el identificador del elemento primario del objeto, etc.).</span><span class="sxs-lookup"><span data-stu-id="d47c8-111">Once your application retrieves this identifier, it can obtain more descriptive object information (such as the object's name, the identifier for the object's parent, and so on).</span></span> <span data-ttu-id="d47c8-112">Esta información descriptiva se conoce como propiedades del objeto (o metadatos).</span><span class="sxs-lookup"><span data-stu-id="d47c8-112">This descriptive information is referred to as object properties (or metadata).</span></span> <span data-ttu-id="d47c8-113">La aplicación puede recuperar estas propiedades llamando a los miembros de la [**interfaz IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span><span class="sxs-lookup"><span data-stu-id="d47c8-113">Your application can retrieve these properties by calling members of the [**IPortableDeviceProperties interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).</span></span>

<span data-ttu-id="d47c8-114">La función EnumerateAllContent comienza mediante la recuperación de un puntero a una [**interfaz IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span><span class="sxs-lookup"><span data-stu-id="d47c8-114">The EnumerateAllContent function begins by retrieving a pointer to an [**IPortableDeviceContent interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent).</span></span> <span data-ttu-id="d47c8-115">Recupera este puntero llamando al método [**IPortableDevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="d47c8-115">It retrieves this pointer by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="d47c8-116">Una vez que recupera el puntero a la interfaz IPortableDeviceContent, la función EnumerateAllContent llama a la función RecursiveEnumerate, que recorre la jerarquía de objetos encontrados en el dispositivo dado y devuelve un identificador de objeto para cada uno.</span><span class="sxs-lookup"><span data-stu-id="d47c8-116">Once it retrieves the pointer to the IPortableDeviceContent interface, the EnumerateAllContent function calls the RecursiveEnumerate function, which walks the hierarchy of objects found on the given device and returns an object identifier for each.</span></span>

<span data-ttu-id="d47c8-117">La función RecursiveEnumerate comienza mediante la recuperación de un puntero a una [**interfaz IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span><span class="sxs-lookup"><span data-stu-id="d47c8-117">The RecursiveEnumerate function begins by retrieving a pointer to an [**IEnumPortableDeviceObjectIDs interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).</span></span> <span data-ttu-id="d47c8-118">Esta interfaz expone los métodos que utiliza una aplicación para navegar por la lista de objetos encontrados en un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="d47c8-118">This interface exposes the methods that an application uses to navigate the list of objects found on a given device.</span></span>

<span data-ttu-id="d47c8-119">En este ejemplo, la función RecursiveEnumerate llama al método [**IEnumPortableDeviceObjectIDs:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) para atravesar la lista de objetos.</span><span class="sxs-lookup"><span data-stu-id="d47c8-119">In this sample, the RecursiveEnumerate function calls the [**IEnumPortableDeviceObjectIDs::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method to traverse the list of objects.</span></span>

<span data-ttu-id="d47c8-120">Cada llamada al método [**IEnumPortableDeviceObjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) solicita un lote de 10 identificadores.</span><span class="sxs-lookup"><span data-stu-id="d47c8-120">Each call to the [**IEnumPortableDeviceObjects::Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) method requests a batch of 10 identifiers.</span></span> <span data-ttu-id="d47c8-121">(El valor se especifica mediante el parámetro NUM \_ OBJETOS \_ para \_ solicitar una constante que se proporciona como primer argumento).</span><span class="sxs-lookup"><span data-stu-id="d47c8-121">(This value is specified by the NUM\_OBJECTS\_TO\_REQUEST constant that is supplied as the first argument.)</span></span>


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="d47c8-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d47c8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d47c8-123">**Interfaz IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="d47c8-123">**IEnumPortableDeviceObjectIDs Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="d47c8-124">**Interfaz IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="d47c8-124">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="d47c8-125">**Interfaz IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="d47c8-125">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="d47c8-126">**Interfaz IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="d47c8-126">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="d47c8-127">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="d47c8-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



