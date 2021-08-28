---
title: Métodos 10Level9 ID3D11Device
description: En esta sección se enumeran las diferencias entre cada nivel de característica 10Level9 y el nivel de característica D3D FEATURE LEVEL 11 0 y superior para los \_ \_ \_ \_ métodos ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467e47d7ba623f1c28111cf3bf7cc6a07da8317
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475791"
---
# <a name="10level9-id3d11device-methods"></a>Métodos 10Level9 ID3D11Device

En esta sección se enumeran las diferencias entre cada nivel de característica 10Level9 y el nivel de característica D3D FEATURE LEVEL 11 0 y superior para los \_ \_ \_ \_ [**métodos ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

-   [ID3D11Device::CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device::CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device::CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device::CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device::CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device::CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device::CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device::CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device::CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device::CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device::CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device::CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device::CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device::CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device::CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device::CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device::CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device::CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device::CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device::CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device::CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device::CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device::CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device::CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device::CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device::OpenSharedResource](#id3d11deviceopensharedresource)
-   [Temas relacionados](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device::CheckCounter




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Opcionalmente, se admiten contadores dependientes del dispositivo. Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo para</strong></a> determinar support.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device::CheckFormatSupport




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Consulte compatibilidad con formato por <a href="overviews-direct3d-11-devices-downlevel-intro.md">nivel de característica</a>${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device::CheckMultisampleQualityLevels




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Los niveles de características no garantizan la compatibilidad con MSAA.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device::CreateBlendState



| Nivel de característica              | Diferencias de comportamiento                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1  | AlphaToCoverageEnable debe ser **FALSE.**<br/> Los cuatro primeros BlendEnables deben tener el mismo valor.<br/> No se admite D3D11 \_ BLEND \_ SRC \_ ALPHASAT.<br/> No se admite la combinación de colores de origen dual (cualquier SrcBlend o DestBlend con SRC1 en el nombre)<br/>                                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | AlphaToCoverageEnable debe ser **FALSE.**<br/> Los cuatro primeros BlendEnables deben tener el mismo valor.<br/> Las cuatro primeras RenderTargetWriteMasks deben tener el mismo valor.<br/> No se admite D3D11 \_ BLEND \_ SRC \_ ALPHASAT.<br/> No se admite la combinación de colores de origen dual (cualquier SrcBlend o DestBlend con SRC1 en el nombre)<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | AlphaToCoverageEnable debe ser **FALSE.**<br/> Los cuatro primeros BlendEnables deben tener el mismo valor.<br/> No se admite D3D11 \_ BLEND \_ SRC \_ ALPHASAT.<br/> No se admite la combinación de colores de origen dual (cualquier SrcBlend o DestBlend con SRC1 en el nombre)<br/>                                                                                |
| NIVEL DE CARACTERÍSTICA D3D \_ \_ \_ 10 \_ 0 | Agrega alfa a cobertura                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device::CreateBlendState1



| Nivel de característica              | Diferencias de comportamiento                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1  | No compatible<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | No compatible<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | No compatible<br/>                                                                                                                                                                                                                                                                                                                                       |
| NIVEL DE CARACTERÍSTICA D3D \_ \_ \_ 10 \_ 0 | El miembro *OutputMergerLogicOp* se ha agregado a [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options)para determinar la compatibilidad con las operaciones lógicas (operaciones lógicas bit a bit entre la salida del sombreador de píxeles y el contenido del destino de representación, consulte [**D3D11 \_ RENDER TARGET BLEND \_ \_ \_ DESC1).**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1) |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device::CreateBuffer




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Los búferes no pueden tener vistas de destino de representación.<br /> Los búferes deben tener exactamente una de D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br /> Solo permite búferes de índice con DXGI_FORMAT_R16_UINT formato. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Los búferes no pueden tener vistas de destino de representación.<br /> Los búferes deben tener exactamente una de D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER o D3D11_BIND_CONSTANT_BUFFER.<br /> Permite búferes de índice con DXGI_FORMAT_R16_UINT y DXGI_FORMAT_R32_UINT formatos como D3D_FEATURE_LEVEL_10_0 y superiores. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device::CreateCounter




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device::CreateDepthStencilView




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No admite galería de símbolos de dos lados.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device::CreateDomainShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*. ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device::CreateGeometryShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device::CreateGeometryShaderWithStreamOutput




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device::CreateHullShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device::CreateInputLayout



| Nivel de característica             | Diferencias de comportamiento                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | No admite D3D11 \_ INPUT \_ PER INSTANCE \_ \_ DATA                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | No admite D3D11 \_ INPUT \_ PER INSTANCE \_ \_ DATA                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | El flujo de vértice cero debe tener D3D11 INPUT PER VERTEX DATA, si alguna secuencia tiene DATOS DE ENTRADA POR VÉRTICE de \_ \_ \_ \_ D3D11 \_ \_ \_ \_ |



 

Consulte el gráfico de compatibilidad de formato por [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) para obtener más información sobre los formatos que se pueden usar para los datos de vértices en cada nivel de característica.

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device::CreatePixelShader



| Nivel de característica             | Diferencias de comportamiento                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Debe usar ps \_ 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Debe usar ps \_ 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Debe usar ps \_ 4 \_ 0 \_ level \_ 9 \_ 3 o ps \_ 4 \_ 0 \_ level \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device::CreatePredicate




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatequery"></a>ID3D11Device::CreateQuery



| Nivel de característica             | Diferencias de comportamiento                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Se admiten consultas de eventos. Las consultas de marca de tiempo son opcionales: llame [**a CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad.               |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Se admiten consultas de eventos y oclusión. Las consultas de marca de tiempo son opcionales: llame [**a CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad. |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Se admiten consultas de eventos y oclusión. Las consultas de marca de tiempo son opcionales: llame [**a CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar la compatibilidad. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device::CreateRasterizerState




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | DepthClipEnable debe ser <strong>TRUE.</strong> DepthBiasClamp debe establecerse en 0.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device::CreateRenderTargetView




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo se pueden admitir vistas de destino de representación de objetos Texture2D.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device::CreateSamplerState




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite el filtro de comparación.<br /> El color del borde debe estar dentro de [0,1]<br /> El LOD mínimo no puede ser fraccionrio<br /> El LOD máximo debe ser FLT_MAX<br /> La anisotropía máxima es 2.<br /> D3D11_TEXTURE_ADDRESS_MIRRORONCE no se admite.<br /> | 
| D3D_FEATURE_LEVEL_9_2 |  No se admite el filtro de comparación.<br /> El color del borde debe estar dentro de [0,1]<br /> El LOD mínimo no puede ser fraccionrio<br /> El LOD máximo debe ser FLT_MAX<br /> La anisotropía máxima es 16.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device::CreateShaderResourceView



| Nivel de característica             | MostDetailedMip más MipLevels debe incluir el LOD más bajo (subrecurso más pequeño). | La vista debe incluir todos los elementos de la matriz de recursos |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Sí                                                                          | sí                                           |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Sí                                                                          | Sí                                           |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Sí                                                                          | Sí                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device::CreateTexture1D




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device::CreateTexture2D

Los recursos de Texture2D tienen límites en su ancho y alto que difieren entre los [niveles de características.](overviews-direct3d-11-devices-downlevel-intro.md) En los niveles de características 9 3, se garantiza el mínimo mínimo de \_ lo siguiente y las implementaciones individuales pueden superar los requisitos.



| Nivel de característica             | Si MipCount > 1, las dimensiones deben ser una potencia integral de dos | Dimensión de textura mínima admitida | Las dimensiones de texturas de cubo deben ser la potencia de dos | Si se establece \_ MISC TEXTURECUBE, ArraySize es: | Si MISC \_ TEXTURECUBE no está establecido, ArraySize es . |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Sí                                                          | 2048                                | Sí                                           | 6                                              | 1                                                  |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Sí                                                          | 2048                                | Sí                                           | 6                                              | 1                                                  |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Sí                                                          | 4096                                | Sí                                           | 6                                              | 1                                                  |



 

En la tabla anterior, el nombre completo de **MISC \_ TEXTURECUBE** es [**D3D11 \_ RESOURCE \_ MISC \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Lo siguiente se aplica a los 9 niveles \_ \* [de características:](overviews-direct3d-11-devices-downlevel-intro.md)

-   Al usar D3D11 \_ USAGE \_ DEFAULT o D3D11 \_ USAGE \_ IMMUTABLE, BindFlags no puede ser cero.
-   Al usar D3D11 \_ BIND \_ DEPTH \_ STENCIL, MipLevels debe ser 1.
-   Al usar D3D11 \_ BIND \_ SHADER \_ RESOURCE, SampleDesc.Count debe ser 1.
-   Cuando se usa D3D11 \_ BIND \_ PRESENT, el recurso no puede tener D3D11 \_ BIND SHADER \_ \_ RESOURCE.
-   Cuando se usa D3D10 DDI RESOURCE MISC SHARED, format no puede ser \_ \_ \_ \_ DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM ni DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device::CreateTexture3D



| Nivel de característica             | Dimensión máxima (cualquier eje) | Las dimensiones deben ser una potencia de dos |
|---------------------------|------------------------------|---------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | 256                          | Sí                             |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | 512                          | Sí                             |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | 512                          | Sí                             |



 

Si el recurso es D3D11 \_ USAGE \_ DEFAULT o D3D11 \_ USAGE \_ IMMUTABLE, BindFlags no puede ser cero.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device::CreateUnorderedAccessView




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device::CreateVertexShader



| Nivel de característica             | Diferencias de comportamiento                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Debe usar frente \_ a 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Debe usar frente \_ a 4 \_ 0 \_ nivel \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Debe usar vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 3 o vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device::OpenSharedResource




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a> con el valor <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> y la D3D11_FEATURE_DATA_FORMAT_SUPPORT2 <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>estructura</strong></a> para determinar si se puede compartir un formato. Si se puede compartir el formato, <strong>CheckFeatureSupport</strong> devuelve <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> marca.<br /><blockquote>[!Note]<br />[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) y <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> nunca se pueden compartir cuando se usa el nivel de característica 9, incluso si el dispositivo indica compatibilidad opcional con características <strong>para D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. Al intentar crear recursos compartidos <strong></strong> con formatos DXGI DXGI_FORMAT_R8G8B8A8_UNORM y <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> siempre se producirá un error a menos que el nivel de característica sea 10_0 o superior.</blockquote><br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

