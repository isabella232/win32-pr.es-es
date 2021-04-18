---
description: Describe un vector de punto flotante de 16 bits.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Estructura D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721460"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>Estructura D3DXFLOAT16 (D3dx9math. h)

Describe un vector de punto flotante de 16 bits.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Datos de 16 bits.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXFLOAT16**](d3dxfloat16-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
