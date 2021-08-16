---
description: Guarda un volumen en un archivo en el disco.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: Función D3DXSaveVolumeToFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e6c5a03f9e1874d7706ecbf43cfd312abc472b8e7127ba9f21a35313374157b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524450"
---
# <a name="d3dxsavevolumetofile-function"></a>Función D3DXSaveVolumeToFile

Guarda un volumen en un archivo en el disco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo de la imagen de destino. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*DestFormat* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT especificando**](./d3dximage-fileformat.md) el formato de archivo que se usará al guardar. Esta función admite el guardado en todos los **formatos \_ FILEFORMAT D3DXIMAGE,** excepto PortableMap (.ppm) y Targa/Truevision Graphics Adapter (.tga).

</dd> <dt>

*pSrcVolume* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntero a [**la interfaz IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) que contiene la imagen que se va a guardar.

</dd> <dt>

*pSrcPalette* \[ En\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una [**estructura PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene una paleta de 256 colores. Este parámetro puede ser **NULL**.

</dd> <dt>

*pSrcBox* \[ En\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntero a una [**estructura D3DBOX.**](d3dbox.md) Especifica el cuadro de origen. Establezca este parámetro en **NULL** para especificar todo el volumen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXSaveVolumeToFileW. De lo contrario, la llamada de función se resuelve >D3DXSaveVolumeToFileA porque se usan cadenas ANSI.

Esta función controla la conversión a y desde formatos de textura comprimidos.

Si el volumen no es dinámico (debido a un parámetro de uso establecido en 0 durante la creación) y se encuentra en la memoria de vídeo (el grupo de memoria establecido en D3DPOOL \_ DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) producirá un error porque D3DX no puede bloquear volúmenes no dinámicos ubicados en la memoria de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveSurfaceToFile**](d3dxsavesurfacetofile.md)
</dt> <dt>

[**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md)
</dt> <dt>

[**D3DXSaveVolumeToFileInMemory**](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
