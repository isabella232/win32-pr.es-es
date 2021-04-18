---
description: Define los modos de filtrado de textura para una fase de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeración D3DTEXTUREFILTERTYPE (D3D9Types. h)
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
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717631"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Enumeración D3DTEXTUREFILTERTYPE

Define los modos de filtrado de textura para una fase de textura.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ ninguno**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), deshabilita mipmapping.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**\_Punto D3DTEXF**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que el filtrado de puntos se va a usar como filtro de aumento de textura o minificación, respectivamente. Cuando se usa con **D3DSAMP \_ MIPFILTER**, habilita mipmapping y especifica que el rasterizador elige el color del textura del nivel de MIP más próximo.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**\_Lineal D3DTEXF**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que el filtrado lineal se va a usar como filtro de aumento de textura o minificación, respectivamente. Cuando se usa con **D3DSAMP \_ MIPFILTER**, habilita el filtrado de mipmapping y trilineal; especifica que el rasterizador se interpola entre los dos niveles de MIP más cercanos.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotrópico**
</dt> <dd>

Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que el filtrado de texturas anisotrópico se usa como filtro de aumento de textura o minificación, respectivamente. Compensa la distorsión causada por la diferencia en el ángulo entre el polígono de textura y el plano de la pantalla. El uso con **D3DSAMP \_ MIPFILTER** es indefinido.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**
</dt> <dd>

Un filtro de carpa de ejemplo 4 usado como filtro de aumento de textura o minificación. El uso con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) es indefinido.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**
</dt> <dd>

Un filtro gaussiano de 4 muestras usado como filtro de aumento de textura o minificación. El uso con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) es indefinido.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**
</dt> <dd>

Filtro de circunvolución para texturas monocromas. Consulte [D3DFMT \_ a1](d3dformat.md).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Diferencias entre Direct3D 9 y Direct3D 9Ex:<br/> Esta marca solo está disponible en Direct3D 9Ex.<br/> |



 

El uso con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) es indefinido.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) usa D3DTEXTUREFILTERTYPE junto con [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para definir los modos de filtrado de textura para una fase de textura.

Para comprobar si un formato admite tipos de filtro de textura distintos \_ del punto D3DTEXF (que siempre se admite), llame a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con el \_ filtro de consulta D3DUSAGE \_ .

Establezca el filtro de ampliación de una fase de textura mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el \_ valor MAGFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como el tercer parámetro.

Establezca el filtro minificación de una fase de textura mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el \_ valor D3DSAMP MINFILTER como segundo parámetro y un miembro de esta enumeración como el tercer parámetro.

Establezca el filtro de textura para que use los niveles entre-MIP mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el \_ valor MIPFILTER de D3DSAMP como el segundo parámetro y un miembro de esta enumeración como el tercer parámetro.

No todos los modos de filtrado válidos para un dispositivo se aplicarán a las asignaciones de volumen. En general, se \_ \_ admitirán los filtros de ampliación lineal D3DTEXF Point y D3DTEXF para los mapas de volumen. Si \_ se establece D3DPTEXTURECAPS MIPVOLUMEMAP, se \_ admitirán los filtros de mapa MIP del punto D3DTEXF y \_ de D3DTEXF y D3DTEXF \_ lineal minificación para los mapas de volumen. El dispositivo puede o no admitir el \_ filtro de mipmap lineal D3DTEXF para mapas de volumen. Los dispositivos que admiten el filtrado anisotrópico para asignaciones 2D no admiten necesariamente el filtrado anisotrópico para mapas de volumen. Sin embargo, las aplicaciones que permiten el filtrado anisotrópico recibirán el mejor filtrado disponible (probablemente lineal) si no se admite el filtrado anisotrópico.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



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

 

 
