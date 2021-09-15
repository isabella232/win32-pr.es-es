---
description: Recupera las coordenadas de textura (u, v) de cada texel.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: Método ID3DXTextureGutterHelper::GetTexelMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465960"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a>Método ID3DXTextureGutterHelper::GetTexelMap

Recupera las coordenadas de textura (u, v) de cada texel.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexelData* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a la ubicación en coordenadas de textura de píxel (u, v) donde se encuentra cada textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

Para los elementos de textura de clase 2 y [**4,**](id3dxtexturegutterhelper.md)las coordenadas de textura devueltas (u, v) corresponden al punto más cercano del triángulo más cercano.

La aplicación debe asignar y administrar pTexelData.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




