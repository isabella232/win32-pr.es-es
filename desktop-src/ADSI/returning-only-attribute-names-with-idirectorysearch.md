---
title: Devolver solo nombres de atributo con IDirectorySearch
description: Puede realizar una búsqueda para determinar qué tipo de datos están disponibles para un objeto determinado.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Devolver solo nombres de atributo con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch y otras opciones de búsqueda, devolviendo únicamente nombres de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656153"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Devolver solo nombres de atributo con IDirectorySearch

Puede realizar una búsqueda para determinar qué tipo de datos están disponibles para un objeto determinado. En este caso, solo está interesado en los nombres de los atributos, no en los valores de atributo del objeto. La opción **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ solo** hace que el servidor devuelva solo los nombres de atributo y no los valores de atributo. Sin embargo, el conjunto de resultados incluye solo los atributos que tienen valores asignados. Por ejemplo, considere un objeto con los siguientes atributos:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Cuando se establece la opción **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ Only** , el conjunto de resultados incluye:

``` syntax
name
sn
department
phone
```

El valor predeterminado es para que se devuelvan los nombres y los valores de atributo.

Para recuperar solo los nombres de atributo, establezca una opción de búsqueda **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ Only** con un valor **\_ booleano ADSTYPE** de **true** en la matriz [**ADS \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) que se pasa al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

En el ejemplo de código siguiente se muestra cómo recuperar solo los nombres de atributo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Para obtener más información y un ejemplo de código que muestra cómo usar la opción de búsqueda **\_ \_ \_ solo ATTRIBTYPES de ADS SEARCHPREF** , consulte el [código de ejemplo para buscar atributos](example-code-for-searching-for-attributes.md).

 

 




