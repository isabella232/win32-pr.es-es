---
description: Tipo de datos para administrar un conjunto de parámetros de efectos predeterminados.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Estructura D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362576"
---
# <a name="d3dxeffectinstance-structure"></a>Estructura D3DXEFFECTINSTANCE

Tipo de datos para administrar un conjunto de parámetros de efectos predeterminados.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pEffectFilename**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nombre del archivo de efectos.

</dd> <dt>

**NumDefaults**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de parámetros predeterminados.

</dd> <dt>

**pDefaults**
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**

</dd> <dd>

Puntero a una matriz de elementos [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , cada uno de los cuales contiene un parámetro Effect.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
