---
description: Contiene datos de rampa rojo, verde y azul.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: Estructura D3DGAMMARAMP (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fbd3acc35b7fd4998f5ba536c1fe4a28cf2a17153bf24aacde1f9f39bbbcd09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751005"
---
# <a name="d3dgammaramp-structure"></a>D3DGAMMARAMP (estructura)

Contiene datos de rampa rojo, verde y azul.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Rojo**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de 256 elementos WORD que describe la rampa gamma roja.

</dd> <dt>

**Verde**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de 256 elementos WORD que describe la rampa gamma verde.

</dd> <dt>

**Azul**
</dt> <dd>

Tipo: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Matriz de 256 elementos WORD que describe la rampa gamma azul.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
