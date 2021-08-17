---
description: Recupera coordenadas baricéntricas de texel.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: Método ID3DXTextureGutterHelper::GetBaryMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetBaryMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4183bf9bfa5065595073b8534e978367c3ec16bf76245d639da81292641afa81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729204"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>Método ID3DXTextureGutterHelper::GetBaryMap

Recupera coordenadas baricéntricas de texel.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBaryMap(
  [in, out] D3DXVECTOR2 *pBaryData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBaryData* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a una [**estructura D3DXVECTOR2**](d3dxvector2.md) que contiene las dos primeras coordenadas centradas en barras de cada texel.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

La tercera coordenada centrada en la barra está dada por:


```
    1 - ( pBaryData.x + pBaryData.y )
```



Las coordenadas centradas en barras siempre se especifican con respecto al triángulo devuelto por [**ID3DXTextureGutterHelper::GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).

Las coordenadas baricéntricas devueltas por este método solo son válidas para los elementos de textura válidos (que no son de clase 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para los elementos de textura válidos.

[**Los elementos de textura de clase 2**](id3dxtexturegutterhelper.md) se asignan al punto más cercano del triángulo en el espacio de texel.

La aplicación debe asignar y administrar pBaryData.

Las coordenadas barítricas definen un punto dentro de un triángulo en términos de los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas baricéntricas, vea [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




