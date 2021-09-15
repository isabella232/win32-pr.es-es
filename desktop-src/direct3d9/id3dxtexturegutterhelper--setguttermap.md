---
description: Establece un valor de clase de texel que indica la clase de texel según la ubicación de cada texel.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: Método ID3DXTextureGutterHelper::SetGutterMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465435"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a>Método ID3DXTextureGutterHelper::SetGutterMap

Establece un valor de clase de texel que indica la clase de texel según la ubicación de cada texel.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGutterData* \[ En\]
</dt> <dd>

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)\***

Puntero a la clase texel. Las clases de texel posibles son las siguientes. No hay ninguna clase de textura 3.



| Texel (clase) | Ubicación de Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto no válido; No se usará el texel.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Dentro del triángulo.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Dentro del medianía.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Dentro del medianía; Texel se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper::ApplyGuttersFloat,**](id3dxtexturegutterhelper--applyguttersfloat.md) [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper::ApplyGuttersPRT.**](id3dxtexturegutterhelper--applyguttersprt.md) |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
