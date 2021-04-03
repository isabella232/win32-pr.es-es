---
title: Comprobar la sintaxis del filtro de consulta
description: La API de LDAP proporciona una sencilla función de comprobación de sintaxis. Tenga en cuenta que solo comprueba la sintaxis y no la existencia de las propiedades especificadas en el filtro.
ms.assetid: 4e564cd9-2f8b-4e70-928c-3a8bd804aeba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da2c15052309bc2acbcff9d6bdabea95337db1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075021"
---
# <a name="checking-the-query-filter-syntax"></a>Comprobar la sintaxis del filtro de consulta

La API de LDAP proporciona una sencilla función de comprobación de sintaxis. Tenga en cuenta que solo comprueba la sintaxis y no la existencia de las propiedades especificadas en el filtro.

La función siguiente comprueba la sintaxis del filtro de consulta y devuelve **S \_ OK** si el filtro es válido o s \_ false si no lo es.


```C++
HRESULT CheckFilterSyntax(
    LPOLESTR szServer, // NULL binds to a DC in the current domain.
    LPOLESTR szFilter) // Filter to check.
{
HRESULT hr = S_OK;
DWORD dwReturn;
LDAP *hConnect = NULL;  // Connection handle
 
if (!szFilter)
  return E_POINTER;
 
// LDAP_PORT is the default port, 389
 
hConnect  = ldap_open(szServer,  LDAP_PORT);
 
// Bind using the preferred authentication method on Windows 2000
// and the calling thread's security context.
 
dwReturn = ldap_bind_s( hConnect, NULL, NULL, LDAP_AUTH_NEGOTIATE );
if (dwReturn==LDAP_SUCCESS) {
    dwReturn = ldap_check_filter(hConnect, szFilter);
    if (dwReturn==LDAP_SUCCESS)
        hr = S_OK;
    else
        hr = S_FALSE;
}
 
// Unbind to free the connection.
 
ldap_unbind( hConnect );
 
return hr;
}
```



 

 




