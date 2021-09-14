---
title: Función D3DX11GetImageInfoFromFile (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar la biblioteca DirectXTex, GetMetadataFromXXXFile (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos). Recupera información sobre un archivo de imagen determinado.
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- Función D3DX11GetImageInfoFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060850"
---
# <a name="d3dx11getimageinfofromfile-function"></a>Función D3DX11GetImageInfoFromFile

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar la biblioteca [DirectXTex,](https://github.com/Microsoft/DirectXTex) **GetMetadataFromXXXFile** (donde XXX es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admite TGA como un formato de origen de arte común para juegos).

 

Recupera información sobre un archivo de imagen determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Nombre de archivo de la imagen sobre la que recuperar información. Si se definen \_ UNICODE o UNICODE, este tipo de parámetro es LPCWSTR; de lo contrario, el tipo es LPCSTR.

</dd> <dt>

*pPump* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***

Bombeo de subprocesos opcional que se puede usar para cargar la información de forma asincrónica. Puede ser **NULL.** Vea [**ID3DX11ThreadPump (interfaz).**](id3dx11threadpump.md)

</dd> <dt>

*pSrcInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

Puntero a una [**información de imagen D3DX11 \_ \_**](d3dx11-image-info.md) que se rellenará con la descripción de los datos del archivo de origen.

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.** Si *pPump* no es **NULL,** *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

Esta función admite cadenas Unicode y ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

