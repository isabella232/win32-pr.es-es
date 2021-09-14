---
description: Carga una superficie de un archivo.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: Función D3DXLoadSurfaceFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969764"
---
# <a name="d3dxloadsurfacefromfile-function"></a>Función D3DXLoadSurfaceFromFile

Carga una superficie de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestSurface* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntero a una [**interfaz IDirect3DSurface9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) Especifica la superficie de destino, que recibe la imagen.

</dd> <dt>

*pDestPalette* \[ En\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la paleta de destino de 256 colores o **NULL.**

</dd> <dt>

*pDestRect* \[ En\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) Especifica el rectángulo de destino. Establezca este parámetro en **NULL para** especificar toda la superficie.

</dd> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*pSrcRect* \[ En\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) Especifica el rectángulo de origen. Establezca este parámetro en **NULL** para especificar toda la imagen.

</dd> <dt>

*Filtro* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios [filtros D3DX \_ que](d3dx-filter.md) controlan cómo se filtra la imagen. Especificar D3DX DEFAULT para este parámetro equivale a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valor D3DCOLOR que**](d3dcolor.md) se reemplazará por negro transparente o 0 para deshabilitar la clave de color. Siempre es un color ARGB de 32 bits, independientemente del formato de imagen de origen. Alfa es significativo y normalmente debe establecerse en FF para las claves de color opacas. Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos del archivo de imagen de origen, o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXLoadSurfaceFromFileW. De lo contrario, la llamada de función se resuelve en D3DXLoadSurfaceFromFileA porque se usan cadenas ANSI.

Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Escribir en una superficie que no sea de nivel cero no hará que se actualice el rectángulo desnuciado. Si se llama a **D3DXLoadSurfaceFromFile** y la superficie aún no estaba desa prueba (es poco probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
