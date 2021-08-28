---
description: Describe un cuadro bloqueado (volumen).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: deb83c71eb9fe9fa5c69667e6dc48187144fa5c18e1daf084e4a04c1fd213744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750995"
---
# <a name="d3dlocked_box-structure"></a>D3DLOCKED \_ BOX (estructura)

Describe un cuadro bloqueado (volumen).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>Miembros

<dl> <dt>

**RowPitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento de bytes desde el borde izquierdo de una fila hasta el borde izquierdo de la fila siguiente.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento de bytes de la parte superior izquierda de un segmento a la parte superior izquierda del siguiente segmento más profundo.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **\* void**

</dd> <dd>

Puntero al principio del cuadro de volumen. Si se [**proporcionó un D3DBOX**](d3dbox.md) a la llamada a LockBox, los pBits se desplazarán correctamente desde el inicio del volumen.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los volúmenes se pueden visualizar como organizados en segmentos de superficies 2D de ancho x alto apilados para crear un volumen de ancho x alto x profundidad. Para obtener más información, vea [Recursos de textura de volumen (Direct3D 9).](volume-texture-resources.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
