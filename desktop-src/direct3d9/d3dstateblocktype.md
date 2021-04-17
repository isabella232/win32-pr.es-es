---
description: Conjuntos predefinidos de estado de canalización usados por bloques de estado (vea bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumeración D3DSTATEBLOCKTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 03b1834a2bd8e1b5f89922d908a558aa97e58f76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104552932"
---
# <a name="d3dstateblocktype-enumeration"></a>Enumeración D3DSTATEBLOCKTYPE

Conjuntos predefinidos de estado de canalización usados por bloques de estado (vea [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ todo**
</dt> <dd>

Capture el estado actual del [dispositivo](saving-all-device-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

Capturar el estado actual de los [píxeles](saving-pixel-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

Capturar el estado actual del [vértice](saving-vertex-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. No utilice este valor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Como se muestra en el diagrama siguiente, el estado de los vértices y los píxeles son ambos subconjuntos del estado del dispositivo.

![diagrama del estado del dispositivo, con estado de vértice y estado de píxel como subconjuntos](images/statesets.png)

Solo hay algunos Estados que se consideran el estado de vértices y de píxeles. Estos estados son:

-   Estado de representación: D3DRS \_ FOGDENSITY
-   Estado de representación: D3DRS \_ FOGSTART
-   Estado de representación: D3DRS \_ FOGEND
-   Estado de textura: D3DTSS \_ TEXCOORDINDEX
-   Estado de textura: D3DTSS \_ TEXTURETRANSFORMFLAGS

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
