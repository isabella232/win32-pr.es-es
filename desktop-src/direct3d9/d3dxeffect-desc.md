---
description: Describe un objeto de efecto.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: D3DXEFFECT_DESC estructura (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072823"
---
# <a name="d3dxeffect_desc-structure"></a>D3DXEFFECT \_ DESC (estructura)

Describe un objeto de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Creador**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Cadena que contiene el nombre del creador del efecto.

</dd> <dt>

**Parámetros**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de parámetros usados para el efecto.

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de técnicas que pueden representar el efecto.

</dd> <dt>

**Funciones**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de funciones que pueden representar el efecto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un objeto de efecto puede contener varias técnicas de representación y parámetros para el mismo efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
