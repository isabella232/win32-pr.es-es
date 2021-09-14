---
description: Las técnicas proporcionan el movimiento de representación. Una técnica encapsula el estado del efecto que determina un estilo de representación. Una técnica se conste de uno o varios pases.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Técnicas y pases (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160426"
---
# <a name="techniques-and-passes-direct3d-9"></a>Técnicas y pases (Direct3D 9)

Las técnicas proporcionan el movimiento de representación. Una técnica encapsula el estado del efecto que determina un estilo de representación. Una técnica se conste de uno o varios pases.

## <a name="techniques"></a>Técnicas

La sintaxis para llamar a una técnica es la siguiente:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Donde:

-   id es un nombre único opcional.
-   annotation es cero o más fragmentos opcionales de información específica del usuario. Vea [Agregar información a parámetros de efecto con \_ anotaciones](using-an-effect.md).
-   pass(es) es cero o más pases. Cada paso contiene asignaciones de estado. Véase a continuación.

## <a name="passes"></a>Pasa

Un paso contiene las asignaciones de estado necesarias para representar.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Donde:

-   id es un nombre único opcional.
-   annotation es una o varias piezas opcionales de información específica del usuario. Vea [Agregar información a parámetros de efecto con \_ anotaciones](using-an-effect.md).
-   asigna cero o más valores de estado, o evalúa una o varias expresiones. Vea [Estados de efecto (Direct3D 9)](effect-states.md) y [Expresiones (Direct3D 9).](expressions.md)

Los pases omiten todas las asignaciones, menos la última de un conjunto de asignaciones repetidas, en el mismo estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



