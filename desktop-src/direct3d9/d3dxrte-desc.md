---
description: Describe un destino de representación fuera de la pantalla utilizado por una instancia de ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: D3DXRTE_DESC estructura (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 69a5957bc9338abac4441f65066a43efb7dabead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280307"
---
# <a name="d3dxrte_desc-structure"></a>D3DXRTE \_ DESC (estructura)

Describe un destino de representación fuera de la pantalla utilizado por una instancia de [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tamaño**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho y alto en píxeles.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número máximo de niveles de detalle (LOD).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato de búfer de color.

</dd> <dt>

**DepthStencil**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Indica si se necesita el búfer z.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato del búfer de profundidad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este método se usa para devolver los parámetros de creación que se usan al crear un objeto [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
