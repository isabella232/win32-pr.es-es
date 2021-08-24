---
title: Ordenar los resultados de la búsqueda con IDirectorySearch
description: De forma predeterminada, los resultados de una búsqueda se devuelven sin ningún orden garantizado. La preferencia SEARCHPREF SORT ON de ADS indica al servidor que ordene el conjunto de resultados en un valor de atributo especificado antes de que se devuelva \_ \_ al \_ cliente.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Ordenar los resultados de la búsqueda con IDirectorySearch
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Ordenar resultados de la búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7864a3878d2cdc44d58c6f6090f6b791b9fe29b3d2613e6e3d4aaf0b6289e100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443875"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Ordenar los resultados de la búsqueda con IDirectorySearch

De forma predeterminada, los resultados de una búsqueda se devuelven sin ningún orden garantizado. La **preferencia \_ SEARCHPREF \_ SORT \_ ON** de ADS indica al servidor que ordene el conjunto de resultados en un valor de atributo especificado antes de que se devuelva al cliente.

Se recomienda usar atributos indexados para la ordenación. De lo contrario, el servidor debe recuperar el conjunto de resultados completo y ordenarlo antes de enviar los resultados al cliente. Esto también se aplica a las búsquedas paginadas. Tenga en cuenta que el rendimiento de una búsqueda ordenada se incrementará si el filtro incluye un atributo indexado y ese atributo se especifica como clave de ordenación. en este caso, Active Directory puede satisfacer la ordenación mientras se procesa el filtro. Por ejemplo, una consulta de ordenación eficaz para un conjunto de usuarios podría tener un filtro que incluye (sn>smith) y una clave de ordenación de sn.

La ordenación del lado servidor con la opción de búsqueda **\_ ADS SEARCHPREF \_ SORT \_ ON** reducirá el rendimiento del servidor. Si va a realizar muchas búsquedas, considere la posibilidad de ordenar los resultados manualmente en el lado cliente para reducir la carga de trabajo en el servidor.

De forma predeterminada, la ordenación de resultados está deshabilitada. Para habilitar la ordenación de resultados, establezca una opción de búsqueda **\_ ADS SEARCHPREF \_ SORT \_ ON** con **ADSTYPE \_ PROV \_ SPECIFIC** que apunta a una estructura [**\_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) de ADS en la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) La **estructura \_ SORTKEY de ADS** se usa para especificar el atributo por el que se va a ordenar y el orden de ordenación.

En el ejemplo de código siguiente se muestra cómo habilitar la ordenación de resultados.


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



Active Directory no admite la ordenación por atributos construidos, por lo que no es posible especificar un atributo construido para la ordenación. El [**atributo distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) tampoco se puede usar para la ordenación. Active Directory tampoco permite la ordenación en más de un atributo, por lo que la opción de búsqueda **\_ SEARCHPREF \_ SORT \_ ON** de ADS solo puede contener una estructura [**\_ SORTKEY de ADS.**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)

 

 