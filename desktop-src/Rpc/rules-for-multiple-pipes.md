---
title: Reglas para varias canalizaciones
description: Reglas para varias canalizaciones en una sola llamada en llamada a procedimiento remoto (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488106"
---
# <a name="rules-for-multiple-pipes"></a><span data-ttu-id="529c5-103">Reglas para varias canalizaciones</span><span class="sxs-lookup"><span data-stu-id="529c5-103">Rules for Multiple Pipes</span></span>

<span data-ttu-id="529c5-104">Puede combinar los \[ parámetros [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] y \[ **in, out** de \] canalización en cualquier combinación en una sola llamada, pero debe procesar las canalizaciones en un orden específico, como se muestra en el siguiente ejemplo de pseudocódigo:</span><span class="sxs-lookup"><span data-stu-id="529c5-104">You can combine \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], and \[**in, out**\] pipe parameters in any combination in a single call, but you must process the pipes in a specific order, as shown in the following pseudocode example:</span></span>

> [!Note]  
> <span data-ttu-id="529c5-105">Esta característica ya no se admite en Windows Vista y en plataformas posteriores.</span><span class="sxs-lookup"><span data-stu-id="529c5-105">This feature is no longer supported in Windows Vista and later platforms.</span></span>

 

-   <span data-ttu-id="529c5-106">Obtenga los datos de cada canalización de entrada, empezando por el primer parámetro (en el extremo izquierdo) \[  \] , y continuando en orden, purgando cada canalización antes de empezar a procesar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="529c5-106">Get the data from every input pipe, starting with the first (leftmost) \[**in**\] parameter, and continuing in order, draining each pipe before beginning to process the next.</span></span>
-   <span data-ttu-id="529c5-107">Una vez procesados por completo cada canalización de entrada, envíe los datos para las canalizaciones de salida, de nuevo a partir del primer \[  \] parámetro out y continúe en orden, rellenando cada canalización antes de empezar a procesar la siguiente.</span><span class="sxs-lookup"><span data-stu-id="529c5-107">After every input pipe has been completely processed, send the data for the output pipes, again starting with the first \[**out**\] parameter, and continuing in order, filling each pipe before beginning to process the next.</span></span>

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 