---
title: CD3DX12_RECT estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura Rect de D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Estructura de CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717609"
---
# <a name="cd3dx12_rect-structure"></a>CD3DX12 \_ Rect (estructura)

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ Rect de D3D12**](d3d12-rect.md) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ Rect ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un CD3DX12 \_ Rect.

</dd> <dt>

**CD3DX12 \_ Rect explícito (const D3D12 \_ Rect& o)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12 \_ Rect, inicializada con el contenido de otra [**estructura \_ Rect de D3D12**](d3d12-rect.md) .

</dd> <dt>

**CD3DX12 \_ rectángulo explícito (largo izquierdo, largo superior, largo derecho, largo inferior)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12 \_ Rect, inicializando los siguientes parámetros:

LARGA izquierda

Superior larga

LARGA a la derecha

Inferior largo

</dd> <dt>

**~ CD3DX12 \_ Rect ()**
</dt> <dd>

Destruye una instancia de un CD3DX12 \_ Rect.

</dd> <dt>

**Operator const D3D12 \_ RECT& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ Rect**](d3d12-rect.md)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





