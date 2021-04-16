---
title: Límite de tamaño con IDirectorySearch
description: El cliente puede centrarse en un pequeño número de objetos devueltos desde el servidor y omitir el resto del conjunto de resultados.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Límite de tamaño con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, límite de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656148"
---
# <a name="size-limit-with-idirectorysearch"></a>Límite de tamaño con IDirectorySearch

Para reducir los requisitos de memoria o para otros propósitos, el cliente puede centrarse en un pequeño número de objetos devueltos desde el servidor y omitir el resto del conjunto de resultados que no son de interés. Para ello, el cliente especifica el límite de tamaño de búsqueda y otros criterios de búsqueda adecuados. Por ejemplo, si el directorio almacena las puntuaciones de pruebas de un distrito escolar, puede consultar los diez estudiantes principales con las puntuaciones de prueba más altas especificando un límite de tamaño de diez (10) y un criterio de ordenación descendente.

El valor predeterminado para el límite de tamaño es sin límite. Para establecer un límite de tamaño, establezca una opción de búsqueda de límite de tamaño de SEARCHPREF de ADS con un valor **\_ entero de ADSTYPE** que contenga el tamaño máximo de la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . **\_ \_ \_**

En el ejemplo de código siguiente se muestra cómo establecer el límite de tamaño. Un valor de límite de tamaño de cero indica que no hay límite de tamaño.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Por Active Directory, el límite de tamaño especifica el número máximo de objetos que se devolverán en la búsqueda. Además, para Active Directory, el número máximo de objetos devueltos por una búsqueda es 1000 objetos.

 

 




