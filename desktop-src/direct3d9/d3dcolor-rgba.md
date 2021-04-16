---
description: Inicializa un color con los valores rojo, verde, azul y alfa proporcionados.
ms.assetid: 87d322f1-4a26-42fd-a1c3-7be220cecf0f
title: Macro D3DCOLOR_RGBA (D3d9types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649397"
---
# <a name="d3dcolor_rgba-macro"></a>D3DCOLOR \_ rgba (macro)

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

Componente rojo del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*g* 
</dt> <dd>

Componente verde del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*b* 
</dt> <dd>

Componente azul del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> <dt>

*un* 
</dt> <dd>

Componente alfa del color. Este valor debe estar en el intervalo comprendido entre 0 y 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de [**D3DCOLOR**](d3dcolor.md) que corresponde a los valores RGBA proporcionados.

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

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




