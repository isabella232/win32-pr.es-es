---
description: Los efectos de efecto de efecto pueden dar mayor realismo a una escena 3D.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Estado de la infusión (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964928"
---
# <a name="fog-state-direct3d-9"></a>Estado de la infusión (Direct3D 9)

Los efectos de efecto de efecto pueden dar mayor realismo a una escena 3D. Puede usar efectos de efecto para algo más que simular el sonido. También pueden reducir la claridad de una escena con distancia. Esto refleja lo que sucede en el mundo real. A medida que los objetos se distancian más del usuario, sus detalles son menos distintos.

Para obtener más información sobre el uso de la nube en la aplicación, vea [Decir (Direct3D 9).](fog.md)

Una aplicación de C++ controla los estados de representación de dispositivos. El tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye estados para controlar si se usan píxeles (tabla) o vértices, de qué color es, de qué color se aplica el sistema y de los parámetros de la fórmula.

Para habilitar el estado de representación de \_ D3DRSEVEENABLE, debe establecerse en **TRUE.** El color de color de color se puede establecer en cualquier valor de color mediante el estado de representación D3DRSCOLORCOLOR; se omite el componente alfa \_ del color de color.

Los estados de representación D3DRS \_ KANBANTABLEMODE y D3DRS KANBANVERTEXMODE controlan la fórmula de matriz aplicada para los cálculos de cálculo, y controlan indirectamente qué tipo de vertía se \_ aplica. Ambos estados de representación se pueden establecer en un miembro del tipo [**enumerado D3DFOGMODE.**](./d3dfogmode.md) Al establecer el estado de representación en D3DFOG NONE, se deshabilitan los \_ píxeles o vértices, respectivamente. Si ambos estados de representación están establecidos en modos válidos, el sistema solo aplica efectos de píxeles de píxel.

Los parámetros de fórmula de control de estados de representación \_ D3DRSSTART y D3DRS DAXSTART para el modo \_ LINEAR D3DFOG. \_ El estado de representación DE D3DRSRDDENSITY controla la densidad de densidad de densidad en \_ los modos de curva exponencial.

Para obtener más información, vea [Parámetros de Parámetros de parámetros de parámetros de Parámetros de parámetros (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representar estados](render-states.md)
</dt> </dl>

 

 
