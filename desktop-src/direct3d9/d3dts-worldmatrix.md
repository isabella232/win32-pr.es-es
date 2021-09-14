---
description: Mapas índices en el intervalo de 0 a 255 a los estados de transformación correspondientes.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: D3DTS_WORLDMATRIX macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963752"
---
# <a name="d3dts_worldmatrix-macro"></a>Macro WORLDMATRIX de D3DTS \_

Mapas índices en el intervalo de 0 a 255 a los estados de transformación correspondientes.

## <a name="syntax"></a>Sintaxis


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*índice* 
</dt> <dd>

Valor de índice en el intervalo de 0 a 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) que se asigna al índice *especificado.*

## <a name="remarks"></a>Observaciones

Los estados de transformación del intervalo de 256 a 511 están reservados para almacenar hasta 256 matrices que se pueden indexar mediante índices de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
