---
description: Las técnicas proporcionan el músculo de representación. Una técnica encapsula el estado del efecto que determina un estilo de representación. Una técnica se compone de una o varias fases.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Técnicas y pasos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686422"
---
# <a name="techniques-and-passes-direct3d-9"></a>Técnicas y pasos (Direct3D 9)

Las técnicas proporcionan el músculo de representación. Una técnica encapsula el estado del efecto que determina un estilo de representación. Una técnica se compone de una o varias fases.

## <a name="techniques"></a>Descrita

La sintaxis para llamar a una técnica es la siguiente:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Donde:

-   ID es un nombre único opcional.
-   la anotación es cero o más partes opcionales de la información específica del usuario. Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).
-   Pass (es) es cero o más pasos. Cada paso contiene asignaciones de estado. Vea a continuación.

## <a name="passes"></a>Paso

Un paso contiene las asignaciones de estado necesarias para representarlas.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Donde:

-   ID es un nombre único opcional.
-   la anotación es una parte opcional de la información específica del usuario. Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).
-   asignación (s) asigna cero o más valores de estado o evalúa una o varias expresiones. Vea [Estados de efectos (Direct3D 9)](effect-states.md) y [expresiones (Direct3D 9)](expressions.md).

Pasa por alto todas las asignaciones menos la última en un conjunto de asignaciones repetidas al mismo estado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



