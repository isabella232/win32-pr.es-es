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
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174837"
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

 

 




