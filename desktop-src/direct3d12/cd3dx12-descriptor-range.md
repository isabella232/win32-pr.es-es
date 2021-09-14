---
title: CD3DX12_DESCRIPTOR_RANGE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ RANGE de DESCRIPTOR D3D12. \_
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160452"
---
# <a name="cd3dx12_descriptor_range-structure"></a>Estructura CD3DX12 \_ DESCRIPTOR \_ RANGE

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura RANGE de DESCRIPTOR \_ D3D12. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)

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



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DESCRIPTOR RANGE de D3DX12. \_ \_

</dd> <dt>

**explicit CD3DX12 \_ DESCRIPTOR \_ RANGE(const D3D12 \_ DESCRIPTOR RANGE &\_ o)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RANGE de D3DX12, inicializado con el contenido de otra estructura DESCRIPTOR RANGE de \_ \_ [**D3D12. \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)

</dd> <dt>

**CD3DX12 \_ DESCRIPTOR \_ RANGE(D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND)**
</dt> <dd>

Crea una nueva instancia de D3DX12 \_ DESCRIPTOR \_ RANGE, inicializando los parámetros siguientes:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

NumDescriptors de UINT

Base de UINTShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**inline Init(D3D12 \_ DESCRIPTOR \_ RANGE TYPE \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

NumDescriptors de UINT

Base de UINTShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> <dt>

**static inline Init(D3D12 \_ DESCRIPTOR \_ RANGE &range, D3D12 \_ DESCRIPTOR RANGE TYPE \_ \_ rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR RANGE OFFSET \_ \_ \_ APPEND)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Intervalo \_ de &**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) DESCRIPTOR

[**D3D12 \_ DESCRIPTOR \_ RANGE \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

NumDescriptors de UINT

Base de UINTShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ DESCRIPTOR \_ RANGE \_ OFFSET \_ APPEND

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INTERVALO DEL DESCRIPTOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





