---
description: En el ejemplo siguiente se usa la función VerifyVersionInfo para determinar si los conjuntos de productos especificados están instalados en el equipo local.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Detección de un conjunto de productos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669975"
---
# <a name="detecting-a-product-suite"></a><span data-ttu-id="90883-103">Detección de un conjunto de productos</span><span class="sxs-lookup"><span data-stu-id="90883-103">Detecting a Product Suite</span></span>

<span data-ttu-id="90883-104">En el ejemplo siguiente se usa la función [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) para determinar si los conjuntos de productos especificados están instalados en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="90883-104">The following example uses the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the specified product suite(s) are installed on the local computer.</span></span>

<span data-ttu-id="90883-105">En este ejemplo se usa la \_ marca ver y.</span><span class="sxs-lookup"><span data-stu-id="90883-105">This example uses the VER\_AND flag.</span></span> <span data-ttu-id="90883-106">Si se especifican dos marcas en la máscara de conjunto, la función devuelve **true** solo si ambos conjuntos de productos están presentes.</span><span class="sxs-lookup"><span data-stu-id="90883-106">If two flags are specified in the suite mask, the function returns **TRUE** only if both product suites are present.</span></span> <span data-ttu-id="90883-107">Si el ejemplo se ha cambiado para usar la \_ marca ver o, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) devolvería **true** si algún conjunto de productos estuviera presente.</span><span class="sxs-lookup"><span data-stu-id="90883-107">If the example were changed to use the VER\_OR flag, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) would return **TRUE** if either product suite were present.</span></span>


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



 

 



