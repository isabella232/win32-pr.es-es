---
description: Carga un volumen de la memoria.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: Función D3DXLoadVolumeFromMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707743"
---
# <a name="d3dxloadvolumefrommemory-function"></a>D3DXLoadVolumeFromMemory función)

Carga un volumen de la memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
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

*pSrcMemory* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero en la esquina superior izquierda del volumen de origen en la memoria.

</dd> <dt>

*SrcFormat* \[ de\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , el formato de píxel del volumen de origen.

</dd> <dt>

*SrcRowPitch* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tono de la imagen de origen, en bytes. En el caso de los formatos de DXT (formatos de textura comprimidos), este número debe representar el tamaño de una fila de celdas, en bytes.

</dd> <dt>

*SrcSlicePitch* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tono de la imagen de origen, en bytes. En el caso de los formatos de DXT (formatos de textura comprimidos), este número debe representar el tamaño de un segmento de celdas, en bytes.

</dd> <dt>

*pSrcPalette* \[ de\]
</dt> <dd>

Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Puntero a una estructura [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la paleta de origen de 256 colores o **null**.

</dd> <dt>

*pSrcBox* \[ de\]
</dt> <dd>

Tipo: **const [**D3DBOX**](d3dbox.md) \***

Puntero a una estructura [**D3DBOX**](d3dbox.md) . Especifica el cuadro de código fuente. **Null** no es un valor válido para este parámetro.

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

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

La escritura en una superficie que no sea de nivel cero de la textura del volumen no hará que se actualice el rectángulo sucio. Si se llama a **D3DXLoadVolumeFromMemory** y la textura no se ha modificado todavía (esto no es probable en escenarios de uso normal), la aplicación debe llamar explícitamente a [**IDirect3DVolumeTexture9:: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) en la textura del volumen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md)
</dt> <dt>

[**D3DXLoadVolumeFromResource**](d3dxloadvolumefromresource.md)
</dt> <dt>

[**D3DXLoadVolumeFromVolume**](d3dxloadvolumefromvolume.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
