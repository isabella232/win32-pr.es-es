---
description: La combinación alfa del búfer de fotogramas es un poco diferente de alfa de vértice, alfa de material y alfa de textura.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Búfer de fotogramas alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565993"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Búfer de fotogramas alfa (Direct3D 9)

La combinación alfa del búfer de fotogramas es un poco diferente de alfa de vértice, alfa de material y alfa de textura. Los valores de transparencia del conjunto alfa de vértice, material y textura solo se usan para la primitiva actual y, por sí mismos, no tienen ningún efecto en otras primitivas. La combinación alfa del búfer de fotogramas controla cómo se combina la primitiva actual con los píxeles existentes en el búfer de fotogramas para producir un color de píxel final.

Al realizar la combinación alfa, se combinan dos colores: un color de origen y un color de destino. El color de origen es del objeto transparente, el color de destino es el color que ya se encuentra en la ubicación de píxeles. El color de destino es el resultado de representar otro objeto que está detrás del objeto transparente, es decir, el objeto que será visible a través del objeto transparente. La combinación alfa usa una fórmula para controlar la relación entre los objetos de origen y de destino.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor es la contribución de la primitiva que se representa en la ubicación de píxeles actual. PixelColor es la contribución del búfer de fotogramas en la ubicación de píxeles actual.

A continuación se muestra el conjunto de factores de combinación alfa que se pueden usar.



| Factor de modo de mezcla         | Descripción                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ ZERO            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ ONE             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (Rs, Gs, Bs, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1-Rs, 1-Gs, 1-Bs, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (As, As, As, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-As, 1-As, 1-As, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (Ad, Ad, Ad, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1-Ad, 1-Ad, 1-Ad, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (Rd, Gd, Bd, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-Gd, 1-Bd, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min(As, 1-Ad)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Obsoleto para DirectX 6 y versiones posteriores. Puede lograr el mismo efecto estableciendo los factores de combinación de origen y destino en D3DBLEND \_ SRCALPHA y D3DBLEND \_ INVSRCALPHA en llamadas independientes. |
| D3DBLEND \_ BOTHINVSRCALPHA | Obsoleto para DirectX 6. Puede lograr el mismo efecto estableciendo los factores de combinación de origen y destino en D3DBLEND \_ INVSRCALPHA y D3DBLEND SRCALPHA en llamadas \_ independientes.           |
| D3DBLEND \_ BLENDFACTOR     | Use color.r, color.g, color.b y color.a obtenidos de la configuración \_ DE BLENDFACTOR de D3DRS.                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Use 1-color.r, 1-color.g, 1-color.b y 1-color.a obtenido de la configuración BLENDFACTOR de D3DRS. \_                                                                                         |



 

Direct3D usa el estado de representación ALPHABLENDENABLE de D3DRS \_ para habilitar la combinación de transparencia alfa. El tipo de combinación alfa que se realiza depende de los estados de representación D3DRS \_ SRCBLEND y D3DRS \_ DESTBLEND. Los estados de combinación de origen y destino se usan en pares. El fragmento de código siguiente establece el estado de mezcla de origen en D3DBLEND SRCCOLOR y el estado de mezcla de destino \_ en D3DBLEND \_ INVSRCCOLOR.


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



Este código realiza una combinación lineal entre el color de origen (el color de la primitiva que se representa en la ubicación actual) y el color de destino (el color de la ubicación actual en el búfer del marco). El aspecto resultante es similar al de un cristal en el que parte del color del objeto de destino parece transmitirse a través del objeto de origen. el resto parece ser desmesado.

Muchos de estos factores de combinación requieren que los valores alfa de la textura funcionen correctamente. Por lo tanto, al usar vértices o materiales alfa, la aplicación está restringida en cuanto a qué modos producirá resultados interesantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Alpha Blending](alpha-blending.md)
</dt> </dl>

 

 



