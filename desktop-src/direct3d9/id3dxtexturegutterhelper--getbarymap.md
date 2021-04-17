---
description: Recupera las coordenadas de Barycentric de textura.
ms.assetid: f380a37f-b9c1-4433-b1d6-e9feeca79b30
title: 'ID3DXTextureGutterHelper:: GetBaryMap (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: 246117569b9106de18a31d08613146a3aa0d88c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707950"
---
# <a name="id3dxtexturegutterhelpergetbarymap-method"></a>ID3DXTextureGutterHelper:: GetBaryMap (método)

Recupera las coordenadas de Barycentric de textura.

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

Puntero a una estructura [**D3DXVECTOR2**](d3dxvector2.md) que contiene las dos primeras coordenadas Barycentric de cada textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

La tercera coordenada Barycentric se proporciona mediante:


```
    1 - ( pBaryData.x + pBaryData.y )
```



Las coordenadas Barycentric siempre se especifican con respecto al triángulo devuelto por [**ID3DXTextureGutterHelper:: GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md).

Las coordenadas Barycentric devueltas por este método solo son válidas para textura válida (que no es de clase 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para textura válido.

Los [**textura de clase 2**](id3dxtexturegutterhelper.md) se asignan al punto más cercano del triángulo en el espacio textura.

La aplicación debe asignar y administrar pBaryData.

Las coordenadas Barycentric definen un punto dentro de un triángulo en cuanto a los vértices del triángulo. Para obtener una descripción más detallada de las coordenadas de Barycentric, consulte Descripción de las [coordenadas del Barycentric de Wolfram](https://mathworld.wolfram.com/BarycentricCoordinates.html).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




