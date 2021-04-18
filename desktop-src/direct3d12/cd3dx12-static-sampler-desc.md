---
title: CD3DX12_STATIC_SAMPLER_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una \_ estructura de descripción de muestra estática de D3D12 \_ \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Estructura de CD3DX12_STATIC_SAMPLER_DESC
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
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717595"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>CD3DX12 \_ \_ estructura de DESC de muestra estática \_

Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ Descripción de muestra estática de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

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

**Descripción de la \_ muestra estática CD3DX12 \_ \_ ()**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una descripción de la \_ muestra estática CD3DX12 \_ \_ .

</dd> <dt>

**CD3DX12 explícito de la \_ muestra estática de la \_ \_ Descripción (const D3D12 \_ &de \_ muestra estática \_ )**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de \_ muestra estática CD3DX12 \_ , inicializada con el contenido de otra estructura D3D12 de la [**\_ muestra estática de la \_ \_ muestra**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

</dd> <dt>

**CD3DX12 \_ static \_ Sampler \_ DESC (uint shaderRegister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ anisotrópico, D3D12 \_ Texture \_ Address \_ mode addressU = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap, D3D12 \_ Texture \_ Address \_ mode addressV = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap D3D12 \_ \_ \_ modo de dirección de textura addressW = D3D12 \_ \_ \_ de modo \_ de dirección de textura Wrap, Float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ FUNC comparisonFunc = D3D12 \_ Comparison la \_ \_ función de comparación menos \_ igual, D3D12 el \_ \_ color del borde estático \_ BorderColor = D3D12 el \_ \_ color del borde estático de la \_ \_ \_ visibilidad del sombreador minLOD = \_ \_ \_ \_ maxLOD \_ Visibility del sombreador \_ \_ All, uint D3D12 = 0)**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de \_ la muestra estática CD3DX12 \_ , inicializando los siguientes parámetros:

UINT shaderRegister

rechace [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotrópico

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace FLOAT mipLODBias = 0

rechace UINT maxAnisotropy = 16

rechace [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = función de comparación de D3D12 \_ \_ \_ menos \_ igual

rechace [**D3D12 \_ \_ \_ Color de borde estático**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ D3D12 \_ borde \_ estático \_ color \_ blanco opaco

rechace FLOAT minLOD = 0. f

rechace FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

rechace [**D3D12 \_ \_Visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 visibilidad del \_ sombreador \_ \_

rechace UINT registerSpace = 0

</dd> <dt>

**Static inline init (D3D12 \_ static \_ sample \_ DESC &SamplerDesc, uint shaderRegister, D3D12 Filter \_ Filter = D3D12 \_ Filter \_ anisotrópico, D3D12 \_ Texture \_ Address \_ mode addressU = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap, D3D12 \_ Texture \_ Address \_ mode addressV = D3D12 \_ Texture Address Mode \_ \_ \_ Wrap D3D12 \_ \_ \_ modo de dirección de textura addressW = D3D12 \_ \_ \_ \_ de modo de dirección de textura Wrap, Float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ FUNC comparisonFunc = D3D12 \_ Comparison la \_ \_ función de comparación menos \_ igual, D3D12 el \_ \_ \_ color del borde estático BorderColor = D3D12 el \_ \_ \_ color del borde estático de la \_ \_ visibilidad del \_ sombreador minLOD = \_ \_ \_ maxLOD Visibility del \_ sombreador \_ \_ All, uint D3D12 = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_ \_ Descripción de muestra estática**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc

UINT shaderRegister

rechace [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotrópico

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace FLOAT mipLODBias = 0

rechace UINT maxAnisotropy = 16

rechace [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = función de comparación de D3D12 \_ \_ \_ menos \_ igual

rechace [**D3D12 \_ \_ \_ Color de borde estático**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ D3D12 \_ borde \_ estático \_ color \_ blanco opaco

rechace FLOAT minLOD = 0. f

rechace FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

rechace [**D3D12 \_ \_Visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 visibilidad del \_ sombreador \_ \_

rechace UINT registerSpace = 0

</dd> <dt>

**Init en línea (UINT shaderRegister, filtro de filtro de D3D12 \_ = D3D12 \_ filtro \_ anisotrópico, D3D12 \_ modo de dirección de textura \_ \_ addressU = D3D12 \_ ajuste del \_ \_ modo de dirección de textura \_ , D3D12 \_ modo de dirección de textura \_ \_ addressV = D3D12 \_ ajuste del \_ \_ modo de dirección de textura \_ , D3D12 \_ \_ \_ modo de dirección de textura addressW = D3D12 \_ \_ \_ \_ de modo de dirección de textura Wrap, Float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ COMparison \_ FUNC comparisonFunc = D3D12 \_ Comparison la \_ \_ función de comparación menos \_ igual, D3D12 el \_ \_ \_ color del borde estático BorderColor = D3D12 el \_ \_ \_ color del borde estático de la \_ \_ \_ visibilidad del sombreador minLOD = \_ \_ \_ maxLOD Visibility del \_ sombreador \_ \_ All, uint D3D12 = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

rechace [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotrópico

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_

rechace FLOAT mipLODBias = 0

rechace UINT maxAnisotropy = 16

rechace [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = función de comparación de D3D12 \_ \_ \_ menos \_ igual

rechace [**D3D12 \_ \_ \_ Color de borde estático**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ D3D12 \_ borde \_ estático \_ color \_ blanco opaco

rechace FLOAT minLOD = 0. f

rechace FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

rechace [**D3D12 \_ \_Visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 visibilidad del \_ sombreador \_ \_

rechace UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Descripción de \_ muestra \_ estática de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





