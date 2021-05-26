---
description: Enumeración del contenido del servicio
ms.assetid: 4af4201c-d3f6-4630-91ec-6509c51871a5
title: Enumeración del contenido del servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b701bdab867e96bc9658e2624ea18aa65dfc33
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424255"
---
# <a name="enumerating-service-content"></a><span data-ttu-id="4294a-103">Enumeración del contenido del servicio</span><span class="sxs-lookup"><span data-stu-id="4294a-103">Enumerating Service Content</span></span>

<span data-ttu-id="4294a-104">Una vez que la aplicación abre un servicio, puede empezar a realizar operaciones relacionadas con el servicio.</span><span class="sxs-lookup"><span data-stu-id="4294a-104">After your application opens a service, it can begin performing service-related operations.</span></span> <span data-ttu-id="4294a-105">En el caso de la aplicación WpdServicesApiSample, una de estas operaciones es la enumeración de contenido para un servicio Contacts determinado.</span><span class="sxs-lookup"><span data-stu-id="4294a-105">In the case of the WpdServicesApiSample application, one of these operations is the enumeration of content for a given Contacts service.</span></span> <span data-ttu-id="4294a-106">En la tabla siguiente se describen las interfaces usadas.</span><span class="sxs-lookup"><span data-stu-id="4294a-106">The following table describes the interfaces used.</span></span>



| <span data-ttu-id="4294a-107">Interfaz</span><span class="sxs-lookup"><span data-stu-id="4294a-107">Interface</span></span>                                                            | <span data-ttu-id="4294a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4294a-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4294a-109">**IPortableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="4294a-109">**IPortableDeviceService**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | <span data-ttu-id="4294a-110">Se usa para recuperar la interfaz IPortableDeviceContent2 para acceder al contenido del servicio.</span><span class="sxs-lookup"><span data-stu-id="4294a-110">Used to retrieve the IPortableDeviceContent2 interface to access content on the service.</span></span>         |
| [<span data-ttu-id="4294a-111">**IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="4294a-111">**IPortableDeviceContent2**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | <span data-ttu-id="4294a-112">Se usa para recuperar la interfaz IEnumPortableDeviceObjectIDs para enumerar objetos en el servicio.</span><span class="sxs-lookup"><span data-stu-id="4294a-112">Used to retrieve the IEnumPortableDeviceObjectIDs interface to enumerate objects on the service.</span></span> |
| [<span data-ttu-id="4294a-113">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="4294a-113">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids) | <span data-ttu-id="4294a-114">Se usa para enumerar objetos en el servicio.</span><span class="sxs-lookup"><span data-stu-id="4294a-114">Used to enumerate objects on the service.</span></span>                                                        |



 

<span data-ttu-id="4294a-115">El código de enumeración de contenido se encuentra en el módulo ContentEnumeration.cpp.</span><span class="sxs-lookup"><span data-stu-id="4294a-115">The content enumeration code is found in the ContentEnumeration.cpp module.</span></span> <span data-ttu-id="4294a-116">Este código reside en los métodos **EnumerateAllContent** y **RecursiveEnumerate.**</span><span class="sxs-lookup"><span data-stu-id="4294a-116">This code resides in the **EnumerateAllContent** and the **RecursiveEnumerate** methods.</span></span> <span data-ttu-id="4294a-117">El método anterior llama a la última.</span><span class="sxs-lookup"><span data-stu-id="4294a-117">The former method calls the latter.</span></span>

<span data-ttu-id="4294a-118">El **método EnumerateContent** toma un puntero a [**un objeto IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) como su único parámetro.</span><span class="sxs-lookup"><span data-stu-id="4294a-118">The **EnumerateContent** method takes a pointer to an [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) object as its one parameter.</span></span> <span data-ttu-id="4294a-119">Este objeto corresponde a un servicio que la aplicación abrió anteriormente cuando llamó al [**método IPortableDeviceService::Open.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open)</span><span class="sxs-lookup"><span data-stu-id="4294a-119">This object corresponds to a service that the application opened earlier when it called the [**IPortableDeviceService::Open**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open) method.</span></span>

<span data-ttu-id="4294a-120">El **método EnumerateContent** crea un objeto [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) y pasa este objeto al [**método IPortableDeviceService::Content.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content)</span><span class="sxs-lookup"><span data-stu-id="4294a-120">The **EnumerateContent** method creates an [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) object and passes this object to the [**IPortableDeviceService::Content**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-content) method.</span></span> <span data-ttu-id="4294a-121">Este método, a su vez, recupera el contenido en el nivel raíz del servicio y, a continuación, comienza de forma recursiva a recuperar el contenido encontrado debajo de la raíz.</span><span class="sxs-lookup"><span data-stu-id="4294a-121">This method, in turn, retrieves the content at the root level of the service, and then recursively begins to retrieve content found beneath the root.</span></span>

<span data-ttu-id="4294a-122">El código siguiente corresponde al **método EnumerateContent.**</span><span class="sxs-lookup"><span data-stu-id="4294a-122">The following code corresponds to the **EnumerateContent** method.</span></span>


```C++
// Enumerate all content on the service starting with the
// "DEVICE" object
void EnumerateAllContent(
    IPortableDeviceService* pService)
{
    HRESULT                          hr = S_OK;
    CComPtr<IPortableDeviceContent2> pContent;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    hr = pService->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



<span data-ttu-id="4294a-123">El código siguiente corresponde al **método RecursiveEnumerate.**</span><span class="sxs-lookup"><span data-stu-id="4294a-123">The following code corresponds to the **RecursiveEnumerate** method.</span></span> <span data-ttu-id="4294a-124">El método RecursiveEnumerate crea una instancia de una interfaz **IEnumPortableDeviceObjectIDs** para el objeto primario proporcionado y llama a **IEnumPortableDeviceObjectIDs::Next**, recuperando un lote de objetos secundarios inmediatos.</span><span class="sxs-lookup"><span data-stu-id="4294a-124">The RecursiveEnumerate method instantiates an **IEnumPortableDeviceObjectIDs** interface for the supplied parent object, and calls **IEnumPortableDeviceObjectIDs::Next**, retrieving a batch of immediate child objects.</span></span> <span data-ttu-id="4294a-125">Para cada objeto secundario, se llama de nuevo a RecursiveEnumerate para devolver sus objetos secundarios descendientes, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4294a-125">For each child object, RecursiveEnumerate is called again to return its descendent child objects, and so on.</span></span>


```C++
// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                   pszObjectID,
    IPortableDeviceContent2* pContent)
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
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent2, hr = 0x%lx\n",hr);
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



## <a name="related-topics"></a><span data-ttu-id="4294a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4294a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4294a-127">**IEnumPortableDeviceObjectIDs**</span><span class="sxs-lookup"><span data-stu-id="4294a-127">**IEnumPortableDeviceObjectIDs**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[<span data-ttu-id="4294a-128">**Interfaz IPortableDeviceContent2**</span><span class="sxs-lookup"><span data-stu-id="4294a-128">**IPortableDeviceContent2 Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[<span data-ttu-id="4294a-129">**IPortableDeviceService (interfaz)**</span><span class="sxs-lookup"><span data-stu-id="4294a-129">**IPortableDeviceService Interface**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[<span data-ttu-id="4294a-130">Abrir un servicio</span><span class="sxs-lookup"><span data-stu-id="4294a-130">Opening a Service</span></span>](opening-a-service.md)
</dt> <dt>

[<span data-ttu-id="4294a-131">WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="4294a-131">WpdServicesApiSample</span></span>](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



