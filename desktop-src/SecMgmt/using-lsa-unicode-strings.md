---
description: Varias de las funciones de directiva LSA usan la estructura \_ STRING UNICODE LSA para almacenar información de \_ cadena. Esta estructura almacena la cadena y su información de longitud.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Uso de cadenas Unicode LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb3c3c41ddd1e3a76ca86880fa47c1d0b2a47897727b820c5f4caf501f4263d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893002"
---
# <a name="using-lsa-unicode-strings"></a>Uso de cadenas Unicode LSA

Varias de las funciones de directiva LSA usan la estructura [**\_ STRING UNICODE \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) para almacenar información de cadena. Esta estructura almacena la cadena y su información de longitud.

El código siguiente implementa una función que convierte los datos **LPWSTR** en estructuras [**STRING UNICODE \_ \_ LSA:**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)


```C++
#include <windows.h>

bool InitLsaString(
  PLSA_UNICODE_STRING pLsaString,
  LPCWSTR pwszString
)
{
  DWORD dwLen = 0;

  if (NULL == pLsaString)
      return FALSE;

  if (NULL != pwszString) 
  {
      dwLen = wcslen(pwszString);
      if (dwLen > 0x7ffe)   // String is too large
          return FALSE;
  }

  // Store the string.
  pLsaString->Buffer = (WCHAR *)pwszString;
  pLsaString->Length =  (USHORT)dwLen * sizeof(WCHAR);
  pLsaString->MaximumLength= (USHORT)(dwLen+1) * sizeof(WCHAR);

  return TRUE;
}
```



 

 



