---
description: Carga un volumen desde otro volumen.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: Función D3DXLoadVolumeFromVolume (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003910"
---
# <a name="d3dxloadvolumefromvolume-function"></a>D3DXLoadVolumeFromVolume función)

Carga un volumen desde otro volumen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDestVolume* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Especifica el volumen de destino, que recibe la imagen.

</dd> <dt>

*pDestPalette* \[ de\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de destino de 256 colores o **null**.

</dd> <dt>

*pDestBox* \[ de\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntero a una estructura [**D3DBOX**](d3dbox.md) . Especifica el cuadro de destino. Establezca este parámetro en **null** para especificar el volumen completo.

</dd> <dt>

*pSrcVolume* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**

Puntero a una interfaz [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) . Especifica el volumen de origen.

</dd> <dt>

*pSrcPalette* \[ de\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de origen de 256 colores o **null**.

</dd> <dt>

*pSrcBox* \[ de\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntero a una estructura [**D3DBOX**](d3dbox.md) . Especifica el cuadro de código fuente. Establezca este parámetro en **null** para especificar el volumen completo.

</dd> <dt>

*Filtro* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o más [ \_ filtros de D3DX](d3dx-filter.md), que controla cómo se filtra la imagen. Especificar \_ el valor predeterminado de d3dx para este parámetro es el equivalente a especificar el filtro de d3dx \_ triángulo del filtro de \_ \| d3dx \_ \_ .

</dd> <dt>

*ColorKey* \[ de\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Valor de [**D3DCOLOR**](d3dcolor.md) que se va a reemplazar con negro transparente o 0 para deshabilitar Colorkey. Siempre es un color ARGB de 32 bits, independientemente del formato de la imagen de origen. Alfa es significativo y, normalmente, se debe establecer en FF para las claves de color opacas. Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio. Si se llama a **D3DXLoadVolumeFromVolume** y no se ha modificado la superficie (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la superficie.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromFileInMemory**](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromMemory**](d3dxloadvolumefrommemory.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
