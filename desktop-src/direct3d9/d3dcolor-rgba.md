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
ms.openlocfilehash: c5047f29a9afbe5bb18db213f90e559b5e11d273
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072834"
---
# <a name="d3dcolor_rgba-macro"></a>Macro RGBA D3DCOLOR \_

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

Componente rojo del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> <dt>

*Un* 
</dt> <dd>

Componente alfa del color. Este valor debe estar en el intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el [**valor D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGBA proporcionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




