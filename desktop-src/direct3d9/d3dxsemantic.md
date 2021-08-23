---
description: La semántica asigna un parámetro a registros de sombreador de vértices o píxeles. También pueden ser cadenas descriptivas opcionales asociadas a parámetros que no son de registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Estructura D3DXSEMANTIC (D3dx9shader.h)
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
ms.openlocfilehash: 2534df72c246fdec361597a8e156f7f19b341ae35fcc04b3bdc6eb71c2903fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631025"
---
# <a name="d3dxsemantic-structure"></a>Estructura D3DXSEMANTIC

La semántica asigna un parámetro a registros de sombreador de vértices o píxeles. También pueden ser cadenas descriptivas opcionales asociadas a parámetros que no son de registro.

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

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opciones que identifican cómo se usan los recursos. Vea [**D3DDECLUSAGE.**](./d3ddeclusage.md)

</dd> <dt>

**UsageIndex**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Opciones que modifican cómo se interpreta el uso. El índice de uso y uso forma una declaración de vértice. Vea [Declaración de vértice (Direct3D 9).](vertex-declaration.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La semántica es necesaria para el sombreador de vértices y píxeles, los registros de entrada y salida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
