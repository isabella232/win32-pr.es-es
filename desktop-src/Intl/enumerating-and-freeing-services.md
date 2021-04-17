---
description: Enumerar y liberar servicios
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Enumerar y liberar servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859abe590ccaf2f71df676d5989778d5b391be57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688343"
---
# <a name="enumerating-and-freeing-services"></a><span data-ttu-id="6632c-103">Enumerar y liberar servicios</span><span class="sxs-lookup"><span data-stu-id="6632c-103">Enumerating and Freeing Services</span></span>

<span data-ttu-id="6632c-104">La aplicación ELS llama a la función [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) para determinar los servicios que están disponibles en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6632c-104">The ELS application calls the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function to determine the services that are available on the operating system.</span></span> <span data-ttu-id="6632c-105">La función se puede utilizar para enumerar todos los servicios de ELS disponibles o para filtrar los servicios según los criterios de búsqueda proporcionados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6632c-105">The function can be used either to enumerate all available ELS services, or to filter the services based on application-provided search criteria.</span></span> <span data-ttu-id="6632c-106">Cuando ya no se necesitan servicios, la aplicación llama a [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span><span class="sxs-lookup"><span data-stu-id="6632c-106">When services are no longer needed, the application calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).</span></span>

## <a name="get-all-supported-services"></a><span data-ttu-id="6632c-107">Obtener todos los servicios admitidos</span><span class="sxs-lookup"><span data-stu-id="6632c-107">Get All Supported Services</span></span>

<span data-ttu-id="6632c-108">En este ejemplo de código se muestra el uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) y [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar y, a continuación, liberar todos los servicios disponibles en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6632c-108">This code example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all available services on the operating system.</span></span> <span data-ttu-id="6632c-109">Para ello, la aplicación pasa **null** para el parámetro *pOptions* de **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="6632c-109">To do this, the application passes **NULL** for the *pOptions* parameter of **MappingGetServices**.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    // Get all installed ELS services.
    Result = MappingGetServices(NULL, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="get-specific-services"></a><span data-ttu-id="6632c-110">Obtener servicios específicos</span><span class="sxs-lookup"><span data-stu-id="6632c-110">Get Specific Services</span></span>

<span data-ttu-id="6632c-111">En el ejemplo siguiente se muestra el uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) y [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar y, a continuación, liberar todos los servicios de la categoría "detección de idioma".</span><span class="sxs-lookup"><span data-stu-id="6632c-111">The next example illustrates the use of [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) and [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) to enumerate and then free all services of category "Language Detection".</span></span> <span data-ttu-id="6632c-112">Para obtener más información acerca de esta categoría de servicio, consulte [**Microsoft detección de idioma**](microsoft-language-detection.md).</span><span class="sxs-lookup"><span data-stu-id="6632c-112">For more information about this service category, see [**Microsoft Language Detection**](microsoft-language-detection.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <elscore.h>

int __cdecl main()
{
    MAPPING_ENUM_OPTIONS    EnumOptions;
    PMAPPING_SERVICE_INFO   prgServices = NULL;
    DWORD                   dwServicesCount = 0;
    HRESULT                 Result;
    DWORD                   i;

    ZeroMemory(&EnumOptions, sizeof (MAPPING_ENUM_OPTIONS));
    EnumOptions.Size = sizeof (MAPPING_ENUM_OPTIONS);

    // Use the Language Auto-Detection category to enumerate
    // all language detection services.
    EnumOptions.pszCategory = L"Language Detection";

    // Execute the enumeration:
    Result = MappingGetServices(&EnumOptions, &prgServices, &dwServicesCount);

    if (SUCCEEDED(Result))
    {
        for (i = 0; i < dwServicesCount; ++i)
        {
            // Do something with each service.
            // ... prgServices[i] ...
            printf_s("Service: %ws, category: %ws\n",
                prgServices[i].pszDescription, prgServices[i].pszCategory);
        }
        MappingFreeServices(prgServices);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="6632c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6632c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6632c-114">Uso de servicios lingüísticos extendidos</span><span class="sxs-lookup"><span data-stu-id="6632c-114">Using Extended Linguistic Services</span></span>](using-extended-linguistic-services.md)
</dt> <dt>

[<span data-ttu-id="6632c-115">**MappingFreeServices**</span><span class="sxs-lookup"><span data-stu-id="6632c-115">**MappingFreeServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[<span data-ttu-id="6632c-116">**MappingGetServices**</span><span class="sxs-lookup"><span data-stu-id="6632c-116">**MappingGetServices**</span></span>](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



