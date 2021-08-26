---
description: Conjuntos predefinidos de estado de canalización usados por bloques de estado (vea State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumeración D3DSTATEBLOCKTYPE (D3D9Types.h)
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
ms.openlocfilehash: 7780b7ded37ba976f32f4439ab793ae711be2f5790d03555a6a8be4f031571e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850195"
---
# <a name="d3dstateblocktype-enumeration"></a>D3DSTATEBLOCKTYPE (enumeración)

Conjuntos predefinidos de estado de canalización usados por los bloques de estado (vea State Blocks Save and Restore State (Direct3D 9) [Guardar y restaurar estado [(Direct3D 9)].](state-blocks-save-and-restore-state.md)

## <a name="syntax"></a>Syntax


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

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ ALL**
</dt> <dd>

Capture el estado [del dispositivo actual.](saving-all-device-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

Capture el estado [de píxel actual.](saving-pixel-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

Capture el estado [del vértice actual.](saving-vertex-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. No use este valor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Como se muestra en el diagrama siguiente, el estado de los vértices y los píxeles son subconjuntos del estado del dispositivo.

![diagrama del estado del dispositivo, con estado de vértice y estado de píxeles como subconjuntos](images/statesets.png)

Solo hay algunos estados que se consideran estado de vértice y píxel. Estos estados son:

-   Estado de representación: D3DRS \_ RAGDENSITY
-   Estado de representación: D3DRSSTART \_ DESTART
-   Estado de representación: \_ D3DRSEND
-   Estado de textura: D3DTSS \_ TEXCOORDINDEX
-   Estado de textura: \_ TEXTURETRANSFORMFLAGS de D3DTSS

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
