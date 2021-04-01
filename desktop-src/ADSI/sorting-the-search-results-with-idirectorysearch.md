---
title: Ordenar los resultados de la búsqueda con IDirectorySearch
description: De forma predeterminada, los resultados de una búsqueda se devuelven sin ningún orden garantizado. La \_ \_ \_ preferencia ordenar por SEARCHPREF de ADS indica al servidor que ordene el conjunto de resultados en un valor de atributo especificado antes de que se devuelva al cliente.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Ordenar los resultados de la búsqueda con IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, ordenar los resultados de la búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793828"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Ordenar los resultados de la búsqueda con IDirectorySearch

De forma predeterminada, los resultados de una búsqueda se devuelven sin ningún orden garantizado. La **preferencia \_ \_ ordenar \_ por SEARCHPREF de ADS** indica al servidor que ordene el conjunto de resultados en un valor de atributo especificado antes de que se devuelva al cliente.

Se recomienda utilizar atributos indexados para la ordenación. De lo contrario, el servidor debe recuperar el conjunto de resultados completo y ordenarlo antes de enviar los resultados al cliente. Esto también se aplica a las búsquedas paginadas. Tenga en cuenta que se aumentará el rendimiento de una búsqueda ordenada si el filtro incluye un atributo indexado y ese atributo se especifica como criterio de ordenación; en este caso, Active Directory puede satisfacer la ordenación mientras se procesa el filtro. Por ejemplo, una consulta de ordenación eficaz para un conjunto de usuarios podría tener un filtro incluido (SN>Smith) y un criterio de ordenación de SN.

La ordenación del lado servidor con la opción de búsqueda **\_ \_ ordenar \_ por SEARCHPREF de ADS** reducirá el rendimiento del servidor. Si va a realizar muchas búsquedas, considere la posibilidad de ordenar los resultados manualmente en el lado del cliente para reducir la carga de trabajo en el servidor.

De forma predeterminada, la ordenación de los resultados está deshabilitada. Para habilitar la ordenación de resultados, establezca una opción **ADS \_ SEARCHPREF \_ Sort \_ on** Search con un valor **\_ \_ específico de ADSTYPE Prov** que señale a una estructura [**\_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) de ADS en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . La **estructura \_ SORTKEY de ADS** se usa para especificar el atributo por el que se va a ordenar y el orden de la ordenación.

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



Active Directory no admite la ordenación de atributos construidos, por lo que no es posible especificar un atributo construido para la ordenación. El atributo [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) tampoco se puede usar para ordenar. Active Directory tampoco permite la ordenación en más de un atributo, por lo que la opción **\_ \_ de ordenación \_ de la búsqueda de SEARCHPREF de anuncios** solo puede contener una estructura de tipo [**\_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .

 

 