---
description: 'Estructura D3DXFLOAT16 (D3dx9math.h): describe un vector de punto flotante de 16 bits.'
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Estructura D3DXFLOAT16 (D3dx9math.h)
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
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567948"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a>Estructura D3DXFLOAT16 (D3dx9math.h)

Describe un vector de punto flotante de 16 bits.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a>Members

<dl> <dt>

**Valor**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Datos de 16 bits.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXFLOAT16**](d3dxfloat16-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
