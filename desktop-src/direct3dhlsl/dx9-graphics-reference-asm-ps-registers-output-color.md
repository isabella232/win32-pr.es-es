---
title: Registro de color de salida
description: Los registros de salida de color del sombreador de píxeles (oC \) son registros de solo escritura que generan resultados en varios destinos de representación.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421209"
---
# <a name="output-color-register"></a>Registro de color de salida

Los registros de salida de color del sombreador de píxeles (oC #) son registros de solo escritura que generan resultados en varios destinos de representación.

Sintaxis



| Opcional # |
|------|



 

Donde:



| Nombre | Descripción       |
|------|-------------------|
| oC0  | destino de representación \# 0 |
| oC1  | destino de representación \# 1 |
| oC2  | destino de representación \# 2 |
| oC3  | destino de representación \# 3 |



 

## <a name="remarks"></a>Observaciones

-   Si oCn se escribe pero no hay ningún destino de representación correspondiente, se omite esta escritura en oCn.
-   Los Estados de representación D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 y D3DRS \_ COLORWRITEENABLE3 determinan qué componentes de oCn se escriben en última instancia en el destino de representación (después de Blend, si procede). Si el sombreador escribe algunos, pero no todos los componentes definidos por los Estados de representación de D3DRS \_ COLORWRITEENABLE \* para un registro de oCn determinado, los canales sin escribir generan valores no definidos en el destino de representación correspondiente. Si no se escribe ninguno de los componentes de un oCn, el destino de representación correspondiente no debe actualizarse en absoluto (como se indicó anteriormente), por lo que \_ no se aplican los Estados de representación COLORWRITEENABLE de D3DRS \* .

### <a name="shader-model-2-restrictions"></a>Restricciones del modelo 2 del sombreador

-   oCn solo se puede escribir con la instrucción [MOV-PS](mov---ps.md) .
-   oC0 debe estar siempre escrito en el sombreador.
-   No se permite ningún swizzle de origen (excepto. xyzw = default swizzle) o el modificador de origen al escribir en cualquier oCn.
-   No se permite ninguna máscara de escritura de destino (excepto. xyzw = máscara predeterminada) o el modificador de instrucciones cuando se escribe en cualquier oCn.
-   Si se escribe oCn, también se debe escribir oC0-oCn-1. Por ejemplo, para escribir en oC2, también debe escribir en oC0 y oC1.
-   Como máximo, se permite una escritura en cualquier número de oC por sombreador.
-   En el caso de PS \_ 2 \_ x y PS \_ 3 \_ 0, no se pueden escribir en los registros de OC # y OD \# en el control de flujo dinámico o en predication (el control de flujo estático de escrituras en OC es fino).

### <a name="shader-model-3-restrictions"></a>Restricciones del modelo de sombreador 3

-   En el caso de PS \_ 3 \_ 0, los registros de salida \# se pueden escribir en cualquier número de veces. La salida del sombreador de píxeles procede del contenido de los registros de salida al final de la ejecución del sombreador. Si no se produce una escritura en un registro de salida, quizás debido al control de flujo o si el sombreador no lo escribió, tampoco se actualiza el rendertarget correspondiente. Si se escribe un subconjunto de los canales en un registro de salida, los valores no definidos se escribirán en los canales restantes.
-   Para PS \_ 3 \_ 0, los registros de OC # se pueden escribir con cualquier writemasks.
-   En el caso de PS \_ 2 \_ x y PS \_ 3 \_ 0, no se pueden escribir en los registros de OC # y OD \# en el control de flujo dinámico o en predication (el control de flujo estático de escrituras en OC es fino).
-   No puede realizar ningún cálculo de degradado (u operaciones que invoquen implícitamente los cálculos de degradado como [texld-PS \_ 2 \_ 0 y up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) dentro de las instrucciones de control de flujo cuyas condiciones de bifurcación varían en función de la primitiva (por ejemplo: instrucciones de control de flujo dinámico). La instrucción predication no se considera el control de flujo dinámico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Varios destinos de representación (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 