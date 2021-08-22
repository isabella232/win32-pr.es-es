---
description: Las aplicaciones de Direct3D pueden lograr numerosos efectos especiales mediante la aplicación de varias texturas a una primitiva a lo largo de varios pases de representación.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Mezcla de textura multipass (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ec4916cb3c86c0e3aa6e2c6ab9a5e03de8304989391b9c80b1070fc7b51594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491525"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Mezcla de textura multipass (Direct3D 9)

Las aplicaciones de Direct3D pueden lograr numerosos efectos especiales mediante la aplicación de varias texturas a una primitiva a lo largo de varios pases de representación. El término común para esto es la mezcla de textura multipass. Un uso típico de la mezcla de textura multipass es emular los efectos de la iluminación compleja y los modelos de sombreado mediante la aplicación de varios colores de varias texturas diferentes. Una de estas aplicaciones se denomina asignación de luz. Para obtener más información, vea [Asignación de luz con texturas (Direct3D 9).](light-mapping-with-textures.md)

> [!Note]  
> Algunos dispositivos son capaces de aplicar varias texturas a las primitivas en un solo paso. Para obtener más información, vea [Mezcla de texturas (Direct3D 9).](texture-blending.md)

 

Si el hardware del usuario no admite la mezcla de varias texturas, la aplicación puede usar la mezcla de textura multipass para lograr los mismos efectos visuales. Sin embargo, la aplicación no puede mantener las velocidades de fotogramas que son posibles cuando se usa la combinación de varias texturas.

Para realizar la mezcla de textura multipass en una aplicación de C/C++.

1.  Establezca una textura en la fase de textura 0 llamando al [**método IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)
2.  Seleccione los argumentos y las operaciones de combinación alfa y color deseados con el método [**IDirect3DDevice9::SetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) La configuración predeterminada es adecuada para la mezcla de textura multipass.
3.  Represente los objetos adecuados en la escena.
4.  Establezca la siguiente textura en la fase de textura 0.
5.  Establezca los estados de representación D3DRS \_ SRCBLEND y D3DRS DESTBLEND para ajustar los factores de combinación de origen y destino según \_ sea necesario. El sistema combina las nuevas texturas con los píxeles existentes en la superficie de destino de representación según estos parámetros.
6.  Repita los pasos 3, 4 y 5 con tantas texturas como sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mezcla de texturas](texture-blending.md)
</dt> </dl>

 

 
