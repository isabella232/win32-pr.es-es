---
title: CD3DX12_ROOT_PARAMETER estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de parámetros raíz D3D12 \_ .
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Estructura de CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717598"
---
# <a name="cd3dx12_root_parameter-structure"></a>\_Estructura del \_ parámetro raíz CD3DX12

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ parámetros raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Parámetro raíz CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ parámetro raíz CD3DX12 \_ .

</dd> <dt>

**\_parámetro raíz CD3DX12 explícito \_ ( \_ parámetro raíz const D3D12 \_ &o)**
</dt> <dd>

Crea una nueva instancia de un \_ parámetro raíz CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ parámetros raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

</dd> <dt>

**Static inline InitAsDescriptorTable ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ intervalo de descriptor \_ \* pDescriptorRanges, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT numDescriptorRanges

[**D3D12 \_ \_Rango de DEscriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsConstants ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT num32BitValues

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsConstantBufferView ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsShaderResourceView ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsUnorderedAccessView ( \_ parámetro raíz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ visibilidad del sombreador \_ \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_Parámetro raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ intervalo de descriptor \_ \* pDescriptorRanges, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

[**D3D12 \_ \_Rango de DEscriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 visibilidad de \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT num32BitValues

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad \_ del sombreador)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad \_ del sombreador)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ visibilidad de \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad \_ del sombreador)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

rechace UINT registerSpace = 0

rechace [**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Parámetro raíz \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





