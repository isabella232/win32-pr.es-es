---
description: Enumerar y liberar servicios
ms.assetid: 526e51c7-9ff2-4590-b092-172f4942ce8e
title: Enumerar y liberar servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6472851fbf5f7f84a499d2e9e04804279d397f31452d9617a8868e05cb8ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086615"
---
# <a name="enumerating-and-freeing-services"></a>Enumerar y liberar servicios

La aplicación ELS llama a [**la función MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) para determinar los servicios que están disponibles en el sistema operativo. La función se puede usar para enumerar todos los servicios ELS disponibles o para filtrar los servicios en función de los criterios de búsqueda proporcionados por la aplicación. Cuando ya no se necesitan servicios, la aplicación llama [**a MappingFreeServices.**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)

## <a name="get-all-supported-services"></a>Obtener todos los servicios admitidos

En este ejemplo de código se muestra el uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) y [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar y, a continuación, liberar todos los servicios disponibles en el sistema operativo. Para ello, la aplicación pasa **NULL para** el *parámetro pOptions* **de MappingGetServices.**


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

En el ejemplo siguiente se muestra el uso de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) y [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) para enumerar y, a continuación, liberar todos los servicios de la categoría "Detección de idioma". Para obtener más información sobre esta categoría de servicio, vea [**Microsoft Detección de idioma**](microsoft-language-detection.md).


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

[Uso de Servicios lingüísticos extendidos](using-extended-linguistic-services.md)
</dt> <dt>

[**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)
</dt> <dt>

[**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)
</dt> </dl>

 

 



