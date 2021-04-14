---
description: La semántica asigna un parámetro a los registros del sombreador de vértices o píxeles. También pueden ser cadenas descriptivas opcionales adjuntas a parámetros que no son de registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Estructura D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424372"
---
# <a name="d3dxsemantic-structure"></a>Estructura D3DXSEMANTIC

La semántica asigna un parámetro a los registros del sombreador de vértices o píxeles. También pueden ser cadenas descriptivas opcionales adjuntas a parámetros que no son de registro.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opciones que identifican el modo en que se usan los recursos. Vea [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Opciones que modifican el modo en que se interpreta el uso. El índice de uso y uso constituye una declaración de vértice. Vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La semántica es necesaria para el sombreador de vértices y píxeles, los registros de entrada y salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
