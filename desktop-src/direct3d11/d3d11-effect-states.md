---
title: Grupos de Estados de efectos (Direct3D 11)
description: Los Estados de efecto son pares de nombre y valor en forma de expresión.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efecto, grupos de Estados (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995282"
---
# <a name="effect-state-groups-direct3d-11"></a>Grupos de Estados de efectos (Direct3D 11)

Los Estados de efecto son pares de nombre y valor en forma de expresión.

-   [Estado de Blend](#blend-state)
-   [Profundidad y estado de estarcido](#depth-and-stencil-state)
-   [Estado del rasterizador](#rasterizer-state)
-   [Estado de muestra](#sampler-state)
-   [Estado del objeto de efecto](#effect-object-state)
-   [Definir y usar objetos de estado](#defining-and-using-state-objects)
-   [Temas relacionados](#related-topics)

## <a name="blend-state"></a>Estado de Blend



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | Miembros de [ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Profundidad y estado de estarcido



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Miembros de la [ **Galería de símbolos de \_ profundidad D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | Miembro de [ **D3D11 \_ Depth \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Estado del rasterizador



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FILLMODE                                                                                                                        | [**\_Modo de relleno de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**\_Modo de selección de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Miembros de [ **D3D11 \_ rasterizador \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Estado de muestra



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Miembros de la [ **\_ muestra D3D11 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Consulte [tipo de muestra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para obtener ejemplos.

## <a name="effect-object-state"></a>Estado del objeto de efecto



| Este objeto de efecto                          | Se asigna a                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Objeto de estado de [Estado de rasterizador](#rasterizer-state) .               |
| DEPTHSTENCILSTATE                           | Objeto de estado de [Estado de estarcido y de profundidad](#depth-and-stencil-state) . |
| BLENDSTATE                                  | Objeto de estado de [Estado de Blend](#blend-state) .                         |
| VERTEXSHADER                                | Objeto de sombreador de vértices compilado.                                    |
| U                                 | Objeto de sombreador de píxeles compilado.                                     |
| GEOMETRYSHADER                              | Objeto de sombreador de geometría compilado.                                  |
| \_STENCILREFAB DS \_ BLENDFACTORAB \_ SAMPLEMASK | Miembros de [**D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Definir y usar objetos de estado

Los objetos de estado se declaran en archivos FX con el siguiente formato. StateObjectType es uno de los Estados enumerados anteriormente y MemberName es el nombre de cualquier miembro que tenga un valor no predeterminado.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Por ejemplo, para configurar un objeto de estado de Blend con AlphaToCoverageEnable y BlendEnable \[ 0 \] establecido en **false** , se utilizaría el código siguiente.


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



El objeto de estado se aplica a un paso de técnica mediante una de las funciones de SetStateGroup descritas en sintaxis de la [técnica de efectos (Direct3D 11)](d3d11-effect-technique-syntax.md). Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se utilizaría el código siguiente.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis de la técnica de efectos](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Formato de efecto (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 