---
description: Diseño de las claves del registro
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Diseño de las claves del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677035"
---
# <a name="layout-of-the-registry-keys"></a><span data-ttu-id="6d9e3-103">Diseño de las claves del registro</span><span class="sxs-lookup"><span data-stu-id="6d9e3-103">Layout of the Registry Keys</span></span>

<span data-ttu-id="6d9e3-104">Los filtros de DirectShow se registran en dos lugares:</span><span class="sxs-lookup"><span data-stu-id="6d9e3-104">DirectShow filters are registered in two places:</span></span>

-   <span data-ttu-id="6d9e3-105">El archivo DLL que contiene el filtro se registra como el servidor COM del filtro.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-105">The DLL that contains the filter is registered as the filter's COM server.</span></span> <span data-ttu-id="6d9e3-106">Cuando una aplicación llama a **CoCreateInstance** para crear el filtro, la biblioteca com de Microsoft Windows usa esta entrada del registro para buscar el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-106">When an application calls **CoCreateInstance** to create the filter, the Microsoft Windows COM library uses this registry entry to locate the DLL.</span></span>
-   <span data-ttu-id="6d9e3-107">Se puede registrar información adicional sobre el filtro dentro de una categoría de filtro.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-107">Additional information about the filter can be registered within a filter category.</span></span> <span data-ttu-id="6d9e3-108">Esta información permite que el [enumerador de dispositivos del sistema](system-device-enumerator.md) y el [asignador de filtros](filter-mapper.md) busquen el filtro.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-108">This information enables the [System Device Enumerator](system-device-enumerator.md) and the [Filter Mapper](filter-mapper.md) to locate the filter.</span></span>

<span data-ttu-id="6d9e3-109">No es necesario que los filtros registren la información de filtro adicional.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-109">Filters are not required to register the additional filter information.</span></span> <span data-ttu-id="6d9e3-110">Siempre que el archivo DLL esté registrado como el servidor COM, una aplicación puede crear el filtro y agregarlo a un gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-110">As long as the DLL is registered as the COM server, an application can create the filter and add it to a filter graph.</span></span> <span data-ttu-id="6d9e3-111">Sin embargo, si desea que el filtro sea reconocible por el enumerador de dispositivos del sistema o por el asignador de filtros, debe registrar la información adicional.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-111">However, if you want your filter to be discoverable by the System Device Enumerator or the Filter Mapper, you must register the additional information.</span></span>

<span data-ttu-id="6d9e3-112">La entrada del registro para el archivo DLL tiene las claves siguientes:</span><span class="sxs-lookup"><span data-stu-id="6d9e3-112">The registry entry for the DLL has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



<span data-ttu-id="6d9e3-113">La entrada del registro para la información de filtro tiene las claves siguientes:</span><span class="sxs-lookup"><span data-stu-id="6d9e3-113">The registry entry for the filter information has the following keys:</span></span>


```
HKEY_CLASSES_ROOT
    CLSID
        Category
            Instance
                Filter CLSID
                    REG_SZ: CLSID = Filter CLSID
                    REG_BINARY: FilterData = Filter information
                    REG_SZ: FriendlyName = Friendly name
```




```
Category
```



<span data-ttu-id="6d9e3-114">es el GUID de una categoría de filtro.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-114">is the GUID of a filter category.</span></span> <span data-ttu-id="6d9e3-115">(Consulte [categorías de filtro](filter-categories.md)). La información del filtro se empaqueta en un formato binario.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-115">(See [Filter Categories](filter-categories.md).) The filter information is packed into a binary format.</span></span> <span data-ttu-id="6d9e3-116">La interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) desempaqueta estos datos cuando busca un filtro en el registro.</span><span class="sxs-lookup"><span data-stu-id="6d9e3-116">The [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface unpacks this data when it searches the registry for a filter.</span></span>

<span data-ttu-id="6d9e3-117">Todos los GUID de categoría de filtro se enumeran en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="6d9e3-117">All of the filter category GUIDs are listed in the registry under the following key:</span></span>


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



