---
description: La distorsión visible en los elementos de textura de un objeto 3D cuya superficie está orientada en un ángulo con respecto al plano de la pantalla se denomina anisotropía.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtrado de textura anisotropica (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060770"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtrado de textura anisotropica (Direct3D 9)

La distorsión visible en los elementos de textura de un objeto 3D cuya superficie está orientada en un ángulo con respecto al plano de la pantalla se denomina anisotropía. Cuando un píxel de una primitiva anisotropica se asigna a los elementos texeles, su forma se distorsiona. Direct3D mide la anisotropía de un píxel como la elongación (es decir, la longitud dividida por ancho) de un píxel de pantalla asignado inversamente al espacio de textura.

Puede usar el filtrado de textura anisotropica junto con el filtrado de textura lineal o el filtrado de texturas mipmap para mejorar los resultados de la representación. La aplicación habilita el filtrado de texturas anisotropicas mediante una llamada [**al método IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que va a seleccionar un método de filtrado de textura. Pase D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER para el segundo parámetro para establecer el filtro \_ \_ de ampliación, minificación o mipmapping. Establezca el tercer parámetro en D3DTEXF \_ ANISOTROPIC.

La aplicación también debe establecer el grado de anisotropía en un valor mayor que uno. Para ello, llame al [**método IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Establezca el valor del primer parámetro en el número de índice entero (0-7) de la textura para la que está estableciendo el grado de isotropía. Pase D3DSAMP \_ MAXANISOTROPY como valor del segundo parámetro. El parámetro final debe ser el grado de isotropía.

Puede deshabilitar el filtrado isotropico estableciendo el grado de isotropía en uno. cualquier valor mayor que uno lo habilita. Compruebe la marca MaxAnisotropy en la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para determinar el posible intervalo de valores para el grado de anisotropía.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtrado de texturas](texture-filtering.md)
</dt> </dl>

 

 
