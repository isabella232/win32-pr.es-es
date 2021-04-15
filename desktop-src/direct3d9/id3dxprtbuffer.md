---
description: La interfaz ID3DXPRTBuffer se usa como un búfer de datos para almacenar datos de vértices y píxeles para su uso con los métodos y funciones de transferencia Radiance precalculada (PRT).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interfaz ID3DXPRTBuffer (D3DX9Mesh. h)
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
ms.openlocfilehash: daadb5b0ad8155062e75ea4eca566a0afbf3631b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708115"
---
# <a name="id3dxprtbuffer-interface"></a>Interfaz ID3DXPRTBuffer

La interfaz ID3DXPRTBuffer se usa como un búfer de datos para almacenar datos de vértices y píxeles para su uso con los métodos y funciones de transferencia Radiance precalculada (PRT).

## <a name="members"></a>Miembros

La interfaz **ID3DXPRTBuffer** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXPRTBuffer** tiene estos métodos.



| Método                                                   | Descripción                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | Agrega otro búfer a **ID3DXPRTBuffer** y almacena los resultados en **ID3DXPRTBuffer**.<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | Asocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) al objeto **ID3DXPRTBuffer** .<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | Aplica los datos de medianil de textura almacenados a un búfer de textura de **ID3DXPRTBuffer** .<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | Extrae los datos coeficientes de un canal de color del búfer para un intervalo de coeficientes especificado y agrega los datos a un objeto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | Extrae los datos coeficientes de un búfer de un solo canal y agrega los datos a un objeto [**ID3DXMesh**](id3dxmesh.md) .<br/>                                                              |
| [**GetHeight**](id3dxprtbuffer--getheight.md)           | Recupera el alto de la textura, en píxeles.<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | Recupera el número de canales de color utilizados en la memoria para almacenar ejemplos.<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Recupera el número de escalares por canal de color usado en la memoria para almacenar ejemplos.<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | Recupera el número de vértices (o textura) muestreados.<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | Recupera el ancho de la textura, en píxeles.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Indica si el búfer contiene una textura.<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | Bloquea un intervalo de datos de ejemplo de vértice o textura y obtiene un puntero a la ubicación en la memoria de búfer.<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Desasocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) asociado con el objeto **ID3DXPRTBuffer** .<br/>                                                   |
| [**Cambiar de tamaño**](id3dxprtbuffer--resize.md)                 | Cambia el número de ejemplos contenidos en el búfer.<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | Multiplica cada valor del búfer por un valor constante.<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | Finaliza la duración del puntero ppData devuelto por [**ID3DXPRTBuffer:: LockBuffer**](id3dxprtbuffer--lockbuffer.md).<br/>                                                              |



 

## <a name="remarks"></a>Observaciones

La interfaz **ID3DXPRTBuffer** se obtiene llamando a las funciones [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) .

El tipo LPD3DXPRTBUFFER se define como un puntero a la interfaz **ID3DXPRTBuffer** .


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
