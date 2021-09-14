---
description: Varias de las funciones de directiva de LSA usan la estructura STRING UNICODE de LSA \_ para almacenar información de \_ cadena. Esta estructura almacena la cadena y su información de longitud.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Uso de cadenas Unicode LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069002"
---
# <a name="using-lsa-unicode-strings"></a>Uso de cadenas Unicode LSA

Varias de las funciones de directiva de LSA usan la estructura STRING UNICODE de [**LSA \_ \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) para almacenar información de cadena. Esta estructura almacena la cadena y su información de longitud.

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



 

 



