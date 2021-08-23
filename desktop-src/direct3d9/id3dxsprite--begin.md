---
description: Prepara un dispositivo para dibujar sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: Método ID3DXSprite::Begin (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94d3ee659937508f52e38513006701494a01ed4ff95fe6c75c56bd9638137160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119277835"
---
# <a name="id3dxspritebegin-method"></a>Método ID3DXSprite::Begin

Prepara un dispositivo para dibujar sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de cero o más marcas que describen las opciones de representación de sprites. Para este método, las marcas válidas son:

-   D3DXSPRITE \_ ALPHABLEND
-   D3DXSPRITEONES \_ \_
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   D3DXSPRITE \_ DONOTSAVESTATE
-   D3DXSPRITE \_ OBJECTSPACE
-   D3DXSPRITE \_ \_ SORT \_ DEPTH \_ BACKTOFRONT
-   FRONTTOBACK DE PROFUNDIDAD \_ \_ DE \_ ORDENACIÓN D3DXSPRITE \_
-   TEXTURA DE ORDENACIÓN D3DXSPRITE \_ \_ \_

Para obtener una descripción de las marcas y para obtener información sobre cómo controlar la captura de estado del dispositivo y las transformaciones de vista de dispositivo, vea [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Se debe llamar a este método desde dentro de [**un IDirect3DDevice9::BeginScene**](/windows/desktop/api) . . . [**Secuencia IDirect3DDevice9::EndScene.**](/windows/desktop/api) **ID3DXSprite::Begin** no se puede usar como sustituto de **IDirect3DDevice9::BeginScene** o [**ID3DXRenderToSurface::BeginScene.**](id3dxrendertosurface--beginscene.md)

Este método establecerá los siguientes estados en el dispositivo.

Estados de representación:



| Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Value                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | TRUE                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ GREATER                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| BLENDOP de D3DRS \_                                                | D3DBLENDOP \_ ADD                                                                                                   |
| RECORTE DE \_ D3DRS                                               | TRUE                                                                                                              |
| CLIPPLANEENABLE DE D3DRS \_                                        | FALSE                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ ALPHA \| D3DCOLORWRITEENABLE \_ BLUE \| D3DCOLORWRITEENABLE \_ GREEN \| D3DCOLORWRITEENABLE \_ RED |
| D3DRS \_ CULLMODE                                               | D3DCULL \_ NONE                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DIFFUSEMATERIALSOURCE                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | FALSE                                                                                                             |
| D3DRS \_ FILLMODE                                               | D3DFILL \_ SOLID                                                                                                    |
| D3DRS \_ RAGENABLE                                              | FALSE                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | FALSE                                                                                                             |
| ILUMINACIÓN D3DRS \_                                               | FALSE                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | FALSE                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE \_ GOURAUD                                                                                                 |
| D3DRS \_ SPECULARENABLE                                         | FALSE                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | FALSE                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | FALSE                                                                                                             |
| VERTEXBLEND de D3DRS \_                                            | FALSE                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Estados de la fase de textura:



| Identificador de fase | Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Value            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | TEXTURA \_ D3DTA   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | D3DTA \_ DIFUSO   |
| 0                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ MODULARTE |
| 0                | D3DTSS \_ COLORARG1                                                         | TEXTURA \_ D3DTA   |
| 0                | D3DTSS \_ COLORARG2                                                         | D3DTA \_ DIFUSO   |
| 0                | COLOROP de D3DTSS \_                                                           | MODULARTE D3DTOP \_ |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | TEXTURA DE \_ D3DTSSTRANSFORMFLAGS                                             | D3DTTFF \_ DISABLE |
| 1                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ DISABLE  |
| 1                | COLOROP de D3DTSS \_                                                           | D3DTOP \_ DISABLE  |



 

Estados del muestreador:



| Sampler Stage Index | Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Value                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ ADDRESSU                                               | D3DTADDRESS \_ CLAMP                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | D3DTADDRESS \_ CLAMP                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | D3DTEXF \_ ANISOTROPIC si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MAGFANISOTROPIC; de lo contrario, D3DTEXF \_ LINEAR |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropy                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | D3DTEXF \_ ANISOTROPIC si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MINFANISOTROPIC; de lo contrario, D3DTEXF \_ LINEAR |
| 0                   | MIPFILTER de D3DSAMP \_                                              | D3DTEXF \_ LINEAR si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MIPFLINEAR; de lo contrario, D3DTEXF \_ POINT            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> Este método deshabilita N revisiones.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
