---
description: Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animación de fotogramas clave almacenado en un formato de datos comprimido.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interfaz ID3DXCompressedAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d0a86e00d216ab0e0b4080abfe4f96d412d06adc86cf50d5d57705bdbab9a1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118804"
---
# <a name="id3dxcompressedanimationset-interface"></a>Interfaz ID3DXCompressedAnimationSet

Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animación de fotogramas clave almacenado en un formato de datos comprimido.

## <a name="members"></a>Miembros

La **interfaz ID3DXCompressedAnimationSet** hereda de [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXCompressedAnimationSet** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXCompressedAnimationSet** tiene estos métodos.



| Método                                                                                  | Descripción                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetCallbackKeys**](id3dxcompressedanimationset--getcallbackkeys.md)                 | Rellena una matriz con datos de clave de devolución de llamada usados para la animación de fotogramas clave.<br/>   |
| [**GetCompressedData**](id3dxcompressedanimationset--getcompresseddata.md)             | Obtiene el búfer de datos que almacena los datos comprimidos de animación de fotogramas clave.<br/> |
| [**GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | Obtiene el número de claves de devolución de llamada del conjunto de animaciones.<br/>                |
| [**GetPlaybackType**](id3dxcompressedanimationset--getplaybacktype.md)                 | Obtiene el tipo del bucle de reproducción del conjunto de animaciones.<br/>                     |
| [**GetSourceTicksPerSecond**](id3dxcompressedanimationset--getsourcetickspersecond.md) | Obtiene el número de tics de fotograma clave de animación que se producen por segundo.<br/>   |



 

## <a name="remarks"></a>Comentarios

Cree un conjunto de animaciones de fotogramas clave con formato comprimido [**con D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).

El tipo LPD3DXCOMPRESSEDANIMATIONSET se define como un puntero a esta interfaz.


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




