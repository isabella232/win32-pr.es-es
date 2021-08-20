---
description: Inicializa un color con los valores rojo, verde, azul y alfa proporcionados.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: D3DCOLOR_RGBA macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_RGBA
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4bd3f0a17b7bf9799630c0eec1c8140cc20a993f4f004819aa5433f7c8109efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911379"
---
# <a name="d3dcolor_rgba-macro"></a>Macro D3DCOLOR \_ RGBA

Inicializa un color con los valores rojo, verde, azul y alfa proporcionados.

## <a name="syntax"></a>Sintaxis


```C++
D3DCOLOR D3DCOLOR_RGBA(
   int r,
   int g,
   int b,
   int a
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*r* 
</dt> <dd>

Componente rojo del color. Este valor debe estar entre 0 y 255.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del color. Este valor debe estar entre 0 y 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul del color. Este valor debe estar entre 0 y 255.

</dd> <dt>

*Un* 
</dt> <dd>

Componente alfa del color. Este valor debe estar entre 0 y 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**valor D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGBA proporcionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




