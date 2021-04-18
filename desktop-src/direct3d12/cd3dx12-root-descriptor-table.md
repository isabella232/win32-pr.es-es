---
title: CD3DX12_ROOT_DESCRIPTOR_TABLE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de tabla de descriptores raíz D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717599"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>CD3DX12 \_ \_ estructura de tabla del descriptor raíz \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ tabla de descriptores raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ \_ tabla de descriptor raíz \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ \_ tabla de descriptor raíz CD3DX12 \_ .

</dd> <dt>

**tabla de \_ \_ descriptor raíz CD3DX12 explícita \_ (const D3D12 \_ tabla de \_ descriptor raíz \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ tabla de \_ descriptor raíz CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ \_ tabla del descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

</dd> <dt>

**CD3DX12 \_ \_ tabla de descriptor raíz \_ (uint NUMDESCRIPTORRANGES, const D3D12 de \_ intervalo de descriptor \_ \* \_ pDescriptorRanges)**
</dt> <dd>

Crea una nueva instancia de una \_ tabla de \_ descriptor raíz CD3DX12 \_ , inicializando los parámetros siguientes:

UINT numDescriptorRanges

[**D3D12 \_ \_Rango de descriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**Init en línea (UINT numDescriptorRanges, const D3D12 \_ intervalo de descriptor \_ \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT numDescriptorRanges

[**D3D12 \_ \_Rango de descriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**Static inline init (D3D12 \_ root \_ descriptor \_ TABLE &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 \_ intervalo de descriptor \_ \* \_ pDescriptorRanges)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_ \_ Tabla del descriptor raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable

UINT numDescriptorRanges

[**D3D12 \_ \_Rango de descriptores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Tabla del \_ descriptor raíz de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





