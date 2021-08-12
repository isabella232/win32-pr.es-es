---
description: Cuando Direct3D representa una primitiva, asigna la primitiva 3D a una pantalla 2D.
ms.assetid: vs|directx_sdk|~\texture_filtering.htm
title: Filtrado de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758ee51df65ffa4dddf793db83fe618107886cd4c20497f0e8090373a1415beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291180"
---
# <a name="texture-filtering-direct3d-9"></a>Filtrado de textura (Direct3D 9)

Cuando Direct3D representa una primitiva, asigna la primitiva 3D a una pantalla 2D. Si la primitiva tiene una textura, Direct3D debe usar esa textura para generar un color para cada píxel de la imagen 2D representada de la primitiva. Para cada píxel de la imagen en pantalla de la primitiva, debe obtener un valor de color de la textura. Este proceso se denomina filtrado de textura.

Cuando se realiza una operación de filtro de textura, la textura que se usa normalmente también se amplía o se minifica. En otras palabras, se asigna a una imagen primitiva mayor o menor que ella misma. La ampliación de una textura puede dar lugar a que muchos píxeles se asignen a un elemento de textura. El resultado puede ser una apariencia fragmentada. La minificación de una textura a menudo significa que un solo píxel se asigna a muchos elementos de textura. La imagen resultante puede estar desenfoque o estar en alias. Para resolver estos problemas, se debe realizar alguna combinación de los colores del texel para llegar a un color para el píxel.

Direct3D simplifica el proceso complejo de filtrado de texturas. Proporciona tres tipos de filtrado de textura: filtrado lineal, filtrado anisotropico y filtrado de mapa mip. Si no selecciona ningún filtrado de textura, Direct3D usa una técnica denominada muestreo de punto más cercano.

Cada tipo de filtrado de textura tiene ventajas y desventajas. Por ejemplo, el filtrado de textura lineal puede producir bordes irregulares o una apariencia fragmentada en la imagen final. Sin embargo, es un método computacionalmente de baja sobrecarga de filtrado de textura. El filtrado con mapas MIP suele producir los mejores resultados, especialmente cuando se combina con el filtrado anisotropico. Sin embargo, requiere la mayor cantidad de memoria de las técnicas que admite Direct3D.

Las aplicaciones que usan punteros de interfaz de textura deben establecer el método de filtrado de textura actual llamando al [**método IDirect3DDevice9::SetSamplerState.**](/windows/desktop/api) Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que va a seleccionar un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER para el segundo parámetro para establecer el filtro \_ \_ de ampliación, minificación o mipmapping. Pase un miembro del [**tipo enumerado D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) como valor en el tercer parámetro.

En esta sección se presentan los métodos de filtrado de textura que admite Direct3D. Se organiza en los temas siguientes.

-   [Muestreo de punto más cercano (Direct3D 9)](nearest-point-sampling.md)
-   [Filtrado de textura lineal (Direct3D 9)](linear-texture-filtering.md)
-   [Filtrado de texturas bilineal (Direct3D 9)](bilinear-texture-filtering.md)
-   [Filtrado de textura anisotrófica (Direct3D 9)](anisotropic-texture-filtering.md)
-   [Filtrado de texturas con mapas Mip (Direct3D 9)](texture-filtering-with-mipmaps.md)

> [!Note]  
> Aunque los estados de representación de filtrado de textura presentes en el tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) se reemplazan por estados de fase de textura, [**IDirect3DDevice9::SetRenderState,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)en lugar de la versión IDirect3DDevice2, no genera un error si intenta usarlos. En su lugar, el sistema asigna los efectos de estos estados de representación a la primera fase de la cascada de varios texto, fase 0. Las aplicaciones no deben mezclar los estados de representación heredados con sus estados de fase de textura correspondientes, ya que pueden producirse resultados impredecibles.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
