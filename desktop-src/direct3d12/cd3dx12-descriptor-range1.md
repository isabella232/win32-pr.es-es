---
title: CD3DX12_DESCRIPTOR_RANGE1 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ RANGE1 del DESCRIPTOR \_ D3D12.
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 estructura
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160450"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>Estructura CD3DX12 \_ DESCRIPTOR \_ RANGE1

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ \_ RANGE1 del DESCRIPTOR D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DESCRIPTOR RANGE1 de CD3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ DESCRIPTOR \_ RANGE1(const D3D12 \_ DESCRIPTOR \_ RANGE1 &o)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RANGE1 de CD3DX12, inicializado con el contenido de otra estructura \_ \_ [**\_ \_ RANGE1 del DESCRIPTOR D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE1(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS flags = D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAG \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RANGE1 de CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

NumDescriptors de UINT

Base de UINTShaderRegister

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE \_ RANGO DE DESCRIPTOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = D3D12 DESCRIPTOR RANGE FLAG \_ \_ \_ \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**init inline(D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR RANGE \_ \_ FLAGS flags = D3D12 \_ DESCRIPTOR RANGE FLAG \_ \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

NumDescriptors de UINT

Base de UINTShaderRegister

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE \_ RANGO DE DESCRIPTOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = D3D12 DESCRIPTOR RANGE FLAG \_ \_ \_ \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE1 &range, D3D12 \_ DESCRIPTOR RANGE TYPE \_ \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12 \_ DESCRIPTOR RANGE \_ \_ FLAGS flags = D3D12 \_ DESCRIPTOR RANGE FLAG \_ \_ \_ NONE, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Intervalo \_ de &DESCRIPTOR RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

NumDescriptors de UINT

Base de UINTShaderRegister

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE \_ RANGO DE DESCRIPTOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = D3D12 DESCRIPTOR RANGE FLAG \_ \_ \_ \_ NONE

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





