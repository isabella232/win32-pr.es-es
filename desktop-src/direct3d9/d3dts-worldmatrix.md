---
description: Asigna índices en el intervalo de 0 a 255 a los Estados de transformación correspondientes.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Macro D3DTS_WORLDMATRIX (D3d9types. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547859"
---
# <a name="d3dts_worldmatrix-macro"></a>D3DTS \_ WORLDMATRIX (macro)

Asigna índices en el intervalo de 0 a 255 a los Estados de transformación correspondientes.

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

Un valor de índice en el intervalo comprendido entre 0 y 255.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) que se asigna al *Índice* especificado.

## <a name="remarks"></a>Observaciones

Los Estados de transformación en el intervalo de 256 a 511 se reservan para almacenar hasta 256 matrices que se pueden indexar con índices de 8 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
