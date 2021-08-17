---
description: Recupera el índice de la cara de malla a la que pertenece cada elemento de textura.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: Método ID3DXTextureGutterHelper::GetFaceMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5fce4400b1f778581f830fff60ef4e1519ad73752da02f5194abe64f433d43c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729195"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>Método ID3DXTextureGutterHelper::GetFaceMap

Recupera el índice de la cara de malla a la que pertenece cada elemento de textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFaceData* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero al índice de la cara de malla a la que pertenece cada elemento de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

Los datos de la cara de malla devueltos por este método solo son válidos para los elementos de textura válidos (que no son de clase 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para los elementos de textura válidos (que no son de clase 0).

Para [**los elementos de textura de clase 2,**](id3dxtexturegutterhelper.md)este método recupera la cara más cercana.

La aplicación debe asignar y administrar pFaceData.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
