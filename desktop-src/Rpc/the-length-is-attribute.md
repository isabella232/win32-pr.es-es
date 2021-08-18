---
title: El length_is atributo
description: El atributo \ size \_ is\ permite especificar el tamaño máximo de la matriz.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436559961d815adb417d83de5ffa8c06d8497fa0899644411d252c84d6e34ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924264"
---
# <a name="the-length_is-attribute"></a>La \[ longitud \_ es \] Attribute

El \[ [**atributo size \_ is**](/windows/desktop/Midl/size-is) \] permite especificar el tamaño máximo de la matriz. Cuando este es el único atributo, se transmiten todos los elementos de la matriz. En lugar de enviar todos los elementos de la matriz, puede especificar los elementos transmitidos mediante \[ [**el atributo length \_ is,**](/windows/desktop/Midl/length-is) \] como se muestra a continuación:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

El tamaño describe la asignación, mientras que la longitud describe la transmisión. El número de elementos transmitidos siempre debe ser menor o igual que el número de elementos asignados. El valor asociado a **la \_ longitud es** siempre menor o igual que el tamaño **\_ es**.

 

 