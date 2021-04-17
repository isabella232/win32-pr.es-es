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
# <a name="enumerating-and-freeing-services"></a>Enumerar y liberar servicios

La aplicación ELS llama a la función [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) para determinar los servicios que están disponibles en el sistema operativo. La función se puede utilizar para enumerar todos los servicios de ELS disponibles o para filtrar los servicios según los criterios de búsqueda proporcionados por la aplicación. Cuando ya no se necesitan servicios, la aplicación llama a [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices).

## <a name="get-all-supported-services"></a>Obtener todos los servicios admitidos

En este ejemplo de código se muestra el uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) y [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar y, a continuación, liberar todos los servicios disponibles en el sistema operativo. Para ello, la aplicación pasa **null** para el parámetro *pOptions* de **MappingGetServices**.


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



## <a name="get-specific-services"></a>Obtener servicios específicos

En el ejemplo siguiente se muestra el uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) y [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar y, a continuación, liberar todos los servicios de la categoría "detección de idioma". Para obtener más información acerca de esta categoría de servicio, consulte [**Microsoft detección de idioma**](microsoft-language-detection.md).


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de servicios lingüísticos extendidos](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



