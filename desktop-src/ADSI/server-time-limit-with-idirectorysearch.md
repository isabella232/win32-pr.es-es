---
title: Límite de tiempo del servidor con IDirectorySearch
description: Para evitar el uso de todo el tiempo de CPU y evitar que se ejecuten otras operaciones, especifique el límite de tiempo de búsqueda en un valor pequeño y, después, vuelva a ejecutar la aplicación más adelante si no puede generar el informe.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Límite de tiempo del servidor con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, límite de tiempo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993840"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Límite de tiempo del servidor con IDirectorySearch

Cuando solicita una búsqueda en un servidor ocupado, es posible que desee solicitar que el servidor restrinja la búsqueda a un límite de tiempo especificado. Por ejemplo, desea ejecutar una aplicación para generar un informe semanal en un servidor que ejecute cerca de su capacidad. Para evitar el uso de todo el tiempo de CPU y evitar que se ejecuten otras operaciones, especifique el límite de tiempo de búsqueda en un valor pequeño y, después, vuelva a ejecutar la aplicación más adelante si no puede generar el informe.

Algunos servidores pueden imponer su propio límite de tiempo administrativo. En estos casos, si especifica un valor de límite de tiempo de búsqueda mayor que el límite de tiempo administrativo, el servidor pasará por alto su especificación y usará su valor de límite de tiempo interno en su lugar.

El valor predeterminado para el límite de tiempo del servidor no es límite. Para establecer un límite de tiempo de servidor, establezca una opción de búsqueda de límite de tiempo de SEARCHPREF de ADS con un valor **\_ entero de ADSTYPE** que contenga el límite de tiempo del servidor, en segundos, en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . **\_ \_ \_** Esta operación se muestra en el ejemplo de código siguiente. Un límite de tiempo de servidor de cero indica que no hay ningún límite de tiempo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




