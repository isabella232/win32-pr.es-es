---
description: Encapsula un marco de transformación en una jerarquía de marco de transformación.
ms.assetid: 838d75c2-41b2-4703-961b-893c34104c55
title: Estructura D3DXFRAME (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFRAME
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 33a851f3580045f5483541be155d3e8e85fddb22b530cb3f889253809f0b13aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123241"
---
# <a name="d3dxframe-structure"></a>Estructura D3DXFRAME

Encapsula un marco de transformación en una jerarquía de marco de transformación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXFRAME {
  LPSTR               Name;
  D3DXMATRIX          TransformationMatrix;
  LPD3DXMESHCONTAINER pMeshContainer;
  D3DXFRAME           *pFrameSibling;
  D3DXFRAME           *pFrameFirstChild;
} D3DXFRAME, *LPD3DXFRAME;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **LPSTR**

</dd> <dd>

Nombre del marco.

</dd> <dt>

**TransformationMatrix**
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)**

</dd> <dd>

Matriz de transformación.

</dd> <dt>

**pMeshContainer**
</dt> <dd>

Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**

</dd> <dd>

Puntero al contenedor de malla.

</dd> <dt>

**pFrameSibling**
</dt> <dd>

Tipo: *:D3DXFRAME **\***

</dd> <dd>

Puntero a un marco relacionado.

</dd> <dt>

**pFrameFirstChild**
</dt> <dd>

Tipo: *:D3DXFRAME **\***

</dd> <dd>

Puntero a un marco secundario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una aplicación puede derivar de esta estructura para agregar otros datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




