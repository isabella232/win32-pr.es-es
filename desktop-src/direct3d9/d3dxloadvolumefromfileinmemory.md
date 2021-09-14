---
description: Carga un volumen desde un archivo en memoria.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: Función D3DXLoadVolumeFromFileInMemory (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969736"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a>Función D3DXLoadVolumeFromFileInMemory

Carga un volumen desde un archivo en memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestVolume* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntero a una [**interfaz IDirect3DVolume9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) Especifica el volumen de destino.

</dd> <dt>

*pDestPalette* \[ En\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) la paleta de destino de 256 colores o **NULL.**

</dd> <dt>

*pDestBox* \[ En\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntero a una [**estructura D3DBOX.**](d3dbox.md) Especifica el cuadro de destino. Establezca este parámetro en **NULL** para especificar todo el volumen.

</dd> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al archivo en memoria desde el que se va a cargar el volumen.

</dd> <dt>

*SrcDataSize* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Tamaño en bytes del archivo en memoria.

</dd> <dt>

*pSrcBox* \[ En\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntero a una [**estructura D3DBOX.**](d3dbox.md) Especifica el cuadro de origen. Establezca este parámetro en **NULL** para especificar todo el volumen.

</dd> <dt>

*Filtro* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios [filtros D3DX, \_ ](d3dx-filter.md)que controlan cómo se filtra la imagen. Especificar D3DX DEFAULT para este parámetro equivale a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*ColorKey* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valor D3DCOLOR**](d3dcolor.md) que se reemplazará por negro transparente o 0 para deshabilitar la clave de color. Siempre es un color ARGB de 32 bits, independientemente del formato de imagen de origen. Alfa es significativo y normalmente debe establecerse en FF para las claves de color opacas. Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen, o **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Esta función controla la conversión a y desde formatos de textura comprimidos y admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Escribir en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio. Si se llama a **D3DXLoadVolumeFromFileInMemory** y la textura aún no estaba desa prueba (es poco probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la textura del volumen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
