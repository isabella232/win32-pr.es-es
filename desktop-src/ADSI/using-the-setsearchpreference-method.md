---
title: Usar el método SetSearchPreference
description: La llamada al método IDirectorySearch SetSearchPreference cambia la manera en que se obtienen los resultados de la búsqueda y se presentan a través de la interfaz IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI, usar el método SetSearchPreference
- ADSI ADSI, código de ejemplo C/C++, usar el método SetSearchPreference
- consulta ADSI mediante SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075052"
---
# <a name="using-the-setsearchpreference-method"></a>Usar el método SetSearchPreference

La llamada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) cambia la manera en que se obtienen los resultados de la búsqueda y se presentan a través de la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

La documentación del SDK define [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) como se indica a continuación:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Se pueden establecer varias preferencias si se pasa una matriz como primer parámetro y el tamaño de la matriz como el segundo parámetro.


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



En este ejemplo se establece el tamaño de página en 100 filas y el ámbito en el \_ tipo de subárbol del ámbito de ADS \_ . La configuración de tamaño de página hace que el servidor devuelva datos inmediatamente al cliente, después de que se hayan calculado 100 filas. La \_ configuración del \_ subárbol del ámbito de ADS hace que la búsqueda abarque todas las ramas del árbol debajo del punto en el que se ejecuta la búsqueda.

 

 




