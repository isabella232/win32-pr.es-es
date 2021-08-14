---
title: Límite de tamaño con IDirectorySearch
description: El cliente puede centrarse en un pequeño número de objetos devueltos desde el servidor e ignorar el resto del conjunto de resultados.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Límite de tamaño con IDirectorySearch ADSI
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Límite de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6ee4e23cb3014ea92e8510da88767a433b76c0fe73ccbe74bac6ba0bfc1c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178750"
---
# <a name="size-limit-with-idirectorysearch"></a>Límite de tamaño con IDirectorySearch

Para reducir el requisito de memoria o para otros fines, el cliente puede centrarse en un pequeño número de objetos devueltos desde el servidor e ignorar el resto del conjunto de resultados que no son de interés. Para ello, el cliente especifica el límite de tamaño de búsqueda y otros criterios de búsqueda adecuados. Por ejemplo, si el directorio almacena las puntuaciones de prueba de un distrito educativo, puede consultar a los diez alumnos con las puntuaciones de prueba más altas especificando un límite de tamaño de diez (10) y un criterio de ordenación descendente.

El valor predeterminado para el límite de tamaño no es ningún límite. Para establecer un límite de tamaño, establezca una opción de búsqueda **ADS \_ SEARCHPREF \_ SIZE \_ LIMIT** con un valor **INTEGER ADSTYPE \_** que contenga el tamaño máximo de la matriz [**\_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

En el ejemplo de código siguiente se muestra cómo establecer el límite de tamaño. Un valor de límite de tamaño de cero indica que no hay límite de tamaño.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Por Active Directory, el límite de tamaño especifica el número máximo de objetos que va a devolver la búsqueda. También para Active Directory, el número máximo de objetos devueltos por una búsqueda es de 1000 objetos.

 

 




