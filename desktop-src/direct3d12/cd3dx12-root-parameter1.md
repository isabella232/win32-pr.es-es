---
title: CD3DX12_ROOT_PARAMETER1 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura ROOT PARAMETER1 de D3D12. \_ \_
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- CD3DX12_ROOT_PARAMETER1 estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566181"
---
# <a name="cd3dx12_root_parameter1-structure"></a>Estructura CD3DX12 \_ ROOT \_ PARAMETER1

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ ROOT \_ PARAMETER1 de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

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



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ ROOT \_ PARAMETER1()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un PARÁMETRO RAÍZ CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ ROOT \_ PARAMETER1(const D3D12 \_ ROOT \_ PARAMETER1 &o)**
</dt> <dd>

Crea una nueva instancia de UN PARÁMETRO RAÍZ CD3DX12, inicializado con el contenido de otra estructura \_ ROOT \_ [**\_ \_ PARAMETER1 de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

</dd> <dt>

**static inline InitAsDescriptorTable(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**static inline InitAsConstants(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

UINT num32BitValues

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**static inline InitAsConstantBufferView(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT DESCRIPTOR \_ \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**static inline InitAsShaderResourceView(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT DESCRIPTOR \_ \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**static inline InitAsUnorderedAccessView(D3D12 \_ ROOT \_ PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT DESCRIPTOR \_ \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE, D3D12 \_ SHADER VISIBILITY VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT num32BitValues

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE, D3D12 \_ SHADER VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE, D3D12 \_ SHADER VISIBILITY visibility = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> <dt>

**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE, D3D12 \_ SHADER VISIBILITY = \_ D3D12 \_ SHADER VISIBILITY \_ \_ ALL)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

[**D3D12 \_ Visibilidad \_ DEL SOMBREADOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = VISIBILIDAD DEL SOMBREADOR D3D12 \_ \_ \_ TODO

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





