---
description: Los parámetros de niebla se controlan a través de los Estados de representación del dispositivo.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Parámetros de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906544"
---
# <a name="fog-parameters-direct3d-9"></a>Parámetros de niebla (Direct3D 9)

Los parámetros de niebla se controlan a través de los Estados de representación del dispositivo. Los tipos de niebla de píxeles y vértices admiten todas las fórmulas de niebla introducidas en [fórmulas de niebla (Direct3D 9)](fog-formulas.md). El tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) define constantes que se pueden usar para identificar la fórmula de niebla que se desea que utilice Microsoft Direct3D. El estado de representación de D3DRS \_ FOGTABLEMODE controla el modo de niebla que Direct3D usa para la niebla de píxeles y el \_ Estado de representación de D3DRS FOGVERTEXMODE controla el modo de niebla de vértices.

Al usar la fórmula de niebla lineal, establezca las distancias inicial y final mediante los \_ Estados de representación D3DRS FOGSTART y D3DRS \_ FOGEND. La forma en que el sistema interprete estos valores depende del tipo de niebla que use la aplicación: la niebla de píxeles o de vértices y, cuando se usa la niebla de píxeles, si se usa la profundidad basada en z o en w. En la tabla siguiente se resumen los tipos de niebla y sus unidades de inicio y finalización.



| Tipo de niebla  | Unidades de inicio y finalización de niebla      |
|-----------|--------------------------|
| Píxel (Z) | Espacio \[ de dispositivo 0.0, 1.0\] |
| Píxel (W) | Espacio de la cámara             |
| Vértice    | Espacio de la cámara             |



 

El estado de representación de D3DRS \_ FOGDENSITY controla la densidad de niebla aplicada cuando se habilita una fórmula de niebla exponencial. La densidad de niebla es esencialmente un factor de ponderación, comprendido entre 0,0 y 1,0 (incluido), que escala el valor de distancia en el exponente.

El color que utiliza el sistema para la combinación de niebla se controla a través del \_ Estado de representación del dispositivo D3DRS FOGCOLOR. Para obtener más información, vea el [color de niebla (Direct3D 9)](fog-color.md) y la [combinación de niebla (Direct3D 9)](fog-blending.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de niebla](fog-types.md)
</dt> </dl>

 

 
