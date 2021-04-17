---
title: CD3DX12_SUBRESOURCE_RANGE_UINT64 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura UINT64 del intervalo de SUBRECURSO D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Estructura de CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717594"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>\_ \_ Estructura UINT64 del intervalo de Subrecursos de CD3DX12 \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ UINT64 del \_ intervalo \_ de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Intervalo de SUBRECURSO CD3DX12 \_ \_ UINT64 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ intervalo de subrecurso de \_ CD3DX12 \_ UINT64.

</dd> <dt>

**intervalo de \_ SUBRECURSO CD3DX12 explícito \_ \_ UINT64 (const D3D12 \_ subresource \_ intervalo \_ UInt64 &o)**
</dt> <dd>

Crea una nueva instancia de un \_ intervalo de SUBRECURSO CD3DX12 \_ \_ UInt64, inicializado con los valores copiados de una estructura UInt64 del [**\_ \_ intervalo \_ de Subrecursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

</dd> <dt>

**\_ \_ Intervalo de subrecurso \_ de CD3DX12 UInt64 (subrecurso uint, const D3D12 \_ intervalo \_ UInt64& intervalo)**
</dt> <dd>

Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.

</dd> <dt>

**\_Intervalo de SUBRECURSO CD3DX12 \_ \_ UInt64 (subrecurso uint, UINT64 Begin, UInt64 end)**
</dt> <dd>

Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.

</dd> <dt>

**operador const D3D12 \_ subresource \_ intervalo \_ UINT64& () Const**
</dt> <dd>

Conversión implícita a una \_ estructura UINT64 del intervalo de SUBRECURSO D3D12 \_ \_ . Dado que \_ \_ el intervalo de Subrecursos \_ de D3D12 UInt64 es el tipo subyacente del \_ intervalo de subrecurso de CD3DX12 \_ \_ UInt64, el objeto simplemente se devuelve como una \_ referencia de galería de símbolos de profundidad const D3D12 \_ \_ DESC1 a sí mismo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Intervalo de SUBrecurso de D3D12 \_ \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





