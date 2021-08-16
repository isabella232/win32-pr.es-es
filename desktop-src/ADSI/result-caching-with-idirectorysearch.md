---
title: Almacenamiento en caché de resultados con IDirectorySearch
description: La preferencia SEARCHPREF CACHE RESULTS de ADS almacena en caché \_ \_ el conjunto de \_ resultados en el cliente.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Almacenamiento en caché de resultados con ADSI de IDirectorySearch
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Almacenamiento en caché de resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838861"
---
# <a name="result-caching-with-idirectorysearch"></a>Almacenamiento en caché de resultados con IDirectorySearch

La **preferencia \_ SEARCHPREF \_ CACHE RESULTS \_ de ADS** almacena en caché el conjunto de resultados en el cliente. El almacenamiento en caché de resultados permite a una aplicación conservar un conjunto de resultados recuperado y volver a pasar por las filas recuperadas. También permite la compatibilidad con cursores donde los métodos [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) e [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) se pueden usar para subir y bajar el conjunto de resultados.

De forma predeterminada, el almacenamiento en caché de resultados está deshabilitado. El almacenamiento en caché de resultados debe habilitarse si se cumple alguna de las siguientes condiciones:

-   Si el mismo conjunto de resultados debe enumerarse varias veces sin volver a realizar la búsqueda en el servidor.
-   Si la búsqueda consume muchos recursos en el servidor (conexión lenta, conjunto de resultados grande o consulta compleja).
-   Si se requiere compatibilidad con cursores.

Desactive el almacenamiento en caché si la aplicación debe reducir los requisitos de memoria para almacenar en caché un conjunto de resultados grande en el cliente.

El almacenamiento en caché de resultados aumenta los requisitos de memoria en el cliente, por lo que el almacenamiento en caché de resultados debe deshabilitarse si esto es un problema.

Para habilitar el almacenamiento en caché de resultados, establezca una opción de búsqueda **\_ SEARCHPREF \_ CACHE \_ RESULTS** de ADS con un valor **\_ BOOLEANo ADSTYPE** **true** en la matriz DE INFORMACIÓN [**\_ SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

En el ejemplo de código siguiente se muestra cómo habilitar el almacenamiento en caché de resultados.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




