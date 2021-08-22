---
description: Guarda una textura en un archivo.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Función D3DXSaveTextureToFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954b761f8980a7397be1c79fbd8beb88ddbb29f29ce74557ca90cc77dee2ea5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988325"
---
# <a name="d3dxsavetexturetofile-function"></a>Función D3DXSaveTextureToFile

Guarda una textura en un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo de la imagen de destino. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*DestFormat* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT especificando**](./d3dximage-fileformat.md) el formato de archivo que se usará al guardar. Esta función admite el guardado en todos los **formatos \_ FILEFORMAT D3DXIMAGE,** excepto Portable PortableMap (.ppm) y Targa/Truevision Graphics Adapter (.tga).

</dd> <dt>

*pSrcTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntero a [**la interfaz IDirect3DBaseTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) que contiene la textura que se va a guardar.

</dd> <dt>

*pSrcPalette* \[ En\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una [**estructura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXSaveTextureToFileW. De lo contrario, la llamada de función se resuelve como D3DXSaveTextureToFileA porque se usan cadenas ANSI.

Esta función controla la conversión a y desde formatos de textura comprimidos.

Si el volumen no es dinámico (debido a un parámetro de uso establecido en 0 durante la creación) y se encuentra en la memoria de vídeo (el grupo de memoria establecido en \_ D3DPOOL DEFAULT), **D3DXSaveTextureToFile** producirá un error porque D3DX no puede bloquear volúmenes no dinámicos ubicados en la memoria de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
