---
description: Los Estados de efecto son pares nombre-valor en forma de expresión.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado del efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361947"
---
# <a name="effect-state-groups-direct3d-10"></a>Grupos de estado del efecto (Direct3D 10)

Los Estados de efecto son pares nombre-valor en forma de expresión.

## <a name="blend-state"></a>Estado de Blend

| | |
|-|-|
| **ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK** | Miembros de [ **D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Profundidad y estado de estarcido

| | |
|-|-|
| **DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK** | Miembros de la [ **Galería de símbolos de \_ profundidad D3D10 \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| FRONTFACESTENCILFAIL * *, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC** | Miembro de [ **D3D10 \_ Depth \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Estado del rasterizador

| | |
|-|-|
| FILLMODE | [**\_Modo de relleno de D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**\_Modo de selección de D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE** | Miembros de [ **D3D10 \_ rasterizador \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Estado de muestra

| | |
|-|-|
| **Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD** | Miembros de la [ **\_ muestra D3D10 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Consulte [tipo de muestra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obtener ejemplos.

## <a name="effect-object-state"></a>Estado del objeto de efecto

| Este objeto de efecto | Se asigna a |
|-|-|
| RASTERIZERSTATE | Objeto de estado de [Estado de rasterizador](#rasterizer-state) . |
| DEPTHSTENCILSTATE | Objeto de estado de [Estado de estarcido y de profundidad](#depth-and-stencil-state) . |
| BLENDSTATE | Objeto de estado de [Estado de Blend](#blend-state) . |
| VERTEXSHADER | Objeto de sombreador de vértices compilado. |
| U | Objeto de sombreador de píxeles compilado. |
| GEOMETRYSHADER | Objeto de sombreador de geometría compilado. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Miembros de [**D3D10 \_ Pass \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Definir y usar objetos de estado

Los objetos de estado se declaran en archivos FX con el siguiente formato. *StateObjectType* es uno de los Estados enumerados anteriormente y *memberName* es el nombre de cualquier miembro que tenga un valor no predeterminado.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Por ejemplo, para configurar un objeto de estado de Blend con AlphaToCoverageEnable y BlendEnable \[ 0 \] establecido en **false**, se utilizaría el código siguiente.

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

El objeto de estado se aplica a un paso de técnica mediante una de las funciones de SetStateGroup descritas en sintaxis de la [técnica de efectos (Direct3D 10)](d3d10-effect-technique-syntax.md). Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se utilizaría el código siguiente.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Para ver un tutorial en el que se describe el uso de Estados, consulte [Administración](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)de Estados.

## <a name="related-topics"></a>Temas relacionados

* [Sintaxis de la técnica de efectos](d3d10-effect-technique-syntax.md)
* [Formato de efecto (Direct3D 10)](d3d10-effect-format.md)
