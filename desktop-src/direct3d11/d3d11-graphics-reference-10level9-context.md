---
title: Métodos 10Level9 ID3D11DeviceContext
description: En esta sección se enumeran las diferencias entre cada nivel de característica 10Level9 y el nivel de característica D3D FEATURE LEVEL 11 0 y superior para los \_ \_ \_ \_ métodos ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e268f45465139e49afe0f81a64eeeb93939734e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361288"
---
# <a name="10level9-id3d11devicecontext-methods"></a>Métodos 10Level9 ID3D11DeviceContext

En esta sección se enumeran las diferencias entre cada nivel de característica 10Level9 y el nivel de característica D3D FEATURE LEVEL 11 0 y superior para los \_ \_ \_ \_ [**métodos ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

-   [ID3D11DeviceContext::CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [ID3D11DeviceContext::CopyResource](#id3d11devicecontextcopyresource)
-   [ID3D11DeviceContext::CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [ID3D11DeviceContext::ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [ID3D11DeviceContext::CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [ID3D11DeviceContext::CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [ID3D11DeviceContext::CSSetShader](#id3d11devicecontextcssetshader)
-   [ID3D11DeviceContext::CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [ID3D11DeviceContext::CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [ID3D11DeviceContext::D ispatch](#id3d11devicecontextdispatch)
-   [ID3D11DeviceContext::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::D raw](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::D rawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::D rawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::D rawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [ID3D11DeviceContext::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::D rawInstanced](#id3d11devicecontextdrawinstanced)
-   [ID3D11DeviceContext::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [ID3D11DeviceContext::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [ID3D11DeviceContext::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [ID3D11DeviceContext::D SSetShader](#id3d11devicecontextdssetshader)
-   [ID3D11DeviceContext::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [ID3D11DeviceContext::GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [ID3D11DeviceContext::GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [ID3D11DeviceContext::GSSetShader](#id3d11devicecontextgssetshader)
-   [ID3D11DeviceContext::GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [ID3D11DeviceContext::HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [ID3D11DeviceContext::HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [ID3D11DeviceContext::HSSetShader](#id3d11devicecontexthssetshader)
-   [ID3D11DeviceContext::HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext::IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [ID3D11DeviceContext::OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [ID3D11DeviceContext::OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [ID3D11DeviceContext::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [ID3D11DeviceContext::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [ID3D11DeviceContext::P SSetShader](#id3d11devicecontextpssetshader)
-   [ID3D11DeviceContext::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [ID3D11DeviceContext::RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [ID3D11DeviceContext::RSSetViewports](#id3d11devicecontextrssetviewports)
-   [ID3D11DeviceContext::SetPredication](#id3d11devicecontextsetpredication)
-   [ID3D11DeviceContext::SOSetTargets](#id3d11devicecontextsosettargets)
-   [ID3D11DeviceContext::VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [ID3D11DeviceContext::VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [ID3D11DeviceContext::VSSetShader](#id3d11devicecontextvssetshader)
-   [ID3D11DeviceContext::VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Temas relacionados](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>ID3D11DeviceContext::CopySubresourceRegion




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Solo se pueden copiar Texture2D y los búferes en la memoria accesible para GPU.<br /> Texture3D no se puede copiar de la memoria accesible desde GPU a la memoria accesible desde la CPU.<br /> Los recursos que solo tienen D3D10_BIND_SHADER_RESOURCE no se pueden copiar de la memoria accesible desde GPU a la memoria accesible desde la CPU.<br /> No se pueden copiar texturas de volumen mipmapped. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext::CopyResource




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Solo se pueden copiar Texture2D y los búferes en la memoria accesible para GPU.<br /> Texture3D no se puede copiar de la memoria accesible desde GPU a la memoria accesible desde la CPU.<br /> Los recursos que solo tienen D3D10_BIND_SHADER_RESOURCE no se pueden copiar de la memoria accesible desde GPU a la memoria accesible desde la CPU.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext::CopyStructureCount




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext::ClearUnorderedAccessViewFloat




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext::ClearUnorderedAccessViewUint




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext::ClearRenderTargetView




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo se borrará el primer segmento de matriz. Las aplicaciones deben crear una vista de destino de representación para cada segmento de cara o matriz y, a continuación, borrar cada vista individualmente.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext::CSSetConstantBuffers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext::CSSetSamplers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext::CSSetShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext::CSSetShaderResources




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext::CSSetUnorderedAccessViews




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext::D ispatch




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext::D ispatchIndirect




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::D raw



| Nivel de característica             | Diferencias de comportamiento                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | El número de primitivas no puede superar 65535.<br/> Las texturas no se pueden repetir en una primitiva más de 128 veces.<br/>    |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Es posible que el número de primitivas no supere 1048575.<br/> Las texturas no se pueden repetir en una primitiva más de 2048 veces.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Es posible que el número de primitivas no supere 1048575.<br/> Las texturas no se pueden repetir en una primitiva más de 8192 veces.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::D rawAuto




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::D rawIndexed



| Nivel de característica             | Diferencias de comportamiento                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | El número de primitivas no puede superar 65535.<br/> Las texturas no se pueden repetir en una primitiva más de 128 veces.<br/> Los valores de índice no pueden superar 65534.<br/> No se admiten listas de puntos indizados.<br/>      |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Es posible que el número de primitivas no supere 1048575.<br/> Las texturas no se pueden repetir en una primitiva más de 2048 veces.<br/> Los valores de índice no pueden superar 1048575.<br/> No se admiten listas de puntos indizados.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Es posible que el número de primitivas no supere 1048575.<br/> Las texturas no se pueden repetir en una primitiva más de 8192 veces.<br/> Los valores de índice no pueden superar 1048575.<br/> No se admiten listas de puntos indizados.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::D rawIndexedInstanced




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Es posible que el número de primitivas no supere 1048575.<br /> Las texturas no se pueden repetir en una primitiva más de 8192 veces.<br /> Los valores de índice no pueden superar 1048575.<br /><blockquote>[!Note]<br />Al llamar al método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> con un sombreador de vértices que está enlazado a la canalización y que no importa ningún dato por instancia, es posible que algún hardware gráfico de Direct3D 9 no dibuje nada. En concreto, si el sombreador de vértices no usa ningún dato por instancia, llamar a <strong>DrawIndexedInstanced</strong> con 1 instancia no equivale a llamar <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>a Draw</strong></a>.</blockquote><br /> | 




 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext::D rawIndexedInstancedIndirect




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::D rawInstanced




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext::D rawInstancedIndirect




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext::D SSetConstantBuffers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext::D SSetSamplers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext::D SSetShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext::D SSetShaderResources




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext::GSSetConstantBuffers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext::GSSetSamplers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext::GSSetShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext::GSSetShaderResources




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext::HSSetConstantBuffers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext::HSSetSamplers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext::HSSetShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext::HSSetShaderResources




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | El formato puede ser diferente del especificado en la creación del búfer, pero se incurrirá en una traducción costosa.<br /> Solo permite búferes de índice con DXGI_FORMAT_R16_UINT formato. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  El formato puede ser diferente del especificado en la creación del búfer, pero se incurrirá en una traducción costosa.<br /> Permite búferes de índice con los DXGI_FORMAT_R16_UINT y DXGI_FORMAT_R32_UINT formatos como D3D_FEATURE_LEVEL_10_0 y superiores. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Las topologías primitivas con adyacencia no se admiten${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext::OMSetBlendState




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | SampleMask no puede ser cero${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext::OMSetRenderTargets




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo se admite un destino de representación${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Solo se admiten cuatro destinos de representación y todos los recursos enlazados deben tener la misma profundidad de bits. | 




 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext::P SSetConstantBuffers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vea el nivel de característica 10.0, pero el número total de constantes usadas por el sombreador no puede superar los 32${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext::P SSetSamplers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se pueden enlazar más de 16 muestreadores${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext::P SSetShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo ps_4_0_level_9_1${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Solo ps_4_0_level_9_3 o ps_4_0_level_9_1 | 




 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext::P SSetShaderResources




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No más de 8 recursos de sombreador enlazados simultáneamente${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext::RSSetScissorRects




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo está disponible el rect zeroth- desenlazamiento${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext::RSSetViewports




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo la ventanilla de cero está disponible${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

Aunque especifique valores float para los miembros de la estructura [**\_ VIEWPORT D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) para la matriz *pViewports* en una llamada a [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para los niveles de característica [9](overviews-direct3d-11-devices-downlevel-intro.md) \_ x, **RSSetViewports** usa DWORD internamente. Debido a este comportamiento, cuando se usa una esquina superior izquierda negativa para la ventanilla, se produce un error en la llamada a **RSSetViewports** para los niveles de característica 9 \_ x. Este error se produce porque **RSSetViewports** para 9 x convierte los valores de punto flotante en enteros sin signo sin validación, lo que produce un desbordamiento \_ de enteros.

La llamada a [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) para los niveles de características [10](overviews-direct3d-11-devices-downlevel-intro.md) x y 11 x funciona como se espera incluso cuando se usa una esquina superior izquierda negativa para la \_ \_ ventanilla.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext::SetPredication




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext::SOSetTargets




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext::VSSetConstantBuffers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vea el nivel de característica 10.0, pero el número total de constantes usadas por el sombreador no puede superar los 255${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext::VSSetSamplers




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext::VSSetShader




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo vs_4_0_level_9_1${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Solo vs_4_0_level_9_3 o vs_4_0_level_9_1 | 




 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext::VSSetShaderResources




| Nivel de característica | Diferencias de comportamiento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | No se admite en ningún nivel de característica 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





