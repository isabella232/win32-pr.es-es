---
description: Los estados de efecto son pares nombre-valor en forma de expresión.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado del efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335579"
---
# <a name="effect-state-groups-direct3d-10"></a>Grupos de estado del efecto (Direct3D 10)

Los estados de efecto son pares nombre-valor en forma de expresión.

## <a name="blend-state"></a>Estado de blend

| Estado del efecto | Grupo |
|-|-|
| **ALPHATOCOVERAGEENABLE,** **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP,** **SRCBLEPHA,** **DESTBLEPHA,** **BLENDOPALPHA,** **RENDERTARGETWRITEMASK** | Miembros de [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Profundidad y estado de galería de símbolos

| Estado del efecto| Grupo |
|-|-|
| **DEPTHENABLE**, **DEPTHWRITEMASK,** **DEPTHFUNC,** **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK** | Miembros de [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| **FRONTFACESTENCICOHERENCIAIL,** **FRONTFACESTENCILZFAIL,** **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC,** **BACKFACESTENCINCIIL,** **BACKFACESTENCILZFAIL,** **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC** | Miembro de [ **D3D10 \_ DEPTH \_ STENCISTONE \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Estado del rasterizador

| Estado del efecto| Grupo |
|-|-|
| FILLMODE | [**MODO DE RELLENO D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**MODO CULL D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE,** **DEPTHBIAS**, DEPTHBIASCLAMP,SAMPLEEDDEPTHBIAS, **ZCLIPENABLE,SAMPLEENABLE,**  **MULTISAMPLEENABLE,** **ANTIALIASEDLINEENABLE**   | Miembros de [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Estado del muestreador

| Estado del efecto | Grupo |
|-|-|
| **Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc,** **BorderColor**, **MinLOD**, **MaxLOD** | Miembros de [ **D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Vea [Sampler type (DirectX HLSL) (Tipo de sampler [HLSL de DirectX])](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obtener ejemplos.

## <a name="effect-object-state"></a>Estado del objeto de efecto

| Este objeto de efecto | Se asigna a |
|-|-|
| RASTERIZERSTATE | Objeto [de estado de rasterizador.](#rasterizer-state) |
| DEPTHSTENCILSTATE | Objeto [de estado Depth y Stencil State.](#depth-and-stencil-state) |
| BLENDSTATE | Objeto [de estado de blend.](#blend-state) |
| VERTEXSHADER | Objeto de sombreador de vértices compilado. |
| PIXELSHADER | Objeto de sombreador de píxeles compilado. |
| GEOMETRYSHADER | Objeto de sombreador de geometría compilado. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Miembros de [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Definición y uso de objetos de estado

Los objetos de estado se declaran en archivos FX en el formato siguiente. *StateObjectType es* uno de los estados enumerados anteriormente y *MemberName* es el nombre de cualquier miembro que tenga un valor no predeterminado.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Por ejemplo, para configurar un objeto de estado de mezcla con AlphaToCoverageEnable y BlendEnable 0 establecidos en FALSE, se usaría \[ \] el código siguiente. 

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

El objeto de estado se aplica a un paso de técnica mediante una de las funciones SetStateGroup descritas en Sintaxis de técnica de [efecto (Direct3D 10).](d3d10-effect-technique-syntax.md) Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se usaría el código siguiente.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Para ver un tutorial en el que se describe el uso de estados, vea [Administración de estado.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)

## <a name="related-topics"></a>Temas relacionados

* [Sintaxis de la técnica de efecto](d3d10-effect-technique-syntax.md)
* [Formato de efecto (Direct3D 10)](d3d10-effect-format.md)
