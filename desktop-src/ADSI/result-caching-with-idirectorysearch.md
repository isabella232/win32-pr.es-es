---
title: Almacenamiento en caché de resultados con IDirectorySearch
description: La \_ \_ preferencia resultados de la caché de SEARCHPREF ADS \_ almacena en caché el conjunto de resultados en el cliente.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Almacenamiento en caché de resultados con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, almacenamiento en caché de resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356696"
---
# <a name="result-caching-with-idirectorysearch"></a>Almacenamiento en caché de resultados con IDirectorySearch

La preferencia resultados de la **\_ caché de SEARCHPREF \_ \_ ADS** almacena en caché el conjunto de resultados en el cliente. El almacenamiento en caché de resultados permite que una aplicación retenga un conjunto de resultados recuperado y vuelva a pasar por las filas recuperadas. También habilita la compatibilidad con cursores en la que se pueden usar los métodos [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) y [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) para moverse hacia arriba y hacia abajo por el conjunto de resultados.

De forma predeterminada, el almacenamiento en caché de resultados está deshabilitado. El almacenamiento en caché de resultados debe estar habilitado si se cumple alguna de las siguientes condiciones:

-   Si el mismo conjunto de resultados se debe enumerar varias veces sin realizar la búsqueda de nuevo en el servidor.
-   Si realiza la búsqueda con un uso intensivo de recursos en el servidor (conexión lenta, conjunto de resultados grande o consulta compleja).
-   Si se requiere compatibilidad con cursores.

Desactive el almacenamiento en caché si la aplicación debe reducir los requisitos de memoria para almacenar en caché un conjunto de resultados grande en el cliente.

El almacenamiento en caché de resultados aumenta los requisitos de memoria en el cliente, por lo que se debe deshabilitar el almacenamiento en caché de resultados si esto supone un problema.

Para habilitar el almacenamiento en caché de resultados, establezca una opción de búsqueda de **\_ \_ \_ resultados de caché ADS SEARCHPREF** con un valor **\_ booleano ADSTYPE** de **true** en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

En el ejemplo de código siguiente se muestra cómo habilitar el almacenamiento en caché de resultados.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




