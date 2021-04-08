---
title: Ejemplos de codificación incremental
description: En la sección siguiente se proporciona un ejemplo de cómo usar el controlador de serialización de estilo incremental para la codificación de tipos.
ms.assetid: c50c0de3-aabb-4166-93dc-67b0fee66635
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de la codificación incremental
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16c9cb61e6b2bf55b29fb02e39f41dd7a61c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994575"
---
# <a name="examples-of-incremental-encoding"></a><span data-ttu-id="b77e7-104">Ejemplos de codificación incremental</span><span class="sxs-lookup"><span data-stu-id="b77e7-104">Examples of Incremental Encoding</span></span>

<span data-ttu-id="b77e7-105">En la sección siguiente se proporciona un ejemplo de cómo usar el controlador de serialización de estilo incremental para la codificación de tipos.</span><span class="sxs-lookup"><span data-stu-id="b77e7-105">The following section provides an example of how to use the incremental style serializing handle for type encoding.</span></span>

``` syntax
/* This is an acf file. MooType is defined in the idl file */

[    explicit_handle
]
interface regress
{
typedef [ encode,decode ] MooType;
}
```

<span data-ttu-id="b77e7-106">El siguiente fragmento representa los fragmentos de aplicación pertinentes.</span><span class="sxs-lookup"><span data-stu-id="b77e7-106">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeIncrementalHandleCreate (State, AllocFn, WriteFn, 
    &Handle) == RPC_S_OK)
{
//...
/* The serialize works from the beginning of the buffer because
    the handle is in the initial state. The Moo_Encode does the
    following:
    - sizes *pMooObject for marshalling,
    - calls AllocFn with the size obtained,
    - marshalls into the buffer returned by Alloc, and
    - calls WriteFn with the filled buffer 
*/

Moo_Encode ( Handle, pMooObject );
...
}
if (MesIncrementalHandleReset (Handle, NULL, NULL, NULL, ReadFn,
    MES_DECODE ) == RPC_OK)
{
/*The ReadFn is needed to reset the handle. The arguments
    that are NULL do not change. You can also call 
    MesDecodeIncrementalHandleCreate (State, ReadFn, &Handle);
    The Moo_Decode does the following:
    - calls Read with the appropriate size of data to read and
        receives a buffer with the data
    - unmarshalls the object from the buffer into *pMooObject 
*/

Moo_Decode ( Handle, pMooObject );
//...
MesHandleFree ( Handle );
}
```



 

 




