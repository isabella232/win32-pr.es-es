---
description: Tipo de datos para administrar un conjunto de parámetros de efecto predeterminados.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Estructura D3DXEFFECTINSTANCE (D3dx9mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072820"
---
# <a name="d3dxeffectinstance-structure"></a>D3DXEFFECTINSTANCE (estructura)

Tipo de datos para administrar un conjunto de parámetros de efecto predeterminados.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>Members

<dl> <dt>

**pEffectFilename**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nombre del archivo de efecto.

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

Puntero a una matriz de [**elementos D3DXEFFECTDEFAULT,**](d3dxeffectdefault.md) cada uno de los cuales contiene un parámetro de efecto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
