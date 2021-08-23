---
description: Describe una técnica utilizada por un efecto.
ms.assetid: 7ba2dbb3-8039-4d1c-ad9d-130d9bf3d80a
title: D3DXTECHNIQUE_DESC estructura (D3dx9effect.h)
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
ms.openlocfilehash: 7e835c0eac067825942568464df8d5d345a06b530b71b7eaf7f319eae5f5d366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630735"
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

**Pasa**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

El número de representaciones pasa lo que requiere la técnica. Vea la sección Comentarios.

</dd> <dt>

**anotaciones**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de anotaciones. Vea [Agregar información a parámetros de efecto con \_ anotaciones](using-an-effect.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Algunas tarjetas de vídeo pueden representar dos texturas en un solo paso. Sin embargo, si una tarjeta no tiene esta funcionalidad, a menudo es posible representar el mismo efecto en dos pases, con una textura para cada paso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efecto](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
