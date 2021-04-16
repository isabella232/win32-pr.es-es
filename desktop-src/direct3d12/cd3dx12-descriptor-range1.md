---
title: CD3DX12_DESCRIPTOR_RANGE1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura RANGE1 del descriptor de D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Estructura de CD3DX12_DESCRIPTOR_RANGE1
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649381"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>CD3DX12 \_ descriptor \_ RANGE1 (estructura)

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ RANGE1 del descriptor de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**\_Descriptor CD3DX12 \_ RANGE1 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ descriptor CD3DX12 \_ RANGE1.

</dd> <dt>

**descriptor de CD3DX12 explícito \_ \_ range1 (const D3D12 \_ descriptor \_ range1 &o)**
</dt> <dd>

Crea una nueva instancia de un \_ descriptor de CD3DX12 \_ range1, inicializada con el contenido de otra estructura del [**\_ descriptor de D3D12 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

</dd> <dt>

**Descriptor de CD3DX12 \_ \_ RANGE1 ( \_ tipo de intervalo de descriptores D3D12 \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ descriptores de intervalo Flags \_ \_ = D3D12 \_ marcador de intervalo de descriptor \_ \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor de \_ desplazamiento de intervalo \_ \_ append)**
</dt> <dd>

Crea una nueva instancia de un \_ descriptor de CD3DX12 \_ RANGE1, inicializando los siguientes parámetros:

[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ rango de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) marcas = marca de intervalo de descriptor de D3D12 \_ \_ \_ \_ ninguno

UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_

</dd> <dt>

**Init en línea ( \_ tipo de intervalo de descriptores \_ de D3D12 \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ descriptores de intervalo Flags \_ \_ = D3D12 \_ \_ marcador de intervalo de DEscriptor \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor de \_ desplazamiento de intervalo \_ \_ append)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ rango de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) marcas = marca de intervalo de descriptor de D3D12 \_ \_ \_ \_ ninguno

UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_

</dd> <dt>

**Inicialización en línea estática ( \_ descriptor \_ de D3D12 RANGE1 &intervalo, \_ tipo de intervalo de descriptor de D3D12 de \_ \_ texto RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 descriptores de intervalo de descriptores \_ \_ \_ = D3D12 \_ marcador de intervalo de descriptor \_ \_ \_ ninguno, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor \_ \_ desplazamiento \_ anexar)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &intervalo

[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ rango de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) marcas = marca de intervalo de descriptor de D3D12 \_ \_ \_ \_ ninguno

UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Descriptor D3D12 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





