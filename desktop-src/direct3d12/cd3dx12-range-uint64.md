---
title: CD3DX12_RANGE_UINT64 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura UINT64 de intervalo de D3D12 \_ .
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Estructura de CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718501"
---
# <a name="cd3dx12_range_uint64-structure"></a>CD3DX12 \_ intervalo \_ UINT64

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ UINT64 de intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ intervalo \_ UINT64 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un CD3DX12 de \_ intervalo \_ UINT64.

</dd> <dt>

**CD3DX12 \_ intervalo \_ UInt64 explícito (const D3D12 \_ intervalo \_ UInt64 &o)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12 de \_ intervalo \_ UInt64, inicializada con los valores copiados de una estructura [**\_ \_ UInt64 del intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

</dd> <dt>

**CD3DX12 \_ intervalo \_ UINT64 (UInt64 Begin, UInt64 end)**
</dt> <dd>

Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.

</dd> <dt>

**Operator const D3D12 \_ intervalo \_ UINT64& () Const**
</dt> <dd>

Conversión implícita a una \_ estructura UINT64 del intervalo de D3D12 \_ . Dado que D3D12 \_ Range \_ UInt64 es el tipo subyacente de CD3DX12 \_ Range \_ UInt64, el objeto simplemente se devuelve como una referencia UINT64 del intervalo const D3D12 \_ \_ a sí mismo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ intervalo \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





