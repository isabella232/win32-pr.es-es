---
title: CD3DX12_RECT estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura RECT D3D12. \_
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- CD3DX12_RECT estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963799"
---
# <a name="cd3dx12_rect-structure"></a>Cd3DX12 \_ RECT (estructura)

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ RECT D3D12.**](d3d12-rect.md)

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



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ RECT()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ RECT CD3DX12.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RECT(const D3D12 \_ RECT& o)**
</dt> <dd>

Crea una nueva instancia de un RECT CD3DX12, inicializado con el contenido de otra estructura \_ [**\_ RECT D3D12.**](d3d12-rect.md)

</dd> <dt>

**EXPLICIT CD3DX12 \_ RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**
</dt> <dd>

Crea una nueva instancia de un RECT CD3DX12, \_ inicializando los parámetros siguientes:

LONG Left

LONG Top

LONG Right

LONG Bottom

</dd> <dt>

**~CD3DX12 \_ RECT()**
</dt> <dd>

Destruye una instancia de un RECT CD3DX12. \_

</dd> <dt>

**operator const D3D12 \_ RECT&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ RECT**](d3d12-rect.md)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





