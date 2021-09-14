---
description: En el ejemplo siguiente se usa la función VerifyVersionInfo para determinar si los grupos de productos especificados están instalados en el equipo local.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Detección de un conjunto de productos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068886"
---
# <a name="detecting-a-product-suite"></a>Detección de un conjunto de productos

En el ejemplo siguiente se usa [**la función VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para determinar si los grupos de productos especificados están instalados en el equipo local.

En este ejemplo se usa la \_ marca VER AND. Si se especifican dos marcas en la máscara del conjunto de datos, la función devuelve **TRUE** solo si ambos conjuntos de productos están presentes. Si se cambió el ejemplo para usar la marca VER \_ OR, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) devolvería **TRUE** si alguno de los dos grupos de productos estuviera presente.


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



