---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura TABLE1 del descriptor raíz D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR_TABLE1
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718494"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>CD3DX12 \_ \_ estructura TABLE1 del descriptor raíz \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ \_ TABLE1 del descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ root \_ descriptor \_ TABLE1 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ \_ descriptor de raíz CD3DX12 \_ TABLE1.

</dd> <dt>

**descriptor de raíz CD3DX12 explícito \_ \_ \_ TABLE1 (const D3D12 \_ raíz \_ \_ Table1 &o)**
</dt> <dd>

Crea una nueva instancia de un \_ \_ descriptor de raíz CD3DX12 \_ Table1, inicializada con el contenido de otra estructura [**\_ \_ \_ TABLE1 del descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

</dd> <dt>

**CD3DX12 \_ root \_ descriptor \_ TABLE1 (uint NUMDESCRIPTORRANGES, const D3D12 \_ descriptor \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Crea una nueva instancia de un \_ \_ descriptor raíz CD3DX12 \_ TABLE1, inicializando los siguientes parámetros:

UINT numDescriptorRanges

const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**Init en línea (UINT numDescriptorRanges, const D3D12 \_ descriptor \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**Inicial inline init (D3D12 \_ root \_ descriptor \_ TABLE1 &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 \_ descriptor \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Descriptor de raíz \_ \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable

UINT numDescriptorRanges

const [**D3D12 \_ descriptor \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ el \_ descriptor raíz \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





