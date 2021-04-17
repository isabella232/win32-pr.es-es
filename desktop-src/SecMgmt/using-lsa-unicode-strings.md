---
description: Varias de las funciones de directiva de LSA usan la \_ estructura de cadena Unicode LSA \_ para almacenar información de cadena. Esta estructura almacena la cadena y su información de longitud.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Usar cadenas Unicode de LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686666"
---
# <a name="using-lsa-unicode-strings"></a>Usar cadenas Unicode de LSA

Varias de las funciones de directiva de LSA usan la estructura de [**\_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) para almacenar información de cadena. Esta estructura almacena la cadena y su información de longitud.

El código siguiente implementa una función que convierte los datos de **LPWStr** en estructuras de [**\_ \_ cadena Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) :


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



 

 



