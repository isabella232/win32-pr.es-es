---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: El ensamblador del sombreador de píxeles se forma de un conjunto de instrucciones que funcionan con los datos de píxeles contenidos en los registros.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e10e4eee48490e7ae998e39d71265aef74339c1979112e2fcf0e47e5b07cda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512946"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4

El ensamblador del sombreador de píxeles se forma de un conjunto de instrucciones que funcionan con los datos de píxeles contenidos en los registros. Las operaciones se expresan como instrucciones formadas por un operador y uno o varios operandos. Las instrucciones usan registros para transferir datos dentro y fuera del sombreador de píxeles ALU. Los registros también se pueden usar en algunas instrucciones para contener resultados temporales.

> [!Note]  
> La compatibilidad de HLSL con el sombreador de píxeles 1.x está en desuso.

 

## <a name="instructions"></a>Instructions

Hay dos categorías principales de instrucciones de sombreador de píxeles: instrucciones aritméticas e instrucciones de direccionamiento de textura. Las instrucciones aritméticas modifican los datos de color. Las operaciones de direccionamiento de textura procesan los datos de coordenadas de textura y, en la mayoría de los casos, muestrea una textura. Las instrucciones del sombreador de píxeles se ejecutan por píxel; es decir, no tienen ningún conocimiento de otros píxeles en la canalización.

Las instrucciones de direccionamiento de textura consumen una ranura, pero las instrucciones aritméticas se pueden emparejar para habilitar ambos componentes de color (RGB) y una instrucción de componente alfa en una sola ranura.

[ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ \_ 1 4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiene una lista de las instrucciones disponibles.

Cuando se habilita la multimuestreo, los sombreadores de píxeles solo se ejecutan una vez por píxel, no una vez por cada subpixel. El multimuestreo solo aumenta la resolución de los bordes del polígono, así como las pruebas de profundidad y galería de símbolos. Por ejemplo, si se habilita el multimuestreo de 3x3 y se encuentra un triángulo que se está rasterizado para cubrir cinco de los nueve subpíxeles de un píxel determinado, el sombreador de píxeles se ejecuta una vez y el mismo resultado de color se aplica a los cinco subpíxeles.

## <a name="registers"></a>Registros

[ps \_ 1 \_ 1 \_ \_ ps \_ 1 \_ 2 ps \_ \_ \_ 1 \_ 3 ps \_ \_ \_ 1 \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) enumera los distintos registros usados por el sombreador ALU.

## <a name="modifiers"></a>Modificadores

[Los modificadores de ps \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) se pueden usar para cambiar la funcionalidad de una instrucción o los datos leídos o escritos en un registro.

Direct3D 9 requiere cálculos intermedios para mantener al menos una precisión de 8 bits para todos los formatos de superficie. Se recomienda una precisión mayor (12 bits) para cálculos matemáticos en fase y una saturación de 8 bits entre fases de textura. No se admiten modos de redondeo modificables ni excepciones. La multiplicación debe ser compatible con una precisión de redondeo a la más cercana para mantener la pérdida de precisión al mínimo.

## <a name="sampler-count"></a>Recuento de muestreador

El número de muestreadores de textura disponibles es:

-   Para ps \_ 1 \_ 0 - ps \_ 1 \_ 3, el máximo es 4.
-   Para ps \_ 1 \_ 4, el máximo es 6.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




