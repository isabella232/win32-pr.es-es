---
description: Describe un cuadro bloqueado (volumen).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX estructura (D3D9Types. h)
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
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280374"
---
# <a name="d3dlocked_box-structure"></a>Estructura del cuadro de D3DLOCKED \_

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

Desplazamiento en bytes desde el borde izquierdo de una fila hasta el borde izquierdo de la fila siguiente.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Tipo: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Desplazamiento de bytes desde la parte superior izquierda de un segmento hasta la parte superior izquierda del siguiente segmento más profundo.

</dd> <dt>

**pBits**
</dt> <dd>

Tipo: **void \***

</dd> <dd>

Puntero al principio del cuadro volumen. Si se proporcionó un [**D3DBOX**](d3dbox.md) a la llamada de Lockbox, pBits se desplazará correctamente desde el inicio del volumen.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los volúmenes se pueden visualizar como organizados en segmentos de superficies 2D de ancho x alto apiladas para crear un volumen x alto x de profundidad. Para obtener más información, vea [recursos de textura de volumen (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9:: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9:: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
