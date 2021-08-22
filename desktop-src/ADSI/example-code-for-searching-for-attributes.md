---
title: Código de ejemplo para buscar atributos
description: En el ejemplo de código siguiente se muestra cómo usar la preferencia de búsqueda \_ SEARCHPREF \_ ATTRIBTYPES ONLY de ADS para recuperar solo los nombres de atributos a los que se han asignado \_ valores.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, código de ejemplo C/C++, buscar atributos
- Código de ejemplo para buscar atributos
- ADSI, Búsqueda, IDirectorySearch, otras opciones de búsqueda, devolver solo nombres de atributo, código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207fcfd2bd688f5bb6ddcd19dcb9b1a87a2e40ddb0a7db1e63e9457e671f9947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428468"
---
# <a name="example-code-for-searching-for-attributes"></a>Código de ejemplo para buscar atributos

En el ejemplo de código siguiente se muestra cómo usar la preferencia de búsqueda **\_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** de ADS para recuperar solo los nombres de atributos a los que se han asignado valores. En el ejemplo se inicializa una estructura [**\_ DE INFORMACIÓN SEARCHPREF \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) de ADS y se establece la preferencia de búsqueda mediante una llamada al método [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) de la [**interfaz IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) A continuación, el ejemplo llama [**al método ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) para realizar la búsqueda.


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



 

 




