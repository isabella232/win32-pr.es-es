---
description: Inicializa un color con los valores de punto flotante rojo, verde, azul y alfa proporcionados.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751235"
---
# <a name="d3dcolor_colorvalue-macro"></a>Macro D3DCOLOR \_ COLORVALUE

Inicializa un color con los valores de punto flotante rojo, verde, azul y alfa proporcionados.

## <a name="syntax"></a>Sintaxis


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*r* 
</dt> <dd>

Componente rojo del color. Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del color. Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul del color. Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.

</dd> <dt>

*Un* 
</dt> <dd>

Componente alfa del color. Este valor debe ser un valor de punto flotante en el intervalo de 0,0 a 1,0.

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
</dt> </dl>

 

 




