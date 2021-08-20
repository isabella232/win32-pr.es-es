---
title: CD3DX12_RANGE_UINT64 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ RANGE \_ UINT64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- CD3DX12_RANGE_UINT64 estructura
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
ms.openlocfilehash: a07cb6a095c707b06b5b9982d29d73bb7bb9b6a32fca02233c50298a9804065a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098704"
---
# <a name="cd3dx12_range_uint64-structure"></a>Cd3DX12 \_ RANGE \_ (estructura UINT64)

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**D3D12 \_ RANGE \_ UINT64.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)

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

**CD3DX12 \_ RANGE \_ UINT64()**
</dt> <dd>

Crea una nueva instancia de CD3DX12 \_ RANGE \_ UINT64 sin inicializar.

</dd> <dt>

**explicit CD3DX12 \_ RANGE \_ UINT64(const D3D12 \_ RANGE \_ UINT64 &o)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12 RANGE UINT64, inicializado con valores copiados de una estructura \_ \_ [**D3D12 \_ RANGE \_ UINT64.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)

</dd> <dt>

**CD3DX12 \_ RANGE \_ UINT64(UINT64 begin, UINT64 end)**
</dt> <dd>

Crea una nueva instancia de CD3DX12 \_ DEPTH \_ STENCIL DESC1, inicializada con los \_ valores pasados en la lista de parámetros.

</dd> <dt>

**operator const D3D12 \_ RANGE \_ UINT64&() const**
</dt> <dd>

Conversión implícita a una estructura D3D12 \_ RANGE \_ UINT64. Dado que D3D12 RANGE UINT64 es el tipo subyacente de CD3DX12 RANGE UINT64, el objeto simplemente se devuelve como una referencia \_ \_ \_ \_ const D3D12 \_ RANGE \_ UINT64 a sí mismo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ RANGE \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





