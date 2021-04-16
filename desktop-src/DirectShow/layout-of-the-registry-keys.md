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
# <a name="layout-of-the-registry-keys"></a>Diseño de las claves del registro

Los filtros de DirectShow se registran en dos lugares:

-   El archivo DLL que contiene el filtro se registra como el servidor COM del filtro. Cuando una aplicación llama a **CoCreateInstance** para crear el filtro, la biblioteca com de Microsoft Windows usa esta entrada del registro para buscar el archivo dll.
-   Se puede registrar información adicional sobre el filtro dentro de una categoría de filtro. Esta información permite que el [enumerador de dispositivos del sistema](system-device-enumerator.md) y el [asignador de filtros](filter-mapper.md) busquen el filtro.

No es necesario que los filtros registren la información de filtro adicional. Siempre que el archivo DLL esté registrado como el servidor COM, una aplicación puede crear el filtro y agregarlo a un gráfico de filtros. Sin embargo, si desea que el filtro sea reconocible por el enumerador de dispositivos del sistema o por el asignador de filtros, debe registrar la información adicional.

La entrada del registro para el archivo DLL tiene las claves siguientes:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



La entrada del registro para la información de filtro tiene las claves siguientes:


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



es el GUID de una categoría de filtro. (Consulte [categorías de filtro](filter-categories.md)). La información del filtro se empaqueta en un formato binario. La interfaz [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) desempaqueta estos datos cuando busca un filtro en el registro.

Todos los GUID de categoría de filtro se enumeran en el registro con la siguiente clave:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



