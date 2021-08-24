---
description: La interfaz ID3DXPRTCompBuffer almacena una versión comprimida de un búfer ID3DXPRTBuffer, para su uso con el análisis de componentes principales (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interfaz ID3DXPRTCompBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a84f1bc7b25af0c900f5587ba0d1dd948cac39bc52f706ff389c0ca9d053ec0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985615"
---
# <a name="id3dxprtcompbuffer-interface"></a>Interfaz ID3DXPRTCompBuffer

La **interfaz ID3DXPRTCompBuffer** almacena una versión comprimida de un búfer [**ID3DXPRTBuffer,**](id3dxprtbuffer.md) para su uso con el análisis de componentes principales (PCA).

## <a name="members"></a>Miembros

La **interfaz ID3DXPRTCompBuffer** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTCompBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXPRTCompBuffer** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtractBasis**](id3dxprtcompbuffer--extractbasis.md)           | Extrae los vectores de base de análisis de componentes principales y medio (PCA) para un clúster determinado de un búfer de datos comprimido **ID3DXPRTCompBuffer.**<br/>                                                                       |
| [**ExtractClusterIDs**](id3dxprtcompbuffer--extractclusterids.md) | Extrae los identificadores de clúster por ejemplo de un búfer de datos **comprimido ID3DXPRTCompBuffer.**<br/>                                                                                                                              |
| [**ExtractPCA**](id3dxprtcompbuffer--extractpca.md)               | Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido **ID3DXPRTCompBuffer.**<br/>                                                                               |
| [**ExtractTexture**](id3dxprtcompbuffer--extracttexture.md)       | Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido **ID3DXPRTCompBuffer** y agrega los datos a un objeto [**IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)<br/> |
| [**ExtractToMesh**](id3dxprtcompbuffer--extracttomesh.md)         | Extrae los coeficientes de proyección de análisis de componentes principales (PCA) por ejemplo de un búfer de datos comprimido **ID3DXPRTCompBuffer** y agrega los datos a un objeto [**ID3DXMesh.**](id3dxmesh.md)<br/>                 |
| [**GetHeight**](id3dxprtcompbuffer--getheight.md)                 | Recupera el alto de la textura, en píxeles.<br/>                                                                                                                                                                         |
| [**GetNumChannels**](id3dxprtcompbuffer--getnumchannels.md)       | Recupera el número de canales de color usados en la memoria para almacenar muestras.<br/>                                                                                                                                                 |
| [**GetNumClusters**](id3dxprtcompbuffer--getnumclusters.md)       | Recupera el número de clústeres que se usarán para la compresión.<br/>                                                                                                                                                                |
| [**GetNumCoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | Recupera el número de escalares por canal de color usado en memoria para almacenar muestras.<br/>                                                                                                                                      |
| [**GetNumPCA**](id3dxprtcompbuffer--getnumpca.md)                 | Recupera el número de vectores de base de análisis de componentes principales (PCA) que se usarán en cada clúster.<br/>                                                                                                                        |
| [**GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)         | Recupera el número de vértices (o texeles) muestreados.<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | Recupera el ancho de la textura, en píxeles.<br/>                                                                                                                                                                          |
| [**IsTexture**](id3dxprtcompbuffer--istexture.md)                 | Indica si el búfer contiene una textura.<br/>                                                                                                                                                                        |
| [**NormalizeData**](id3dxprtcompbuffer--normalizedata.md)         | Normaliza todos los pesos de análisis de componentes principales (PCA) para que estén entre -1 y 1. Los vectores base se modifican para reflejar esta normalización.<br/>                                                                  |



 

## <a name="remarks"></a>Comentarios

La **interfaz ID3DXPRTCompBuffer** se obtiene mediante una llamada a la función [**D3DXCreatePRTCompBuffer.**](d3dxcreateprtcompbuffer.md)

El tipo LPD3DXPRTCOMPBUFFER se define como un puntero a la **interfaz ID3DXPRTCompBuffer.**


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
