---
description: 'Función D3DXGetImageInfoFromFile: recupera información sobre un archivo de imagen determinado.'
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: Función D3DXGetImageInfoFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb03b6482d140a3b78e43d8b99c60499ae6c8b16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567893"
---
# <a name="d3dxgetimageinfofromfile-function"></a>Función D3DXGetImageInfoFromFile

Recupera información sobre un archivo de imagen determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de archivo de la imagen sobre la que recuperar información. Si se definen UNICODE o UNICODE, este tipo de parámetro \_ es LPCWSTR; de lo contrario, el tipo es LPCSTR.

</dd> <dt>

*pSrcInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con la descripción de los datos del archivo de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

Esta función admite cadenas Unicode y ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXGetImageInfoFromFileInMemory**](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[**D3DXGetImageInfoFromResource**](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
