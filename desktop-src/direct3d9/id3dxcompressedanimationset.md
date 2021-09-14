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
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168521"
---
# <a name="id3dxcompressedanimationset-interface"></a>Interfaz ID3DXCompressedAnimationSet

Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animación de fotogramas clave almacenado en un formato de datos comprimido.

## <a name="members"></a>Members

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



 

## <a name="remarks"></a>Observaciones

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

 

 




