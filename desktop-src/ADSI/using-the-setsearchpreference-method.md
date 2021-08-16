---
title: Usar el método SetSearchPreference
description: Llamar al método SetSearchPreference de IDirectorySearch cambia la forma en que se obtienen y presentan los resultados de la búsqueda a través de la interfaz IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI , mediante el método SetSearchPreference
- ADSI ADSI , código de ejemplo C/C++ , mediante el método SetSearchPreference
- consulta ADSI mediante SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7f40d7af4069c9b67d9cd2634f6b7f58f51aafce95af9d4f9275b0e55fc1b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637485"
---
# <a name="using-the-setsearchpreference-method"></a>Usar el método SetSearchPreference

Llamar al [**método IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) cambia la forma en que se obtienen y presentan los resultados de la búsqueda a través de la [**interfaz IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

La documentación del SDK [**define SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) de la siguiente manera:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Se pueden establecer varias preferencias pasando una matriz como primer parámetro y el tamaño de la matriz como segundo parámetro.


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



En este ejemplo se establece el tamaño de página en 100 filas y el ámbito en el tipo ADS \_ SCOPE \_ SUBTREE. La configuración de tamaño de página hace que el servidor devuelva datos inmediatamente al cliente, después de que se hayan calculado 100 filas. La configuración ADS SCOPE SUBTREE hace que la búsqueda abarque todas las ramas del árbol debajo del punto desde el que se \_ \_ ejecuta la búsqueda.

 

 




