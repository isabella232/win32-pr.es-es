---
description: Define los modos de filtrado de textura para una fase de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeración D3DTEXTUREFILTERTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a9a55632ee1f1b8f2e40b1be1272411c7c24b3b18c576563ff9c0de7c79bc413
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069375"
---
# <a name="d3dtexturefiltertype-enumeration"></a>D3DTEXTUREFILTERTYPE (enumeración)

Define los modos de filtrado de textura para una fase de textura.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**
</dt> <dd>

Cuando se usa [**con \_ MIPFILTER de D3DSAMP,**](./d3dsamplerstatetype.md)deshabilita mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ POINT**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)especifica que el filtrado de puntos se usará como filtro de ampliación o minificación de textura, respectivamente. Cuando se usa con **\_ MIPFILTER de D3DSAMP,** habilita mipmapping y especifica que el rasterizador elige el color del texel del nivel de mip más cercano.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ LINEAR**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)especifica que el filtrado lineal se usará como filtro de ampliación o minificación de textura, respectivamente. Cuando se usa con **\_ MIPFILTER de D3DSAMP,** habilita el filtrado de mipmapping y trilinear; especifica que el rasterizador se interpola entre los dos niveles de mip más cercanos.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROPIC**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)especifica que el filtrado de textura anisotrófica se usa como filtro de ampliación o minificación de textura, respectivamente. Compensa la distorsión causada por la diferencia de ángulo entre el polígono de textura y el plano de la pantalla. El uso **con \_ MIPFILTER de D3DSAMP** no está definido.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Filtro de tienda de 4 muestras que se usa como filtro de ampliación o minificación de textura. El uso [**con \_ MIPFILTER de D3DSAMP**](./d3dsamplerstatetype.md) no está definido.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

Filtro gaussiano de 4 muestras que se usa como filtro de ampliación o minificación de textura. El uso [**con \_ MIPFILTER de D3DSAMP**](./d3dsamplerstatetype.md) no está definido.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

Filtro de convolución para texturas monocromáticas. Vea [D3DFMT \_ A1.](d3dformat.md)

Diferencias entre Direct3D 9 y Direct3D 9Ex:

- Esta marca solo está disponible en Direct3D 9Ex.



 

El uso [**con \_ MIPFILTER de D3DSAMP**](./d3dsamplerstatetype.md) no está definido.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) usa D3DTEXTUREFILTERTYPE junto con [**D3DSAMPLERSTATETYPE para**](./d3dsamplerstatetype.md) definir modos de filtrado de textura para una fase de textura.

Para comprobar si un formato admite tipos de filtro de textura distintos de D3DTEXF POINT (que siempre se admite), llame a \_ [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ FILTER.

Establezca el filtro de ampliación de una fase de textura llamando a [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el valor DE MAGFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como tercer \_ parámetro.

Establezca el filtro de minificación de una fase de textura llamando a [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el valor MINFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como tercer \_ parámetro.

Establezca el filtro de textura para usar entre niveles mipmap mediante una llamada a [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el valor MIPFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como tercer \_ parámetro.

No todos los modos de filtrado válidos para un dispositivo se aplicarán a los mapas de volumen. En general, se admiten los filtros de ampliación LINEAR D3DTEXF POINT y \_ D3DTEXF \_ para mapas de volúmenes. Si se establece D3DPTEXTURECAPS MIPVOLUMEMAP, se admiten los filtros \_ mipmap D3DTEXF POINT y \_ D3DTEXF POINT y \_ D3DTEXF LINEAR minification para mapas \_ de volúmenes. El dispositivo puede admitir o no el filtro mipmap LINEAR de D3DTEXF para \_ mapas de volúmenes. Los dispositivos que admiten el filtrado anisotropico para mapas 2D no admiten necesariamente el filtrado anisotropico para mapas de volúmenes. Sin embargo, las aplicaciones que habilitan el filtrado anisotropico recibirán el mejor filtrado disponible (probablemente lineal) si no se admite el filtrado anisotropico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh::GetDisplaceParam**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh::SetDisplaceParam**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
