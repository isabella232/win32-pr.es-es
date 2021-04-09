---
description: Carga una superficie de un archivo en la memoria.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: Función D3DXLoadSurfaceFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821466"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a>D3DXLoadSurfaceFromFileInMemory función)

Carga una superficie de un archivo en la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestSurface* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**

Puntero a una interfaz [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) . Especifica la superficie de destino, que recibe la imagen.

</dd> <dt>

*pDestPalette* \[ de\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.

</dd> <dt>

*pDestRect* \[ de\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Especifica el rectángulo de destino. Establezca este parámetro en **null** para especificar toda la superficie.

</dd> <dt>

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al archivo en la memoria desde el que se va a cargar la superficie.

</dd> <dt>

*SrcData* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño del archivo en memoria, en bytes.

</dd> <dt>

*pSrcRect* \[ de\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Especifica el rectángulo de origen. Establezca este parámetro en **null** para especificar la imagen completa.

</dd> <dt>

*Filtro* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md) que controlan cómo se filtra la imagen. Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .

</dd> <dt>

*ColorKey* \[ de\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey. Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen. Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas. Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***

Puntero a una estructura de [**\_ información D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

La escritura en una superficie que no sea de nivel cero no hará que se actualice el rectángulo sucio. Si se llama a **D3DXLoadSurfaceFromFileInMemory** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
