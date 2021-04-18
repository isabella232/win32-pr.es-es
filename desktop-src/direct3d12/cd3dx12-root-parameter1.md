---
title: CD3DX12_ROOT_PARAMETER1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura PARÁMETRO1 raíz D3D12.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Estructura de CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718488"
---
# <a name="cd3dx12_root_parameter1-structure"></a>CD3DX12 \_ raíz \_ parámetro1

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ parámetro1 raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ raíz \_ parámetro1 ()**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una \_ raíz CD3DX12 \_ parámetro1.

</dd> <dt>

**raíz CD3DX12 \_ explícita \_ parámetro1 (const D3D12 \_ raíz \_ parámetro1 &o)**
</dt> <dd>

Crea una nueva instancia de la raíz de CD3DX12 \_ \_ parámetro1, inicializada con el contenido de otra estructura [**\_ \_ parámetro1 raíz de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

</dd> <dt>

**Static inline InitAsDescriptorTable (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ descriptor \_ RANGE1 \* pDescriptorRanges, D3D12 visibilidad \_ del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ All)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT numDescriptorRanges

const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsConstants (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsConstantBufferView (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ )**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsShaderResourceView (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ )**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Static inline InitAsUnorderedAccessView (D3D12 \_ raíz \_ Parámetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ )**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ RAÍZ \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ descriptor \_ RANGE1 \* pDescriptorRanges, D3D12 \_ visibilidad del sombreador Visibility \_ = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 visibilidad de \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> <dt>

**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None, D3D12 \_ \_ visibilidad del sombreador = D3D12 \_ \_ visibilidad del sombreador \_ todos)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

[**D3D12 \_ Visibilidad de \_ visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = D3D12 \_ visibilidad del sombreador \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ raíz \_ parámetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





