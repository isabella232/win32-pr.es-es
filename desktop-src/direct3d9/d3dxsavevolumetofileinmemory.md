---
description: Guarda un volumen en un búfer. El método crea un búfer ID3DXBuffer para almacenar los datos y devuelve ese objeto.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: Función D3DXSaveVolumeToFileInMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7c7326609d6d3c006f3c97aeff18de425a27569db63378864fc34335558117e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298408"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a>Función D3DXSaveVolumeToFileInMemory

Guarda un volumen en un búfer. El método crea un [**búfer ID3DXBuffer**](id3dxbuffer.md) para almacenar los datos y devuelve ese objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDestBuf* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a un [**búfer ID3DXBuffer**](id3dxbuffer.md) que almacenará la imagen.

</dd> <dt>

*DestFormat* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md)**

[**D3DXIMAGE \_ FILEFORMAT especificando**](./d3dximage-fileformat.md) el formato de archivo que se usará al guardar. Esta función admite el guardado en todos los **formatos \_ FILEFORMAT D3DXIMAGE** excepto Portable PortableMap (.ppm) y Targa/Truevision Graphics Adapter (.tga).

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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[**D3DXSaveVolumeToFile**](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
