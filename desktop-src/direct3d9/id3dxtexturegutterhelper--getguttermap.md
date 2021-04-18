---
description: Recibe un valor de la clase textura que indica la clase textura según la ubicación de cada textura.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: 'ID3DXTextureGutterHelper:: GetGutterMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d973e716c598eaceaf7f75e6694a35691df4266
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649419"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>ID3DXTextureGutterHelper:: GetGutterMap (método)

Recibe un valor de la clase textura que indica la clase textura según la ubicación de cada textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGutterData* \[ in, out\]
</dt> <dd>

Tipo: **[ **byte**](../winprog/windows-data-types.md)\***

Puntero a la clase textura. Las clases posibles de textura son las siguientes. No hay ninguna clase textura 3.



| Clase textura | Ubicación de textura                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto no válido; no se usará textura.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triángulo interior.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Encuadernación interior.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Encuadernación interior; textura se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

La aplicación debe asignar y administrar pGutterData, con un tamaño dado por:


```
texture width * texture height * sizeof(BYTE)
```



[**ID3DXTextureGutterHelper:: GetWidth**](id3dxtexturegutterhelper--getwidth.md) y [**ID3DXTextureGutterHelper:: getHeight**](id3dxtexturegutterhelper--getheight.md)devuelven el ancho y el alto de la textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
