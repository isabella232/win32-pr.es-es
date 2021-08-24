---
title: Devolver solo nombres de atributo con IDirectorySearch
description: Puede realizar una búsqueda para determinar qué tipo de datos está disponible para un objeto determinado.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Devolver solo nombres de atributo con ADSI de IDirectorySearch
- ADSI, Searching, IDirectorySearch, Other Search Options, Returning Only Attribute Names
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b9c69a99cad0ece5c660ba45954fe537abe69cfa88947b52b0d69d7833b4e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444015"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Devolver solo nombres de atributo con IDirectorySearch

Puede realizar una búsqueda para determinar qué tipo de datos está disponible para un objeto determinado. En este caso, solo le interesan los nombres de los atributos, no los valores de atributo del objeto. La **opción \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** de ADS hace que el servidor solo devuelva los nombres de atributo y no los valores de atributo. Sin embargo, el conjunto de resultados incluye solo los atributos que tienen valores asignados. Por ejemplo, considere un objeto con los atributos siguientes:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Cuando se **establece la opción ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY,** el conjunto de resultados incluye:

``` syntax
name
sn
department
phone
```

El valor predeterminado es que se devuelvan los valores de atributo y los nombres.

Para recuperar solo nombres de atributo, establezca una opción de búsqueda **\_ ADS SEARCHPREF \_ ATTRIBTYPES \_ ONLY** con un valor **\_ BOOLEANo ADSTYPE** **true** en la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

En el ejemplo de código siguiente se muestra cómo recuperar solo nombres de atributo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Para obtener más información y un ejemplo de código que muestra cómo usar la opción de búsqueda **\_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** de ADS, vea Código de ejemplo para buscar [atributos.](example-code-for-searching-for-attributes.md)

 

 




