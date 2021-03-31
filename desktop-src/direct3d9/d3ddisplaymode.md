---
description: Describe el modo de presentación.
ms.assetid: e83c03ee-2067-45c9-8fd8-8c4db5558df4
title: Estructura D3DDISPLAYMODE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYMODE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8bf73899742f02a9682a3a27319768db894fd682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157156"
---
# <a name="d3ddisplaymode-structure"></a>Estructura D3DDISPLAYMODE

Describe el modo de presentación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDISPLAYMODE {
  UINT      Width;
  UINT      Height;
  UINT      RefreshRate;
  D3DFORMAT Format;
} D3DDISPLAYMODE, *LPD3DDISPLAYMODE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la pantalla, en píxeles.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de la pantalla, en píxeles.

</dd> <dt>

**Frecuencia**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Frecuencia de actualización. El valor 0 indica un valor predeterminado del adaptador.

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de superficie del modo de presentación.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)
</dt> <dt>

[**GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode)
</dt> <dt>

[**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)
</dt> </dl>

 

 
