---
title: Grupos de estados de efecto (Direct3D 11)
description: Los estados de efecto son pares de valor de nombre en forma de expresión.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efecto, grupos de estados (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335345"
---
# <a name="effect-state-groups-direct3d-11"></a>Grupos de estados de efecto (Direct3D 11)

Los estados de efecto son pares de valor de nombre en forma de expresión.

-   [Estado de blend](#blend-state)
-   [Profundidad y estado de galería de símbolos](#depth-and-stencil-state)
-   [Estado del rasterizador](#rasterizer-state)
-   [Estado del muestreador](#sampler-state)
-   [Estado del objeto de efecto](#effect-object-state)
-   [Definición y uso de objetos de estado](#defining-and-using-state-objects)
-   [Temas relacionados](#related-topics)

## <a name="blend-state"></a>Estado de blend



| Estado del efecto                                                                                                                      | Grupo                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLEPHADESTBLEPHABLENDOPALPHARENDERTARGETWRITEMASK | Miembros de [ **D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Profundidad y estado de galería de símbolos



|  Estado del efecto                                                                                                                                                              | Grupo                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Miembros de [ **D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCINCIILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCINCIILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFACESTENCILFUNC | Miembro de [ **D3D11 \_ DEPTH \_ STENCISTONE \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Estado del rasterizador



| Estado del efecto                                                                                                                                | Grupo                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FILLMODE                                                                                                                        | [**MODO DE RELLENO D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**MODO CULL D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSSTONEESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Miembros de [ **D3D11 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Estado del muestreador



| Estado del efecto                                                                                                    | Grupo                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Miembros de [ **D3D11 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Vea [Sampler Type (DirectX HLSL) (Tipo de sampler [HLSL de DirectX])](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para obtener ejemplos.

## <a name="effect-object-state"></a>Estado del objeto de efecto



| Este objeto de efecto                          | Se asigna a                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Objeto [de estado de rasterizador.](#rasterizer-state)               |
| DEPTHSTENCILSTATE                           | Objeto [de estado Depth y Stencil State.](#depth-and-stencil-state) |
| BLENDSTATE                                  | Objeto [de estado de blend.](#blend-state)                         |
| VERTEXSHADER                                | Objeto de sombreador de vértices compilado.                                    |
| PIXELSHADER                                 | Objeto de sombreador de píxeles compilado.                                     |
| GEOMETRYSHADER                              | Objeto de sombreador de geometría compilado.                                  |
| DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK | Miembros de [**D3DX11 \_ PASS \_ DESC**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Definición y uso de objetos de estado

Los objetos de estado se declaran en archivos FX con el formato siguiente. StateObjectType es uno de los estados enumerados anteriormente y MemberName es el nombre de cualquier miembro que tenga un valor no predeterminado.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Por ejemplo, para configurar un objeto de estado de mezcla con AlphaToCoverageEnable y BlendEnable 0 establecido en FALSE, se usaría \[ \] el código siguiente. 


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



El objeto de estado se aplica a un paso de técnica mediante una de las funciones SetStateGroup descritas en Sintaxis de técnica de [efecto (Direct3D 11).](d3d11-effect-technique-syntax.md) Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se usaría el código siguiente.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de la técnica de efecto](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Formato de efecto (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 