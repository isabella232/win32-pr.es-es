---
description: Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animación de fotogramas clave.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interfaz ID3DXKeyframedAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060589"
---
# <a name="id3dxkeyframedanimationset-interface"></a>Interfaz ID3DXKeyframedAnimationSet

Una aplicación usa los métodos de esta interfaz para implementar un conjunto de animación de fotogramas clave.

## <a name="members"></a>Members

La **interfaz ID3DXKeyframedAnimationSet** hereda de [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXKeyframedAnimationSet** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXKeyframedAnimationSet** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compress**](id3dxkeyframedanimationset--compress.md)                                 | Transforma las animaciones de un conjunto de animación en un formato comprimido y devuelve un puntero al búfer que almacena los datos comprimidos.<br/> |
| [**GetCallbackKey**](id3dxkeyframedanimationset--getcallbackkey.md)                     | Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.<br/>                                                                        |
| [**GetCallbackKeys**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | Rellena una matriz con datos de clave de devolución de llamada usados para la animación de fotogramas clave.<br/>                                                                     |
| [**GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | Obtiene el número de claves de devolución de llamada del conjunto de animaciones.<br/>                                                                                  |
| [**GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | Obtiene el número de claves de rotación en la animación de fotogramas clave especificada.<br/>                                                                  |
| [**GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | Obtiene el número de claves de escala de la animación de fotogramas clave especificada.<br/>                                                                     |
| [**GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | Obtiene el número de claves de traducción en la animación de fotogramas clave especificada.<br/>                                                               |
| [**GetPlaybackType**](id3dxkeyframedanimationset--getplaybacktype.md)                   | Obtiene el tipo del bucle de reproducción del conjunto de animaciones.<br/>                                                                                       |
| [**GetRotationKey**](id3dxkeyframedanimationset--getrotationkey.md)                     | Obtiene información de rotación para un fotograma clave específico del conjunto de animaciones.<br/>                                                                 |
| [**GetRotationKeys**](id3dxkeyframedanimationset--getrotationkeys.md)                   | Rellena una matriz con datos de clave de rotación utilizados para la animación de fotogramas clave.<br/>                                                                   |
| [**GetScaleKey**](id3dxkeyframedanimationset--getscalekey.md)                           | Obtenga información de escala para un fotograma clave específico del conjunto de animaciones.<br/>                                                                    |
| [**GetScaleKeys**](id3dxkeyframedanimationset--getscalekeys.md)                         | Rellena una matriz con datos de clave de escala utilizados para la animación de fotogramas clave.<br/>                                                                        |
| [**GetSourceTicksPerSecond**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | Obtiene el número de tics de fotograma clave de animación que se producen por segundo.<br/>                                                                     |
| [**GetTranslationKey**](id3dxkeyframedanimationset--gettranslationkey.md)               | Obtenga información de traducción de un fotograma clave específico en el conjunto de animaciones.<br/>                                                              |
| [**GetTranslationKeys**](id3dxkeyframedanimationset--gettranslationkeys.md)             | Rellena una matriz con datos de clave de traducción utilizados para la animación de fotogramas clave.<br/>                                                                |
| [**RegisterAnimationSRTKeys**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | Registre los datos de fotogramas clave de escala, rotación y traducción (SRT) de una animación.<br/>                                                        |
| [**SetCallbackKey**](id3dxkeyframedanimationset--setcallbackkey.md)                     | Establece información sobre una devolución de llamada específica en el conjunto de animaciones.<br/>                                                                        |
| [**SetRotationKey**](id3dxkeyframedanimationset--setrotationkey.md)                     | Establezca la información de rotación de un fotograma clave específico en el conjunto de animaciones.<br/>                                                                 |
| [**SetScaleKey**](id3dxkeyframedanimationset--setscalekey.md)                           | Establezca la información de escala de un fotograma clave específico en el conjunto de animación.<br/>                                                                    |
| [**SetTranslationKey**](id3dxkeyframedanimationset--settranslationkey.md)               | Establezca la información de traducción de un fotograma clave específico en el conjunto de animaciones.<br/>                                                              |
| [**UnregisterAnimation**](id3dxkeyframedanimationset--unregisteranimation.md)           | Quite los datos de animación del conjunto de animaciones.<br/>                                                                                       |
| [**UnregisterRotationKey**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | Quita los datos de rotación en el fotograma clave especificado.<br/>                                                                                   |
| [**UnregisterScaleKey**](id3dxkeyframedanimationset--unregisterscalekey.md)             | Quita los datos de escala en el fotograma clave especificado.<br/>                                                                                      |
| [**UnregisterTranslationKey**](id3dxkeyframedanimationset--unregistertranslationkey.md) | Quita los datos de traducción en el fotograma clave especificado.<br/>                                                                                |



 

## <a name="remarks"></a>Observaciones

Cree un conjunto de animaciones con fotogramas clave [**con D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).

El tipo LPD3DXKEYFRAMEDANIMATIONSET se define como un puntero a esta interfaz.


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




