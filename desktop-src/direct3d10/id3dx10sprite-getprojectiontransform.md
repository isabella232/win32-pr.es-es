---
description: Obtiene la matriz de proyección de sprite que se aplica a todos los sprites.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: Método ID3DX10Sprite::GetProjectionTransform (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5c3f5b0a0dc60316398575855c79bdb8ac9b7113f953af75489d5b65d9ff8fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301972"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a>Método ID3DX10Sprite::GetProjectionTransform

Obtiene la matriz de proyección de sprite que se aplica a todos los sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProjectionTransform* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Puntero a [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que se establecerá en la matriz de proyección del sprite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
