---
description: Mapas los índices del intervalo de 0 a 255 hasta los estados de transformación correspondientes.
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
ms.openlocfilehash: 03a93753790378a7066f4a3ffa6bc6b7fb8139b77f9096886161013653312bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850065"
---
# <a name="d3dts_worldmatrix-macro"></a>Macro WORLDMATRIX de D3DTS \_

Mapas los índices del intervalo de 0 a 255 hasta los estados de transformación correspondientes.

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

[**D3DTRANSFORMSTATETYPE que**](./d3dtransformstatetype.md) se asigna al índice *especificado.*

## <a name="remarks"></a>Comentarios

Los estados de transformación del intervalo de 256 a 511 están reservados para almacenar hasta 256 matrices que se pueden indexar mediante índices de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
