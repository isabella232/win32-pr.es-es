---
title: CD3DX12_BOX estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de cuadro de D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Estructura de CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698204"
---
# <a name="cd3dx12_box-structure"></a>Estructura del cuadro de CD3DX12 \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ cuadro de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**Cuadro de CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ cuadro CD3DX12.

</dd> <dt>

**cuadro CD3DX12 explícito \_ (const D3D12 \_ Box& o)**
</dt> <dd>

Crea una nueva instancia de un \_ cuadro CD3DX12, inicializada con el contenido de otra estructura de [**\_ cuadros de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .

</dd> <dt>

**cuadro CD3DX12 explícito \_ (largo izquierdo, largo derecho)**
</dt> <dd>

Crea una nueva instancia de un \_ cuadro CD3DX12, inicializando los siguientes parámetros:

LARGA izquierda

LARGA a la derecha

</dd> <dt>

**cuadro CD3DX12 explícito \_ (largo izquierdo, largo superior, largo derecho, largo inferior)**
</dt> <dd>

Crea una nueva instancia de un \_ cuadro CD3DX12, inicializando los siguientes parámetros:

LARGA izquierda

Superior larga

LARGA a la derecha

Inferior largo

</dd> <dt>

**cuadro CD3DX12 explícito \_ (Long Left, Long Top, Long Front, Long Right, Long Bottom, Long back)**
</dt> <dd>

Crea una nueva instancia de un \_ cuadro CD3DX12, inicializando los siguientes parámetros:

LARGA izquierda

Superior larga

Inicial larga

LARGA a la derecha

Inferior largo

LARGA

</dd> <dt>

**~ CD3DX12 \_ Box ()**
</dt> <dd>

Destruye una instancia de un cuadro de CD3DX12 \_ .

</dd> <dt>

**Operator const D3D12 \_ BOX& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cuadro de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





