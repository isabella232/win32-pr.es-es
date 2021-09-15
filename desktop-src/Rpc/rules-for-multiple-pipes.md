---
title: Reglas para varias canalizaciones
description: Reglas para varias canalizaciones en una sola llamada en llamada a procedimiento remoto (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473564"
---
# <a name="rules-for-multiple-pipes"></a>Reglas para varias canalizaciones

Puede combinar en , out y en parámetros de canalización out en cualquier combinación en una sola llamada, pero debe procesar las canalizaciones en un orden específico, como se muestra en el siguiente ejemplo de \[ [](/windows/desktop/Midl/in) \] \[ [](/windows/desktop/Midl/out-idl) \] \[  \] pseudocódigo:

> [!Note]  
> Esta característica ya no se admite en Windows Vista y plataformas posteriores.

 

-   Obtenga los datos de cada canalización de entrada, empezando por el primer parámetro (situado más a la izquierda) en el parámetro y continuando en orden, purgando cada canalización antes de empezar a \[  \] procesar la siguiente.
-   Una vez que todas las canalizaciones de entrada se hayan procesado completamente, envíe los datos de las canalizaciones de salida, empezando de nuevo por el primer parámetro out y continuando en orden, rellenando cada canalización antes de empezar a procesar la \[  \] siguiente.

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

 

 