---
description: Los efectos de niebla pueden dar mayor realismo a una escena 3D.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Estado de niebla (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422732"
---
# <a name="fog-state-direct3d-9"></a>Estado de niebla (Direct3D 9)

Los efectos de niebla pueden dar mayor realismo a una escena 3D. Puede usar efectos de niebla para más que simular la niebla. También pueden reducir la claridad de una escena con distancia. Esto refleja lo que sucede en el mundo real; a medida que los objetos van más alejados del usuario, sus detalles son menos distintos.

Para obtener más información sobre el uso de la niebla en la aplicación, vea [niebla (Direct3D 9)](fog.md).

Una aplicación de C++ controla la niebla a través de los Estados de representación de dispositivos. El tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye los Estados para controlar si se usa la niebla de píxel (tabla) o de vértices, el color que tiene, la fórmula de niebla que aplica el sistema y los parámetros de la fórmula.

Para habilitar la niebla, establezca el \_ Estado de representación de FOGENABLE de D3DRS en **true**. El color de niebla se puede establecer en cualquier valor de color mediante el \_ Estado de representación de D3DRS FOGCOLOR; se omite el componente alfa del color de niebla.

Los \_ Estados de representación D3DRS FOGTABLEMODE y D3DRS \_ FOGVERTEXMODE controlan la fórmula de niebla aplicada para los cálculos de niebla y controlan indirectamente qué tipo de niebla se aplica. Ambos Estados de representación se pueden establecer en un miembro del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . Al establecer el estado de representación en D3DFOG \_ None, se deshabilita la niebla de píxel o de vértices, respectivamente. Si ambos Estados de representación están establecidos en modos válidos, el sistema aplica solo los efectos de niebla de píxeles.

Los \_ \_ parámetros de la fórmula de niebla de control D3DRS FOGSTART y D3DRS FOGEND para el \_ modo lineal D3DFOG. El estado de representación de D3DRS \_ FOGDENSITY controla la densidad de niebla en los modos de niebla exponencial.

Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estados de representación](render-states.md)
</dt> </dl>

 

 
