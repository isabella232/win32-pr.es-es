---
description: La distorsión visible en el textura de un objeto 3D cuya superficie está orientada en un ángulo con respecto al plano de la pantalla se denomina anisotropía.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtrado de texturas anisotrópico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496565"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtrado de texturas anisotrópico (Direct3D 9)

La distorsión visible en el textura de un objeto 3D cuya superficie está orientada en un ángulo con respecto al plano de la pantalla se denomina anisotropía. Cuando un píxel de un primitivo anisotrópico se asigna a textura, se distorsiona su forma. Direct3D mide el anisotropía de un píxel como el alargamiento, es decir, la longitud dividida por el ancho de un píxel de la pantalla que está inverso y se asigna a un espacio de textura.

Puede usar el filtrado de texturas anisotrópico junto con el filtrado de texturas lineal o el filtrado de texturas de mipmap para mejorar los resultados de la representación. La aplicación permite el filtrado de texturas anisotrópico llamando al método [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que está seleccionando un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER para el segundo parámetro con el fin de establecer el filtro de ampliación, minificación o mipmapping. Establezca el tercer parámetro en D3DTEXF \_ anisotrópico.

La aplicación también debe establecer el grado de anisotropía en un valor mayor que uno. Para ello, llame al método [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que está estableciendo el grado de isotropy. Pase D3DSAMP \_ MAXANISOTROPY como el valor del segundo parámetro. El parámetro final debe ser el grado de isotropy.

Puede deshabilitar el filtrado anisotrópico estableciendo el grado de isotropy en uno; cualquier valor mayor que uno lo habilita. Compruebe la marca MaxAnisotropy en la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar el intervalo posible de valores para el grado de anisotropía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de textura](texture-filtering.md)
</dt> </dl>

 

 
