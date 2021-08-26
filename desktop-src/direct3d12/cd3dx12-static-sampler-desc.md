---
title: CD3DX12_STATIC_SAMPLER_DESC estructura (D3dx12.h)
description: Una estructura auxiliar para permitir la inicialización sencilla de una estructura \_ \_ DESC STATIC SAMPLER de D3D12. \_
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- CD3DX12_STATIC_SAMPLER_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd2e64a98a8dd11b62154bb3239934fd8da29eb6f8bf2919ef88452d280de6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069765"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>Estructura \_ \_ DESC DESC DE SAMPLER ESTÁTICA DE3DX12 \_

Una estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ \_ \_ DESC STATIC SAMPLER de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ STATIC \_ SAMPLER \_ DESC()**
</dt> <dd>

Crea una nueva instancia de UNSC STATIC SAMPLER CD3DX12 sin \_ \_ \_ inicializar.

</dd> <dt>

**EXPLICIT CD3DX12 \_ STATIC \_ SAMPLER \_ DESC(const D3D12 \_ STATIC \_ SAMPLER \_ DESC &o)**
</dt> <dd>

Crea una nueva instancia de un DESC DESC STATIC SAMPLER cd3DX12, inicializado con el contenido de otra estructura \_ \_ \_ [**\_ \_ \_ DESC de D3D12 STATIC SAMPLER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)

</dd> <dt>

**CD3DX12 \_ STATIC \_ SAMPLER \_ DESC(UINT shaderRegister, Filtro de filtro \_ D3D12 = D3D12 \_ FILTER \_ ANISOTROPIC, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressU = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressV = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressW = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, COMPARACIÓN de \_ D3D12 COMPARACIÓN \_ FUNC ComparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL, D3D12 \_ STATIC BORDER COLOR \_ \_ borderColor = D3D12 \_ STATIC BORDER COLOR OPAQUE \_ \_ \_ \_ WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX, D3D12 \_ SHADER VISIBILITY shader shader visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL, UINT registerSpace = 0)**
</dt> <dd>

Crea una nueva instancia de UN \_ \_ DESC DESC STATIC SAMPLER de CD3DX12, \_ inicializando los parámetros siguientes:

Sombreador UINTRegistrar

(opt) [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12 \_ FILTER \_ ANISOTROPIC

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) FLOAT mipLODBias = 0

(opt) UINT maxAnisotropy = 16

(opt) [**D3D12 \_ COMPARACIÓN \_ COMPARACIÓN FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL

(opt) [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12 \_ STATIC \_ BORDER \_ COLOR \_ OPAQUE \_ WHITE

(opt) FLOAT minLOD = 0.f

(opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

(opt) [**D3D12 \_ Sombreador \_ SHADER VISIBILITYVisibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

(opt) UINT registerSpace = 0

</dd> <dt>

**static inline Init(D3D12 \_ STATIC \_ SAMPLER \_ DESC &samplerDesc, Sombreador UINTRegistrar, filtro DE FILTRO \_ D3D12 = D3D12 \_ FILTER \_ ANISOTROPIC, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressU = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressV = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE address address \_ \_ wrap= D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12 \_ COMPARISON \_ FUNC comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL, D3D12 \_ STATIC BORDER COLOR \_ \_ borderColor = D3D12 \_ STATIC BORDER COLOR OPAQUE WHITE , FLOAT \_ \_ \_ \_ minLOD = 0.f, FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX, D3D12 \_ SHADER VISIBILITY \_ shaderVisibility = D3D12 \_ SHADER VISIBILITY \_ \_ ALL, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc

Sombreador UINTRegistrar

(opt) [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12 \_ FILTER \_ ANISOTROPIC

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) FLOAT mipLODBias = 0

(opt) UINT maxAnisotropy = 16

(opt) [**D3D12 \_ COMPARACIÓN \_ COMPARACIÓN FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL

(opt) [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12 \_ STATIC \_ BORDER \_ COLOR \_ OPAQUE \_ WHITE

(opt) FLOAT minLOD = 0.f

(opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

(opt) [**D3D12 \_ Sombreador \_ SHADER VISIBILITYVisibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

(opt) UINT registerSpace = 0

</dd> <dt>

**inline Init(UINT shaderRegister, Filtro de filtro \_ D3D12 = D3D12 \_ FILTER \_ ANISOTROPIC, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressU = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressV = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressW = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, COMPARACIÓN de \_ D3D12 COMPARACIÓN \_ FUNC ComparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL, D3D12 \_ STATIC BORDER COLOR \_ \_ borderColor = D3D12 \_ STATIC BORDER COLOR OPAQUE \_ \_ \_ \_ WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX, D3D12 \_ SHADER VISIBILITY shader shader visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

(opt) [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12 \_ FILTER \_ ANISOTROPIC

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) FLOAT mipLODBias = 0

(opt) UINT maxAnisotropy = 16

(opt) [**D3D12 \_ COMPARACIÓN \_ COMPARACIÓN FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL

(opt) [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12 \_ STATIC \_ BORDER \_ COLOR \_ OPAQUE \_ WHITE

(opt) FLOAT minLOD = 0.f

(opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

(opt) [**D3D12 \_ Sombreador \_ SHADER VISIBILITYVisibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ SHADER VISIBILITY \_ \_ ALL

(opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





