---
title: CD3DX12_ROOT_PARAMETER estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura ROOT PARAMETER de D3D12. \_ \_
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- CD3DX12_ROOT_PARAMETER estructura
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
ms.openlocfilehash: 56d1acb150b4af3f096b8ebf8c5a91caef831ebc03f84df10440b95110bc018e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953165"
---
# <a name="cd3dx12_root_parameter-structure"></a>Estructura DE PARÁMETROS RAÍZ DE CD3DX12 \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ ROOT \_ PARAMETER de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)

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

**CD3DX12 \_ ROOT \_ PARAMETER()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un PARÁMETRO RAÍZ CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ ROOT \_ PARAMETER(const D3D12 \_ ROOT PARAMETER &\_ o)**
</dt> <dd>

Crea una nueva instancia de UN PARÁMETRO RAÍZ CD3DX12, inicializado con el contenido de otra estructura \_ \_ ROOT [**\_ \_ PARAMETER de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)

</dd> <dt>

**static inline InitAsDescriptorTable(D3D12 \_ ROOT \_ PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR RANGE \_ \* pDescriptorRanges, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT numDescriptorRanges

[**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**static inline InitAsConstants(D3D12 \_ ROOT \_ PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT num32BitValues

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**static inline InitAsConstantBufferView(D3D12 \_ ROOT \_ PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**static inline InitAsShaderResourceView(D3D12 \_ ROOT \_ PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**static inline InitAsUnorderedAccessView(D3D12 \_ ROOT \_ PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE \* pDescriptorRanges, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

[**D3D12 \_ DESCRIPTOR \_ RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT num32BitValues

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> <dt>

**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

(opt) [**D3D12 \_ Visibilidad \_ del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ ALL

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PARÁMETRO RAÍZ D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





