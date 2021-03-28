---
title: Métodos 10Level9 ID3D11Device
description: En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421155"
---
# <a name="10level9-id3d11device-methods"></a>Métodos 10Level9 ID3D11Device

En esta sección se enumeran las diferencias entre cada nivel de característica de 10Level9 y el nivel \_ \_ de característica de D3D \_ 11 \_ 0 y el nivel de características superior para los métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

-   [ID3D11Device:: CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device:: CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device:: CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device:: CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device:: CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device:: CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device:: CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device:: CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device:: CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device:: CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device:: CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device:: CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device:: CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device:: CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device:: CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device:: CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device:: CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device:: CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device:: CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device:: CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device:: CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device:: CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device:: CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device:: CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device:: CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device:: OpenSharedResource](#id3d11deviceopensharedresource)
-   [Temas relacionados](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device:: CheckCounter



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Los contadores dependientes del dispositivo se admiten opcionalmente. Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: CheckCounterInfo</strong></a> para determinar la compatibilidad. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device:: CheckFormatSupport



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Consulte compatibilidad con el formato de <a href="overviews-direct3d-11-devices-downlevel-intro.md">nivel de característica</a>$ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device:: CheckMultisampleQualityLevels



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Los niveles de características no ofrecen ninguna garantía sobre el soporte técnico de MSAA. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device:: CreateBlendState



| Nivel de características              | Diferencias de comportamiento                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1  | AlphaToCoverageEnable debe ser **false**.<br/> Los primeros cuatro BlendEnables deben tener el mismo valor.<br/> \_No se admite D3D11 Blend \_ src \_ ALPHASAT.<br/> No se admite la mezcla de colores de doble origen (cualquier SrcBlend o DestBlend con SRC1 en el nombre)<br/>                                                                                |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2  | AlphaToCoverageEnable debe ser **false**.<br/> Los primeros cuatro BlendEnables deben tener el mismo valor.<br/> Los primeros cuatro RenderTargetWriteMasks deben tener el mismo valor.<br/> \_No se admite D3D11 Blend \_ src \_ ALPHASAT.<br/> No se admite la mezcla de colores de doble origen (cualquier SrcBlend o DestBlend con SRC1 en el nombre)<br/> |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3  | AlphaToCoverageEnable debe ser **false**.<br/> Los primeros cuatro BlendEnables deben tener el mismo valor.<br/> \_No se admite D3D11 Blend \_ src \_ ALPHASAT.<br/> No se admite la mezcla de colores de doble origen (cualquier SrcBlend o DestBlend con SRC1 en el nombre)<br/>                                                                                |
| Nivel de característica de D3D \_ \_ \_ 10 \_ 0 | Agrega alfa a cobertura                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device:: CreateBlendState1



| Nivel de características              | Diferencias de comportamiento                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1  | No compatible<br/>                                                                                                                                                                                                                                                                                                                                       |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2  | No compatible<br/>                                                                                                                                                                                                                                                                                                                                       |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3  | No compatible<br/>                                                                                                                                                                                                                                                                                                                                       |
| Nivel de característica de D3D \_ \_ \_ 10 \_ 0 | El miembro *OutputMergerLogicOp* se ha agregado a [**\_ \_ \_ \_ las opciones de D3D11 de datos de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), para determinar la compatibilidad con las operaciones lógicas (operaciones de lógica bit a bit entre el resultado del sombreador de píxeles y el contenido de destino de representación, consulte [**D3D11 \_ Render \_ target \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device:: CreateBuffer



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Los búferes no pueden tener vistas de destino de representación.<br/> Los búferes deben tener exactamente uno de D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br/> Solo permite búferes de índice con el formato de DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Los búferes no pueden tener vistas de destino de representación.<br/> Los búferes deben tener exactamente uno de D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br/> Permite búferes de índice con los formatos DXGI_FORMAT_R16_UINT y DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 y versiones posteriores. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device:: CreateCounter



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device:: CreateDepthStencilView



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No admite la galería de símbolos de dos caras. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device:: CreateDomainShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en cualquier nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device:: CreateGeometryShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device:: CreateGeometryShaderWithStreamOutput



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device:: CreateHullShader



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">No se admite en ningún nivel de características 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device:: CreateInputLayout



| Nivel de características             | Diferencias de comportamiento                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | No admite datos de \_ entrada D3D11 \_ por \_ instancia \_                                                                |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | No admite datos de \_ entrada D3D11 \_ por \_ instancia \_                                                                |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | El flujo de vértices cero debe tener \_ una entrada D3D11 \_ por \_ \_ datos de vértice, si alguna secuencia tiene una \_ entrada D3D11 \_ por \_ datos de vértice \_ |



 

Para más información sobre los formatos que se pueden usar para los datos de vértices en cada nivel de característica, vea el gráfico compatibilidad con el formato de [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) .

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device:: CreatePixelShader



| Nivel de características             | Diferencias de comportamiento                                    |
|---------------------------|---------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | Debe usar PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | Debe usar PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | Debe usar PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 3 o PS \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device:: CreatePredicate



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a>ID3D11Device:: CreateQuery



| Nivel de características             | Diferencias de comportamiento                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | Se admiten las consultas de eventos. Las consultas de marca de tiempo son opcionales: llame a [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad.               |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | Se admiten las consultas de eventos y de oclusión. Las consultas de marca de tiempo son opcionales: llame a [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad. |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | Se admiten las consultas de eventos y de oclusión. Las consultas de marca de tiempo son opcionales: llame a [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device:: CreateRasterizerState



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">DepthClipEnable debe ser <strong>true</strong>. DepthBiasClamp debe establecerse en 0. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device:: CreateRenderTargetView



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Solo puede admitir vistas de destino de representación de objetos Texture2D. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device:: CreateSamplerState



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>No se admite el filtro de comparación.<br/> El color del borde debe estar comprendido entre [0, 1]<br/> El LOD mínimo no puede ser fraccionario<br/> El máximo de LOD debe ser FLT_MAX<br/> El valor máximo de anisotropía es 2.<br/> D3D11_TEXTURE_ADDRESS_MIRRORONCE no se admiten.<br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> No se admite el filtro de comparación.<br/> El color del borde debe estar comprendido entre [0, 1]<br/> El LOD mínimo no puede ser fraccionario<br/> El máximo de LOD debe ser FLT_MAX<br/> El valor máximo de anisotropía es 16.<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device:: CreateShaderResourceView



| Nivel de características             | MostDetailedMip Plus MipLevels debe incluir el valor de LOD más bajo (subrecurso más pequeño | La vista debe incluir todos los elementos de la matriz de recursos |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | Sí                                                                          | sí                                           |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | Sí                                                                          | Sí                                           |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | Sí                                                                          | Sí                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device:: CreateTexture1D



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device:: CreateTexture2D

Los recursos de Texture2D tienen límites en el ancho y el alto que difieren entre [los niveles de características](overviews-direct3d-11-devices-downlevel-intro.md). En los niveles de características 9 \_ 3, los siguientes son mínimos garantizados y las implementaciones individuales pueden superar los requisitos.



| Nivel de características             | Si MipCount > 1, las dimensiones deben ser potencia integral de dos. | Dimensión de textura mínima admitida | Las dimensiones de las texturas del cubo deben ser potencia de dos | Si \_ se establece varios TEXTURECUBE, el valor de tamaño es: | Si \_ no se establece TEXTURECUBE, el valor de tamaño es. |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | Sí                                                          | 2048                                | Sí                                           | 6                                              | 1                                                  |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | Sí                                                          | 2048                                | Sí                                           | 6                                              | 1                                                  |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | Sí                                                          | 4096                                | Sí                                           | 6                                              | 1                                                  |



 

En la tabla anterior, el nombre completo de **\_ TEXTURECUBE** es [**D3D11 \_ Resource \_ Misc \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Lo siguiente es cierto para los 9 \_ \* [niveles de características](overviews-direct3d-11-devices-downlevel-intro.md):

-   Cuando se usa \_ el \_ valor predeterminado de uso de D3D11 o el \_ uso \_ de D3D11 inmutable, BindFlags no puede ser cero.
-   Al usar la \_ \_ \_ Galería de símbolos de profundidad de enlace de D3D11, MipLevels debe ser 1.
-   Al usar el \_ \_ \_ recurso de sombreador de enlace de D3D11, SampleDesc. Count debe ser 1.
-   Cuando se usa el \_ enlace D3D11 \_ presente, el recurso no puede tener el \_ recurso de sombreador de enlace D3D11 \_ \_ .
-   Cuando se usa \_ el \_ recurso D3D10 DDI \_ varios \_ compartido, el formato no puede ser dxgi \_ format \_ R8G8B8A8 \_ UNORM o dxgi \_ format \_ R8G8B8A8 \_ UNORM \_ sRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device:: CreateTexture3D



| Nivel de características             | Dimensión máxima (cualquier eje) | Las dimensiones deben ser potencia de dos |
|---------------------------|------------------------------|---------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | 256                          | Sí                             |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | 512                          | Sí                             |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | 512                          | Sí                             |



 

Si el recurso es \_ un \_ valor predeterminado de uso de D3D11 o el \_ uso de D3D11 es \_ inmutable, BindFlags no puede ser cero.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device:: CreateUnorderedAccessView



<table>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">No se admite en cualquier nivel de características 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device:: CreateVertexShader



| Nivel de características             | Diferencias de comportamiento                                    |
|---------------------------|---------------------------------------------------------|
| Nivel de característica de D3D \_ \_ \_ 9 \_ 1 | Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 2 | Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| Nivel de característica de D3D \_ \_ \_ 9 \_ 3 | Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 3 o vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device:: OpenSharedResource



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nivel de características</th>
<th>Diferencias de comportamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> con el valor <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> y la estructura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> para determinar si se puede compartir un formato. Si el formato se puede compartir, <strong>CheckFeatureSupport</strong> devuelve la marca <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .<br/>
<blockquote>
[!Note]<br />
[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) y <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> nunca se pueden compartir cuando se usa el nivel de característica 9, incluso si el dispositivo indica compatibilidad con características opcionales para <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. Al intentar crear recursos compartidos con formatos de DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> y <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> , siempre se producirá un error a menos que el nivel de característica sea 10_0 o superior.
</blockquote>
<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

