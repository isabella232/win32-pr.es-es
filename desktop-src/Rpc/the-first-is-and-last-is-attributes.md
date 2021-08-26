---
title: Atributos first_is y last_is de datos
description: Puede determinar el número de elementos transmitidos especificando el primer y el último elemento.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c30c2e7e6689ba2a61f7f5e694a5b29f39af5cadcf7fa2ca2f51e14e1f3457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017145"
---
# <a name="the-first_is-and-last_is-attributes"></a>El \[ primero es y el último es \_ \] \[ \_ \] Atributos.

Puede determinar el número de elementos transmitidos especificando el primer y el último elemento. Use el \[ [**primero es \_ y**](/windows/desktop/Midl/first-is) \] el último son \[ [**\_ los**](/windows/desktop/Midl/last-is) \] atributos como se muestra:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 