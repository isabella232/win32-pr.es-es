---
description: Devuelve el cuadrado de la longitud de un cuaternión.
ms.assetid: 358d2a2b-7baf-4ae9-9b92-7a7f01ca843b
title: Función D3DXQuaternionLengthSq (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 062339144a182d0ceeec27d34dd0d572d470ef10fcc1722375f89156b6b55874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631085"
---
# <a name="d3dxquaternionlengthsq-function"></a>Función D3DXQuaternionLengthSq

Devuelve el cuadrado de la longitud de un cuaternión.

## <a name="syntax"></a>Sintaxis


```C++
FLOAT D3DXQuaternionLengthSq(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQ* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud cuadrada del cuaternión.

## <a name="remarks"></a>Comentarios

Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLength**](d3dxquaternionlength.md)
</dt> </dl>

 

 
