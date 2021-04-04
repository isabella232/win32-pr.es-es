---
title: Código de ejemplo para buscar atributos
description: En el ejemplo de código siguiente se muestra cómo usar \_ la \_ \_ preferencia de búsqueda solo ATTRIBTYPES de ADS SEARCHPREF para recuperar los nombres de los atributos a los que se han asignado valores.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, código de ejemplo C/C++, buscar atributos
- Código de ejemplo para buscar atributos
- ADSI, buscar, IDirectorySearch, otras opciones de búsqueda, devolver únicamente nombres de atributo, código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344ce99fe9de606212d786ff2e7b88b5eba34d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772967"
---
# <a name="example-code-for-searching-for-attributes"></a>Código de ejemplo para buscar atributos

En el ejemplo de código siguiente se muestra cómo usar la preferencia de búsqueda **\_ \_ \_ solo ATTRIBTYPES de ADS SEARCHPREF** para recuperar los nombres de los atributos a los que se han asignado valores. En el ejemplo se inicializa una estructura [**ADS \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) y se establece la preferencia de búsqueda llamando al método [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) de la interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . A continuación, en el ejemplo se llama al método [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) para realizar la búsqueda.


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




