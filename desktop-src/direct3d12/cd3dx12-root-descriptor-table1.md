---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE1 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura TABLE1 del DESCRIPTOR RAÍZ de D3D12. \_ \_ \_
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1 estructura
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566185"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>Estructura TABLE1 del \_ \_ DESCRIPTOR RAÍZ \_ DE CD3DX12

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ \_ \_ TABLE1 del DESCRIPTOR RAÍZ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DESCRIPTOR RAÍZ DE CD3DX12 \_ \_ \_ TABLE1.

</dd> <dt>

**EXPLICIT CD3DX12 \_ ROOT \_ DESCRIPTOR \_ TABLE1(const D3D12 \_ ROOT DESCRIPTOR \_ \_ TABLE1 &o)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RAÍZ TABLE1 de CD3DX12, inicializado con el contenido de otra estructura TABLE1 del \_ \_ DESCRIPTOR RAÍZ \_ [**\_ \_ \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)

</dd> <dt>

**CD3DX12 \_ \_ ROOT DESCRIPTOR \_ TABLE1(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Crea una nueva instancia de UN DESCRIPTOR RAÍZ DE CD3DX12 \_ \_ \_ TABLE1, inicializando los parámetros siguientes:

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**inline Init(UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**static inline Init(D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable

UINT numDescriptorRanges

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





