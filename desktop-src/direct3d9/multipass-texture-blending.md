---
description: Las aplicaciones de Direct3D pueden lograr numerosos efectos especiales aplicando varias texturas a una primitiva en el transcurso de varias fases de representación.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Combinación de texturas de Multipass (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152320"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Combinación de texturas de Multipass (Direct3D 9)

Las aplicaciones de Direct3D pueden lograr numerosos efectos especiales aplicando varias texturas a una primitiva en el transcurso de varias fases de representación. El término común para esto es Multipass Texture blending. Un uso típico de la combinación de texturas de Multipass es emular los efectos de los modelos de iluminación y sombreado complejos mediante la aplicación de varios colores de varias texturas diferentes. Una de estas aplicaciones se denomina asignación ligera. Para obtener más información, vea [asignación de luz con texturas (Direct3D 9)](light-mapping-with-textures.md).

> [!Note]  
> Algunos dispositivos pueden aplicar varias texturas a primitivos en un solo paso. Para obtener más información, vea [combinación de texturas (Direct3D 9)](texture-blending.md).

 

Si el hardware del usuario no admite varias combinaciones de texturas, la aplicación puede usar la combinación de texturas Multipass para lograr los mismos efectos visuales. Sin embargo, la aplicación no puede admitir las velocidades de fotogramas que son posibles cuando se usa la combinación de texturas múltiples.

Para realizar la combinación de texturas de Multipass en una aplicación de C/C++.

1.  Establezca una textura en la fase de textura 0 llamando al método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .
2.  Seleccione el color deseado y los argumentos y las operaciones de combinación alfa con el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) . La configuración predeterminada es adecuada para la combinación de texturas de Multipass.
3.  Representar los objetos adecuados en la escena.
4.  Establezca la siguiente textura en la fase de textura 0.
5.  Establezca los \_ Estados de representación D3DRS SRCBLEND y D3DRS \_ DESTBLEND para ajustar los factores de mezcla de origen y destino según sea necesario. El sistema combina las nuevas texturas con los píxeles existentes en la superficie de representación-destino según estos parámetros.
6.  Repita los pasos 3, 4 y 5 con tantas texturas como sea necesario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Combinación de texturas](texture-blending.md)
</dt> </dl>

 

 
