---
description: Tipos de revisión de malla.
ms.assetid: 229d01b2-781c-48a8-93f2-9dd9dbd67f3e
title: Enumeración D3DXPATCHMESHTYPE (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHMESHTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 1e5953e81431878b293a554665ea2b1bac53e62d80ee3a6d20e55385a82b098d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119065"
---
# <a name="d3dxpatchmeshtype-enumeration"></a>D3DXPATCHMESHTYPE (enumeración)

Tipos de revisión de malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPATCHMESHTYPE { 
  D3DXPATCHMESH_RECT         = 0x001,
  D3DXPATCHMESH_TRI          = 0x002,
  D3DXPATCHMESH_NPATCH       = 0x003,
  D3DXPATCHMESH_FORCE_DWORD  = 0x7fffffff
} D3DXPATCHMESHTYPE, *LPD3DXPATCHMESHTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXPATCHMESH_RECT"></span><span id="d3dxpatchmesh_rect"></span>**D3DXPATCHMESH \_ RECT**
</dt> <dd>

Tipo de malla de revisión de rectángulo.

</dd> <dt>

<span id="D3DXPATCHMESH_TRI"></span><span id="d3dxpatchmesh_tri"></span>**D3DXPATCHMESH \_ TRI**
</dt> <dd>

Tipo de malla de revisión de triángulo.

</dd> <dt>

<span id="D3DXPATCHMESH_NPATCH"></span><span id="d3dxpatchmesh_npatch"></span>**D3DXPATCHMESH \_ NPATCH**
</dt> <dd>

Tipo de malla de N revisiones.

</dd> <dt>

<span id="D3DXPATCHMESH_FORCE_DWORD"></span><span id="d3dxpatchmesh_force_dword"></span>**D3DXPATCHMESH \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las revisiones de triángulo tienen tres lados y se describen en [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md). Las revisiones de rectángulo son de cuatro lados y se describen en [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[Usar Higher-Order primitivos (Direct3D 9)](using-higher-order-primitives.md)
</dt> </dl>

 

 




