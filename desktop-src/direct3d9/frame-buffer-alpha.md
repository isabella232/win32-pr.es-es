---
description: La mezcla alfa del búfer de fotogramas es un poco diferente que el vértice alfa, el alfa del material y la textura alfa.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Búfer de trama alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152115"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Búfer de trama alfa (Direct3D 9)

La mezcla alfa del búfer de fotogramas es un poco diferente que el vértice alfa, el alfa del material y la textura alfa. Los valores de transparencia de vértices, materiales y texturas que se usan solo para el primitivo actual y no tienen ningún efecto en otros tipos primitivos. La mezcla alfa de búfer de fotogramas controla cómo se combina el primitivo actual con los píxeles existentes en el búfer de fotogramas para producir un color de píxel final.

Al realizar la combinación alfa, se combinan dos colores: un color de origen y un color de destino. El color de origen es del objeto transparente, el color de destino es el color que ya está en la ubicación de píxeles. El color de destino es el resultado de representar algún otro objeto situado detrás del objeto transparente, es decir, el objeto que será visible a través del objeto transparente. La combinación alfa utiliza una fórmula para controlar la relación entre los objetos de origen y de destino.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor es la contribución de la primitiva que se representa en la ubicación de píxeles actual. PixelColor es la contribución del búfer de fotogramas en la ubicación de píxeles actual.

A continuación se enumera el conjunto de factores de mezcla alfa que se pueden usar.



| Factor de modo de mezcla         | Descripción                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ cero            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ uno             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (RS, GS, BS, as)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1-RS, 1-GS, 1-BS, 1-as)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (Como, como, como)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-as, 1-as, 1-as, 1-as)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (Ad, ad, ad, ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1: AD, 1: AD, 1: AD, 1-ad)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (Rd, GD, BD, ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-GD, 1-BD, 1-ad)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min (as, 1-ad)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Obsoleto para DirectX 6 y versiones posteriores. Puede lograr el mismo efecto si establece los factores de mezcla de origen y destino en D3DBLEND \_ SRCALPHA y D3DBLEND \_ INVSRCALPHA en llamadas independientes. |
| D3DBLEND \_ BOTHINVSRCALPHA | Obsoleto para DirectX 6. Puede lograr el mismo efecto si establece los factores de mezcla de origen y destino en D3DBLEND \_ INVSRCALPHA y D3DBLEND \_ SRCALPHA en llamadas independientes.           |
| D3DBLEND \_ BLENDFACTOR     | Use color. r, color. g, color. b y color. Obtenido de la configuración de BLENDFACTOR de D3DRS \_ .                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Use 1-color. r, 1-color. g, 1-color. b y 1-color. obtenido del valor BLENDFACTOR de D3DRS \_ .                                                                                         |



 

Direct3D usa el \_ Estado de representación de ALPHABLENDENABLE de D3DRS para habilitar la combinación de transparencia alfa. El tipo de combinación alfa que se realiza depende de los Estados de \_ representación D3DRS SRCBLEND y D3DRS \_ DESTBLEND. Los Estados de mezcla de origen y destino se usan en pares. El siguiente fragmento de código establece el estado de Blend de origen en D3DBLEND \_ SRCCOLOR y el estado de Blend de destino en D3DBLEND \_ INVSRCCOLOR.


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



Este código realiza una mezcla lineal entre el color de origen (el color de la primitiva que se representa en la ubicación actual) y el color de destino (el color de la ubicación actual en el búfer de marco). La apariencia resultante es similar a la del matiz con matices en el hecho de que parte del color del objeto de destino parezca transmitirse a través del objeto de origen. el resto de ellos parece ser absorbido.

Muchos de estos factores de mezcla requieren valores alfa en la textura para que funcionen correctamente. Por lo tanto, cuando se usa el vértice o el alfa del material, la aplicación se restringe en qué modos se producirán resultados interesantes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación alfa](alpha-blending.md)
</dt> </dl>

 

 



