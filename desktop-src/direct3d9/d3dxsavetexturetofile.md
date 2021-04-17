---
description: Guarda una textura en un archivo.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: Función D3DXSaveTextureToFile (D3dx9tex. h)
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
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698225"
---
# <a name="d3dxsavetexturetofile-function"></a>D3DXSaveTextureToFile función)

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

*pDestFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo de la imagen de destino. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*DestFormat* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md) que especifica el formato de archivo que se va a utilizar al guardar. Esta función permite guardar en todos los formatos **\_ FILEFORMAT de D3DXIMAGE** , excepto el portable pixmap (. ppm) y el adaptador de gráficos Targa/Truevision (. TGA).

</dd> <dt>

*pSrcTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Puntero a la interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , que contiene la textura que se va a guardar.

</dd> <dt>

*pSrcPalette* \[ de\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXSaveTextureToFileW. De lo contrario, la llamada de función se resuelve como D3DXSaveTextureToFileA porque se usan cadenas ANSI.

Esta función controla la conversión a y desde formatos de textura comprimidos.

Si el volumen no es dinámico (debido a un parámetro de uso establecido en 0 en la creación) y se encuentra en la memoria de vídeo (el grupo de memoria se establece en el \_ valor predeterminado de D3DPOOL), **D3DXSaveTextureToFile** producirá un error porque D3DX no bloquea volúmenes no dinámicos ubicados en la memoria de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
