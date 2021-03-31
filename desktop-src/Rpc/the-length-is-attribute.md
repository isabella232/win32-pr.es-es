---
title: El atributo length_is
description: El atributo \ size \_ es \ permite especificar el tamaño máximo de la matriz.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793492"
---
# <a name="the-length_is-attribute"></a><span data-ttu-id="7a8e9-104">La \[ longitud \_ es \] Attribute</span><span class="sxs-lookup"><span data-stu-id="7a8e9-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="7a8e9-105">El \[ [**atributo \_ size**](/windows/desktop/Midl/size-is) \] permite especificar el tamaño máximo de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7a8e9-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="7a8e9-106">Cuando este es el único atributo, se transmiten todos los elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="7a8e9-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="7a8e9-107">En lugar de enviar todos los elementos de la matriz, puede especificar los elementos transmitidos mediante el \[ atributo length, como [**\_ se**](/windows/desktop/Midl/length-is) \] indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="7a8e9-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

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

<span data-ttu-id="7a8e9-108">Tamaño describe la asignación mientras que la longitud describe la transmisión.</span><span class="sxs-lookup"><span data-stu-id="7a8e9-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="7a8e9-109">El número de elementos transmitidos siempre debe ser menor o igual que el número de elementos asignados.</span><span class="sxs-lookup"><span data-stu-id="7a8e9-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="7a8e9-110">El valor asociado con **la \_ longitud** es siempre menor o igual que el **tamaño \_ es**.</span><span class="sxs-lookup"><span data-stu-id="7a8e9-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 