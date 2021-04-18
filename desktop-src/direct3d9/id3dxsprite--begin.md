---
description: Prepara un dispositivo para dibujar sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite:: Begin (método) (D3dx9core. h)'
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
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718291"
---
# <a name="id3dxspritebegin-method"></a>ID3DXSprite:: Begin (método)

Prepara un dispositivo para dibujar sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de cero o más marcadores que describen las opciones de representación de Sprite. Para este método, las marcas válidas son:

-   D3DXSPRITE \_ ALPHABLEND
-   D3DXSPRITE de la \_ \_ cartelera
-   D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE
-   D3DXSPRITE \_ DONOTSAVESTATE
-   D3DXSPRITE \_ OBJECTSPACE
-   D3DXSPRITE \_ \_ profundidad de ordenación \_ \_ BACKTOFRONT
-   D3DXSPRITE \_ \_ profundidad de ordenación \_ \_ FRONTTOBACK
-   D3DXSPRITE \_ \_ ordenar \_ textura

Para obtener una descripción de las marcas y obtener información sobre cómo controlar la captura de estado de los dispositivos y las transformaciones de la vista de dispositivos, vea [D3DXSPRITE](d3dxsprite.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Se debe llamar a este método desde dentro de [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) . . . Secuencia [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) . **ID3DXSprite:: Begin** no se puede usar como sustituto de **IDirect3DDevice9:: BeginScene** o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).

Este método establecerá los siguientes Estados en el dispositivo.

Estados de representación:



| Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)) | Value                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3DRS \_ ALPHABLENDENABLE                                       | TRUE                                                                                                              |
| D3DRS \_ ALPHAFUNC                                              | D3DCMP \_ mayor                                                                                                   |
| D3DRS \_ ALPHAREF                                               | 0x00                                                                                                              |
| D3DRS \_ ALPHATESTENABLE                                        | AlphaCmpCaps                                                                                                      |
| D3DRS \_ BLENDOP                                                | D3DBLENDOP \_ Agregar                                                                                                   |
| Recorte de D3DRS \_                                               | TRUE                                                                                                              |
| D3DRS \_ CLIPPLANEENABLE                                        | false                                                                                                             |
| D3DRS \_ COLORWRITEENABLE                                       | D3DCOLORWRITEENABLE \_ alfa \| D3DCOLORWRITEENABLE \_ azul \| D3DCOLORWRITEENABLE \_ verde \| D3DCOLORWRITEENABLE \_ rojo |
| D3DRS \_ CULLMODE                                               | D3DCULL \_ ninguno                                                                                                     |
| D3DRS \_ DESTBLEND                                              | D3DBLEND \_ INVSRCALPHA                                                                                             |
| D3DRS \_ DIFFUSEMATERIALSOURCE                                  | D3DMCS \_ COLOR1                                                                                                    |
| D3DRS \_ ENABLEADAPTIVETESSELLATION                             | false                                                                                                             |
| D3DRS \_ FILLMODE                                               | D3DFILL \_ Solid                                                                                                    |
| D3DRS \_ FOGENABLE                                              | false                                                                                                             |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE                               | false                                                                                                             |
| \_Iluminación D3DRS                                               | false                                                                                                             |
| D3DRS \_ RANGEFOGENABLE                                         | false                                                                                                             |
| D3DRS \_ SEPARATEALPHABLENDENABLE                               | false                                                                                                             |
| D3DRS \_ SHADEMODE                                              | D3DSHADE \_ GOURAUD                                                                                                 |
| D3DRS \_ SPECULARENABLE                                         | false                                                                                                             |
| D3DRS \_ SRCBLEND                                               | D3DBLEND \_ SRCALPHA                                                                                                |
| D3DRS \_ SRGBWRITEENABLE                                        | false                                                                                                             |
| D3DRS \_ STENCILENABLE                                          | false                                                                                                             |
| D3DRS \_ VERTEXBLEND                                            | false                                                                                                             |
| D3DRS \_ WRAP0                                                  | 0                                                                                                                 |



 

Estados de la fase de textura:



| Identificador de la fase | Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)) | Value            |
|------------------|---------------------------------------------------------------------------|------------------|
| 0                | D3DTSS \_ ALPHAARG1                                                         | \_Textura D3DTA   |
| 0                | D3DTSS \_ ALPHAARG2                                                         | \_Difusión D3DTA   |
| 0                | D3DTSS \_ ALPHAOP                                                           | D3DTOP \_ modular |
| 0                | D3DTSS \_ COLORARG1                                                         | \_Textura D3DTA   |
| 0                | D3DTSS \_ COLORARG2                                                         | \_Difusión D3DTA   |
| 0                | D3DTSS \_ COLOROP                                                           | D3DTOP \_ modular |
| 0                | D3DTSS \_ TEXCOORDINDEX                                                     | 0                |
| 0                | D3DTSS \_ TEXTURETRANSFORMFLAGS                                             | Deshabilitación de D3DTTFF \_ |
| 1                | D3DTSS \_ ALPHAOP                                                           | Deshabilitación de D3DTOP \_  |
| 1                | D3DTSS \_ COLOROP                                                           | Deshabilitación de D3DTOP \_  |



 

Estados de muestra:



| Índice de fase de muestra | Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)) | Value                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 0                   | D3DSAMP \_ ADDRESSU                                               | \_Abrazadera D3DTADDRESS                                                                                             |
| 0                   | D3DSAMP \_ ADDRESSV                                               | \_Abrazadera D3DTADDRESS                                                                                             |
| 0                   | D3DSAMP \_ MAGFILTER                                              | D3DTEXF \_ anisotrópico si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MAGFANISOTROPIC; de lo contrario D3DTEXF \_ lineal |
| 0                   | D3DSAMP \_ MAXMIPLEVEL                                            | 0                                                                                                              |
| 0                   | D3DSAMP \_ MAXANISOTROPY                                          | MaxAnisotropy                                                                                                  |
| 0                   | D3DSAMP \_ MINFILTER                                              | D3DTEXF \_ anisotrópico si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MINFANISOTROPIC; de lo contrario D3DTEXF \_ lineal |
| 0                   | D3DSAMP \_ MIPFILTER                                              | D3DTEXF \_ linear si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MIPFLINEAR; de lo contrario D3DTEXF \_ Point            |
| 0                   | D3DSAMP \_ MIPMAPLODBIAS                                          | 0                                                                                                              |
| 0                   | D3DSAMP \_ SRGBTEXTURE                                            | 0                                                                                                              |



 

> [!Note]  
> Este método deshabilita N-patches.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[D3DXSPRITE](d3dxsprite.md)
</dt> </dl>

 

 
