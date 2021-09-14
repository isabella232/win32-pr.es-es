---
description: Diseño de las claves del Registro
ms.assetid: c041d094-8165-446f-bf77-0d53b728fe7a
title: Diseño de las claves del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5783a9f083f639912188f418238f46a5d45ed922
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061026"
---
# <a name="layout-of-the-registry-keys"></a>Diseño de las claves del Registro

DirectShow se registran en dos lugares:

-   El archivo DLL que contiene el filtro se registra como servidor COM del filtro. Cuando una aplicación llama a **CoCreateInstance** para crear el filtro, la biblioteca COM de Microsoft Windows usa esta entrada del Registro para buscar el archivo DLL.
-   Se puede registrar información adicional sobre el filtro dentro de una categoría de filtro. Esta información permite que [el enumerador de dispositivos del sistema](system-device-enumerator.md) y el [asignador de filtros](filter-mapper.md) busquen el filtro.

Los filtros no son necesarios para registrar la información de filtro adicional. Siempre que el archivo DLL esté registrado como servidor COM, una aplicación puede crear el filtro y agregarlo a un gráfico de filtros. Sin embargo, si desea que el enumerador de dispositivos del sistema o el asignador de filtros puedan detectar el filtro, debe registrar la información adicional.

La entrada del Registro para el archivo DLL tiene las siguientes claves:


```
HKEY_CLASSES_ROOT
    CLSID
        Filter CLSID 
            REG_SZ: (Default) = Friendly name

            InprocServer32
                REG_SZ: (Default) = File name of the DLL
                REG_SZ: ThreadingModel = Both
```



La entrada del Registro para la información del filtro tiene las siguientes claves:


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



es el GUID de una categoría de filtro. (Vea [Categorías de filtro](filter-categories.md)). La información del filtro se empaqueta en un formato binario. La [**interfaz IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) desempaqueta estos datos cuando busca un filtro en el Registro.

Todos los GUID de la categoría de filtro se enumeran en el Registro con la clave siguiente:


```C++
HKEY_CLASSES_ROOT\CLSID\{DA4E3DA0-D07D-11d0-BD50-00A0C911CE86}\Instance
```



 

 



