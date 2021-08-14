---
title: Recuperar el atributo objectClass
description: El atributo objectClass contiene la clase de la que el objeto es una instancia de , así como todas las clases de las que se deriva esa clase.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c4ae206298937839a965eca787b0d56b0021cff32c7d89b06865bb27855a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184146"
---
# <a name="retrieving-the-objectclass-attribute"></a>Recuperar el atributo objectClass

El **atributo objectClass** contiene la clase de la que el objeto es una instancia de , así como todas las clases de las que se deriva esa clase. Por ejemplo, la **clase de** usuario hereda de **la parte** superior , **person** y **organizationalPerson**; Por lo tanto, **el atributo objectClass** contiene los nombres de esas clases, así como user. Por lo tanto, ¿cómo averiguar de qué clase es una instancia el objeto? El **atributo objectClass** es el único atributo con varios valores que tiene valores ordenados. El primer valor es la parte superior de la jerarquía de clases, que es la clase superior, y el último valor es la clase más derivada, que es la clase de la que el objeto es una instancia.

La función siguiente toma un puntero a una columna que contiene un atributo **objectClass** y devuelve la **instancia objectClass** del objeto.


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




