---
title: Registro de color de salida
description: Los registros de salida de color del sombreador de píxeles (oC\) son registros de solo escritura que muestran resultados en varios destinos de representación.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 038446bb7d588222e04028727a447b6a47c941ab6a18a3ba4216f46e93440961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119709"
---
# <a name="output-color-register"></a>Registro de color de salida

Los registros de salida de color del sombreador de píxeles (oC#) son registros de solo escritura que muestran resultados en varios destinos de representación.

Syntax



| Oc # |
|------|



 

Donde:



| Nombre | Descripción       |
|------|-------------------|
| oC0  | destino de representación \# 0 |
| oC1  | destino de representación \# 1 |
| oC2  | destino de representación \# 2 |
| oC3  | destino de representación \# 3 |



 

## <a name="remarks"></a>Comentarios

-   Si oCn está escrito pero no hay ningún destino de representación correspondiente, se omite esta escritura en oCn.
-   Los estados de representación D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 y D3DRS COLORWRITEENABLE3 determinan qué componentes de oCn se escriben en última instancia en el destino de representación (después de \_ blend, si procede). Si el sombreador escribe algunos de los componentes definidos por los estados de representación COLORWRITEENABLE de D3DRS para un registro \_ oCn determinado, los canales no escritos generan valores no definidos en el destino de representación \* correspondiente. Si no se escribe ninguno de los componentes de un oCn, el destino de representación correspondiente no se debe actualizar en absoluto (como se indicó anteriormente), por lo que no se aplican los estados de representación \_ COLORWRITEENABLE de D3DRS. \*

### <a name="shader-model-2-restrictions"></a>Restricciones del modelo de sombreador 2

-   oCn solo se puede escribir con la [instrucción mov - ps.](mov---ps.md)
-   oC0 debe escribirse siempre en el sombreador.
-   Al escribir en cualquier oCn, no se permite ningún modificador de origen (excepto .xyzw = swzzle predeterminado) o de origen.
-   No se permite ninguna máscara de escritura de destino (excepto .xyzw = máscara predeterminada) ni modificador de instrucción al escribir en cualquier oCn.
-   Si se escribe oCn, también se debe escribir oC0 - oCn-1. Por ejemplo, para escribir en oC2, también debe escribir en oC0 y oC1.
-   Se permite como máximo una escritura en cualquier oC# por sombreador.
-   Para ps 2 x y \_ ps 3 0, no puede escribir en registros de oC# y oD dentro del control de flujo dinámico o predicado \_ \_ (las escrituras en \_ \# oC# dentro del control de flujo estático están bien).

### <a name="shader-model-3-restrictions"></a>Restricciones del modelo de sombreador 3

-   Para ps \_ 3 \_ 0, la salida registra oC# y oD \# se puede escribir cualquier número de veces. La salida del sombreador de píxeles procede del contenido de los registros de salida al final de la ejecución del sombreador. Si no se realiza una escritura en un registro de salida, quizás debido al control de flujo o si el sombreador simplemente no lo ha escrito, tampoco se actualiza el destino de representación correspondiente. Si se escribe un subconjunto de los canales de un registro de salida, se escribirán valores no definidos en los canales restantes.
-   Para ps \_ 3 \_ 0, los registros de oC# se pueden escribir con cualquier máscara de escritura.
-   Para ps 2 x y \_ ps 3 0, no puede escribir en registros de oC# y oD dentro del control de flujo dinámico o predicado \_ \_ (las escrituras en \_ \# oC# dentro del control de flujo estático están bien).
-   No puede realizar cálculos de degradado (u operaciones que invoque implícitamente cálculos de degradado como [texld - ps \_ 2 \_ 0 y](texld---ps-2-0.md)hacia arriba, [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) dentro de las instrucciones de control de flujo cuyas condiciones de bifurcación varían por primitiva (es decir, instrucciones de control de flujo dinámico). El predicado de instrucciones no se considera control de flujo dinámico.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Varios destinos de representación (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 