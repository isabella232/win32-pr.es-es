---
description: Establece el índice de la cara de malla a la que pertenece cada elemento de textura.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: Método ID3DXTextureGutterHelper::SetFaceMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7de812f5445d0d8d704aeba939cf8cbc4441d4ed542bf716371a7fc12a1ba6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747394"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>Id3DXTextureGutterHelper::SetFaceMap (método)

Establece el índice de la cara de malla a la que pertenece cada elemento de textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFaceMap(
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

La entrada de datos de la cara de malla a este método solo es válida para los elementos de textura válidos (que no son de clase 0). [**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para los elementos de textura válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
