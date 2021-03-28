---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: El ensamblador de sombreador de píxeles se compone de un conjunto de instrucciones que operan en los datos de píxeles contenidos en los registros.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268242"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a>PS \_ 1 \_ , PS \_ 1 \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4

El ensamblador de sombreador de píxeles se compone de un conjunto de instrucciones que operan en los datos de píxeles contenidos en los registros. Las operaciones se expresan como instrucciones que se componen de un operador y de uno o varios operandos. Las instrucciones usan registros para transferir datos dentro y fuera del sombreador de píxeles ALU. Los registros también se pueden usar en algunas instrucciones para almacenar resultados temporales.

> [!Note]  
> La compatibilidad de HLSL con el sombreador de píxeles 1. x está en desuso.

 

## <a name="instructions"></a>Instrucciones

Hay dos categorías principales de instrucciones del sombreador de píxeles: Instrucciones aritméticas e instrucciones de direccionamiento de texturas. Las instrucciones aritméticas modifican los datos de color. Las operaciones de direccionamiento de texturas procesan datos de coordenadas de textura y, en la mayoría de los casos, muestra una textura. Las instrucciones del sombreador de píxeles se ejecutan por píxel; es decir, no tienen ningún conocimiento de otros píxeles en la canalización.

Las instrucciones de direccionamiento de texturas consumen una ranura, pero las instrucciones aritméticas se pueden emparejar para habilitar los componentes de color (RGB) y una instrucción de componente alfa en una sola ranura.

[las \_ instrucciones PS 1 \_ , PS 1 \_ \_ 2, PS 1 \_ \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contiene una lista de las instrucciones disponibles.

Cuando se habilita el muestreo múltiple, los sombreadores de píxeles solo se ejecutan una vez por píxel, no una vez para cada subpíxel. El muestreo múltiple solo aumenta la resolución de los bordes de polígono, así como las pruebas de profundidad y de estarcido. Por ejemplo, si está habilitado el muestreo múltiple de 3x3 y se detecta que un triángulo que se está rasterizando abarca cinco de los nueve subpíxeles de un píxel determinado, el sombreador de píxeles se ejecuta una vez y se aplica el mismo resultado de color a los cinco subpíxeles.

## <a name="registers"></a>Registros

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) muestra los distintos registros utilizados por el sombreador Alu.

## <a name="modifiers"></a>Modificadores

Los [modificadores para PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) se pueden usar para cambiar la funcionalidad de una instrucción o los datos se leen o se escriben en un registro.

Direct3D 9 requiere cálculos intermedios para mantener una precisión de 8 bits como mínimo para todos los formatos de superficie. Se recomienda la precisión superior (12 bits) para las matemáticas en la fase y la saturación a 8 bits entre las fases de textura. No se admiten los modos de redondeo ni las excepciones modificables. La multiplicación debe admitirse con una precisión de un paso a más cercano para mantener una pérdida de precisión mínima.

## <a name="sampler-count"></a>Recuento de muestras

El número de muestras de textura disponibles es:

-   Para PS \_ 1 \_ 0-PS \_ 1 \_ 3, el máximo es 4.
-   Para PS \_ 1 \_ 4, el máximo es 6.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sombreadores de píxeles](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




