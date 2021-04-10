---
description: Describe una técnica utilizada por un efecto.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTECHNIQUE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 35dd483a983f17371d6a77e6c020b3a45d9e9360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083716"
---
# <a name="d3dxtechnique_desc-structure"></a>D3DXTECHNIQUE \_ DESC (estructura)

Describe una técnica utilizada por un efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DXTECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DXTECHNIQUE_DESC, *LPD3DXTECHNIQUE_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Cadena que contiene el nombre de la técnica.

</dd> <dt>

**Paso**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de pasos de representación que requiere la técnica. Vea la sección Comentarios.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de anotaciones. Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Algunas tarjetas de vídeo pueden representar dos texturas en un solo paso. Sin embargo, si una tarjeta no tiene esta capacidad, a menudo es posible representar el mismo efecto en dos pasos, utilizando una textura para cada paso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
