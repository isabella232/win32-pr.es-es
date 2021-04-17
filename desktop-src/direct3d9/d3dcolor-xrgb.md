---
description: Inicializa un color con los valores rojo, verde y azul proporcionados.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: Macro D3DCOLOR_XRGB (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 4932e34979b0913f27874e57cfa881f18fb16364
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424348"
---
# <a name="d3dcolor_xrgb-macro"></a>D3DCOLOR \_ XRGB (macro)

Inicializa un color con los valores rojo, verde y azul proporcionados.

## <a name="syntax"></a>Sintaxis


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*r* 
</dt> <dd>

Componente rojo del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGB proporcionados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**\_ARGB D3DCOLOR**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> </dl>

 

 




