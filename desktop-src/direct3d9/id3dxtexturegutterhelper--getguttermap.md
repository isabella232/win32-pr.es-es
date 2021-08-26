---
description: Recibe un valor de clase de texel que indica la clase de texel según la ubicación de cada texel.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: Método ID3DXTextureGutterHelper::GetGutterMap (D3DX9Mesh.h)
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
ms.openlocfilehash: 8ef2ed7b088e54dd82b1cc99422e1488139199ffe034e810de8e0a0bdb242f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095695"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>Método ID3DXTextureGutterHelper::GetGutterMap

Recibe un valor de clase de texel que indica la clase de texel según la ubicación de cada texel.

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

Tipo: **[ **BYTE**](../winprog/windows-data-types.md)\***

Puntero a la clase texel. Las clases de texel posibles son las siguientes. No hay ninguna clase de texel 3.



| Texel (clase) | Ubicación de Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto no válido; No se usará texel.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Dentro del triángulo.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Dentro del medianía.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Dentro del medianía; Texel se evaluará como un ejemplo completo en los métodos [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper::ApplyGuttersPRT.**](id3dxtexturegutterhelper--applyguttersprt.md) |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

La aplicación debe asignar y administrar pGutterData, con el tamaño especificado por:


```
texture width * texture height * sizeof(BYTE)
```



[**Id3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) e [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md)devuelven el ancho y el alto de la textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
