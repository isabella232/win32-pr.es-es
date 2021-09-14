---
description: Los parámetros de la cola se controlan a través de los estados de representación del dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parámetros de parámetros de parámetros de destino (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964931"
---
# <a name="fog-parameters-direct3d-9"></a>Parámetros de parámetros de parámetros de destino (Direct3D 9)

Los parámetros de la cola se controlan a través de los estados de representación del dispositivo. Tanto los tipos de píxeles como los de vértice admiten todas las fórmulas de ánxeles introducidas en [Fórmulas de fórmulas de fórmulas (Direct3D 9)](fog-formulas.md). El [**tipo enumerado D3DFOGMODE**](./d3dfogmode.md) define constantes que se pueden usar para identificar la fórmula de fórmula de fórmula que quiere que use Microsoft Direct3D. El estado de representación D3DRS SHADERTABLEMODE controla el modo de navegación que Direct3D usa para píxeles de píxeles, y el estado de representación \_ de D3DRSVERTEXMODE controla el modo de \_ vértices.

Cuando se usa la fórmula linear de la cola, se establecen las distancias inicial y final a través de los estados de representación \_ D3DRSSTART y D3DRS \_ DAXEND. La forma en que el sistema interpreta estos valores depende del tipo de profundidad que usa la aplicación (píxel o vértice vértice) y, al usar píxeles de píxeles, si se usa profundidad basada en z o w. En la tabla siguiente se resumen los tipos de punto y sus unidades inicial y final.



| Tipo de bruma  | Unidades iniciales y finales de Extremo      |
|-----------|--------------------------|
| Píxel (Z) | Espacio del \[ dispositivo 0.0,1.0\] |
| Píxel (W) | Espacio de la cámara             |
| Vértice    | Espacio de la cámara             |



 

El estado de representación de D3DRS DAXDENSITY controla la densidad de densidad de densidad que se aplica cuando se habilita una \_ fórmula de curva exponencial. La densidad de densidad es básicamente un factor de ponderación, que va de 0,0 a 1,0 (ambos inclusive), que escala el valor de distancia en el exponente.

El color que el sistema usa para la mezcla de mezcla se controla a través del estado de representación del dispositivo \_ D3DRSCOLOR. Para obtener más información, vea [Color de fusión (Direct3D 9)](fog-color.md) y [Blending de Fusión (Direct3D 9).](fog-blending.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de tipos de](fog-types.md)
</dt> </dl>

 

 
