---
description: La interfaz ID3DXPRTBuffer se usa como búfer de datos para almacenar datos de vértices y píxeles para su uso con métodos y funciones de transferencia de radiancia precalutados (PRT).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interfaz ID3DXPRTBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69f4a40055adea1440436cc54cecc5735db95bc01787cb779cc8a7d6c51b0011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120549"
---
# <a name="id3dxprtbuffer-interface"></a>Interfaz ID3DXPRTBuffer

La interfaz ID3DXPRTBuffer se usa como búfer de datos para almacenar datos de vértices y píxeles para su uso con métodos y funciones de transferencia de radiancia precalutados (PRT).

## <a name="members"></a>Miembros

La **interfaz ID3DXPRTBuffer** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXPRTBuffer** tiene estos métodos.



| Método                                                   | Descripción                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | Agrega otro búfer a **ID3DXPRTBuffer** y almacena los resultados en **ID3DXPRTBuffer.**<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | Asocia un [**objeto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) al **objeto ID3DXPRTBuffer.**<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | Aplica los datos de los medianes de textura almacenados a **un búfer de textura ID3DXPRTBuffer.**<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | Extrae los datos del coeficiente de un canal de color del búfer para un intervalo de coeficientes especificado y agrega los datos a un [**objeto IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | Extrae los datos de coeficiente de un búfer de canal único y agrega los datos a un [**objeto ID3DXMesh.**](id3dxmesh.md)<br/>                                                              |
| [**GetHeight**](id3dxprtbuffer--getheight.md)           | Recupera el alto de la textura, en píxeles.<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | Recupera el número de canales de color usados en la memoria para almacenar muestras.<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Recupera el número de escalares por canal de color usado en memoria para almacenar muestras.<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | Recupera el número de vértices (o texeles) muestreados.<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | Recupera el ancho de la textura, en píxeles.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Indica si el búfer contiene una textura.<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | Bloquea un intervalo de datos de muestra de vértices o texeles y obtiene un puntero a la ubicación en la memoria del búfer.<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Desasocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) adjunto con el **objeto ID3DXPRTBuffer.**<br/>                                                   |
| [**Cambiar de tamaño**](id3dxprtbuffer--resize.md)                 | Cambia el número de muestras contenidas en el búfer.<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | Multiplica cada valor del búfer por un valor constante.<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | Finaliza la duración del puntero ppData devuelto por [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).<br/>                                                              |



 

## <a name="remarks"></a>Comentarios

La **interfaz ID3DXPRTBuffer** se obtiene mediante una llamada a las funciones [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex.**](d3dxcreateprtbuffertex.md)

El tipo LPD3DXPRTBUFFER se define como un puntero a la **interfaz ID3DXPRTBuffer.**


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
