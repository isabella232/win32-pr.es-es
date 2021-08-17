---
description: Carga una superficie de la memoria.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: Función D3DXLoadSurfaceFromMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1b2bcb98f5fd64da221f73bf2cee4222d8925797acd4c7e01914e8e068d6e381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123053"
---
# <a name="d3dxloadsurfacefrommemory-function"></a>Función D3DXLoadSurfaceFromMemory

Carga una superficie de la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
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

*pSrcMemory* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a la esquina superior izquierda de la imagen de origen en memoria.

</dd> <dt>

*SrcFormat* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) el formato de píxel de la imagen de origen.

</dd> <dt>

*SrcPitch* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Paso de la imagen de origen, en bytes. Para los formatos DXT, este número debe representar el ancho de una fila de celdas, en bytes.

</dd> <dt>

*pSrcPalette* \[ En\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la paleta de origen de 256 colores o **NULL.**

</dd> <dt>

*pSrcRect* \[ En\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Puntero a una [**estructura RECT.**](/previous-versions//dd162897(v=vs.85)) Especifica las dimensiones de la imagen de origen en memoria. Este valor no puede ser **NULL.**

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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Esta función controla la conversión a y desde formatos de textura comprimidos.

Escribir en una superficie que no sea de nivel cero no hará que se actualice el rectángulo desnuciado. Si se llama a **D3DXLoadSurfaceFromMemory** y la superficie aún no estaba desasegada (es poco probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) en la superficie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
