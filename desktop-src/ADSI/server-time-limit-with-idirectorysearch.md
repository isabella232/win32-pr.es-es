---
title: Límite de tiempo del servidor con IDirectorySearch
description: Para evitar usar todo el tiempo de CPU e impedir que se ejecuten otras operaciones, especifique el límite de tiempo de búsqueda en un valor pequeño y, a continuación, vuelva a ejecutar la aplicación más adelante si no se puede generar el informe.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Límite de tiempo del servidor con IDirectorySearch ADSI
- ADSI, Búsqueda, IDirectorySearch, Otras opciones de búsqueda, Límite de tiempo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e120586cb05fa07baf1e26fa8c1db8e11eecdbd1b19ed7f4f9c2215a921409ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262143"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Límite de tiempo del servidor con IDirectorySearch

Al solicitar una búsqueda en un servidor ocupado, puede solicitar que el servidor restrinja la búsqueda a un límite de tiempo especificado. Por ejemplo, quiere ejecutar una aplicación para generar un informe semanal en un servidor que se ejecuta cerca de su capacidad. Para evitar usar todo el tiempo de CPU e impedir que se ejecuten otras operaciones, especifique el límite de tiempo de búsqueda en un valor pequeño y, a continuación, vuelva a ejecutar la aplicación más adelante si no se puede generar el informe.

Algunos servidores pueden imponer su propio límite de tiempo administrativo. En estos casos, si especifica un valor de límite de tiempo de búsqueda mayor que el límite de tiempo administrativo, el servidor omitirá la especificación y usará su valor de límite de tiempo interno en su lugar.

El valor predeterminado para el límite de tiempo del servidor no es ningún límite. Para establecer un límite de tiempo de servidor, establezca una opción de búsqueda **ADS \_ SEARCHPREF \_ TIME \_ LIMIT** con un valor **ADSTYPE \_ INTEGER** que contenga el límite de tiempo del servidor, en segundos, en la matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Esta operación se muestra en el ejemplo de código siguiente. Un límite de tiempo de servidor de cero indica que no hay límite de tiempo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




