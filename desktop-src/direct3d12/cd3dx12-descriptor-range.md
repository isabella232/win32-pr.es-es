---
title: CD3DX12_DESCRIPTOR_RANGE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de intervalo de descriptores de D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Estructura de CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b511af1766daaefa7f92d33b71841b3a69c99927
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649382"
---
# <a name="cd3dx12_descriptor_range-structure"></a>CD3DX12 \_ estructura de intervalo de descriptores \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ intervalo de descriptores de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Intervalo del descriptor de CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ intervalo de descriptor D3DX12 \_ .

</dd> <dt>

**intervalo de \_ descriptor de CD3DX12 explícito \_ (const D3D12 \_ \_ Range &o)**
</dt> <dd>

Crea una nueva instancia de un \_ intervalo de descriptor de D3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ intervalo de descriptores de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

</dd> <dt>

**Intervalo de descriptor de CD3DX12 (tipo de intervalo de descriptores \_ \_ D3D12 \_ \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor \_ desplazamiento de intervalo \_ \_ append)**
</dt> <dd>

Crea una nueva instancia de un \_ intervalo de descriptor de D3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_

</dd> <dt>

**Init en línea ( \_ tipo de intervalo de descriptor D3D12 \_ \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor de desplazamiento de intervalo de descriptor \_ \_ \_ )**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_

</dd> <dt>

**Init en línea estático ( \_ intervalo de descriptor \_ de D3D12 &intervalo, \_ tipo de intervalo de descriptor D3D12 \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ descriptor \_ desplazamiento de intervalo \_ \_ anexar)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Rango \_ de DEscriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &intervalo

[**D3D12 \_ \_ \_ Tipo de intervalo de descriptor**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ de \_ desplazamiento de intervalo de descriptor \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Intervalo de descriptor de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





