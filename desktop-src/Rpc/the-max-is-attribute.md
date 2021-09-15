---
title: El max_is atributo
description: Puede especificar los límites válidos de los números de índice de una matriz mediante el atributo \max \_ is\.
ms.assetid: b629e3cf-544d-47ee-8f8f-b049f693897c
keywords:
- max_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8901f952a55de6b81143b0e615c878d8599fb354
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476564"
---
# <a name="the-max_is-attribute"></a>El \[ valor máximo es \_ \] Attribute

Puede especificar los límites válidos de los números de índice de una matriz mediante \[ [**el atributo max \_ is.**](/windows/desktop/Midl/max-is) \]

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(5.0)
]
interface arraytest
{
  void fArray5([in] short sMax,
               [in, out, max_is(sMax)]  char achArray[]);
}
```

 

 