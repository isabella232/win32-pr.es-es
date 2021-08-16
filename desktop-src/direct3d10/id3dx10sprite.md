---
description: La interfaz ID3DX10Sprite proporciona un conjunto de métodos que simplifican el proceso de dibujo de sprites mediante Microsoft Direct3D. Esta interfaz puede funcionar en un conjunto de muchos sprites.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: Interfaz ID3DX10Sprite (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8495d967d0f512e16a06506e73ac1a35bf5fa380924cdbe6513b06a43502b137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301933"
---
# <a name="id3dx10sprite-interface"></a>Interfaz ID3DX10Sprite

La interfaz ID3DX10Sprite proporciona un conjunto de métodos que simplifican el proceso de dibujo de sprites mediante Microsoft Direct3D. Esta interfaz puede funcionar en un conjunto de muchos sprites.

## <a name="members"></a>Miembros

La **interfaz ID3DX10Sprite** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10Sprite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX10Sprite** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comenzar**](id3dx10sprite-begin.md)                                   | Prepare un dispositivo para dibujar sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | Agregue una matriz de sprites al lote de sprites que se va a representar. Se debe llamar a esto entre las llamadas a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End,**](id3dx10sprite-end.md)y se debe llamar a [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) antes de End para enviar todos los sprites por lotes al dispositivo para su representación. Este método de dibujo es muy útil al dibujar un pequeño número de sprites que desea almacenar en búfer en un lote grande, como las fuentes.<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | Dibuje una matriz de sprites. Esto enviará inmediatamente los sprites al dispositivo para su representación, que es diferente de [**ID3DX10Sprite::D rawSpritesBuffered,**](id3dx10sprite-drawspritesbuffered.md) que solo agrega una matriz de sprites a un lote de sprites que se representarán cuando se llama a [**ID3DX10Sprite::Flush.**](id3dx10sprite-flush.md) Este método de dibujo es muy útil al dibujar un gran número de sprites que ya se han ordenado en la CPU (o no es necesario ordenar), como en un sistema de partículas. Se debe llamar a esto entre llamadas a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End**](id3dx10sprite-end.md).<br/> |
| [**End**](id3dx10sprite-end.md)                                       | Llame a esto después de ID3DX10Sprite::Flush. Si se especificó D3DX10 SPRITE SAVE STATE cuando se llamó a ID3DX10Sprite::Begin, esta API restaurará el estado del dispositivo a como estaba antes de llamar a \_ \_ \_ ID3DX10Sprite::Begin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Vaciar**](id3dx10sprite-flush.md)                                   | Fuerce que todos los sprites por lotes se envían al dispositivo. Los estados del dispositivo permanecen como estaban después de la última llamada a ID3DX10Sprite::Begin. A continuación, se borra la lista de sprites por lotes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Recupere el dispositivo asociado al objeto sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | Obtiene la matriz de proyección de sprite que se aplica a todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Obtenga la transformación de vista que se aplica a todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | Establezca la matriz de proyección para todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Establezca la transformación de vista que se aplica a todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentarios

La interfaz ID3DX10Sprite se obtiene llamando a la función [**D3DX10CreateSprite.**](d3dx10createsprite.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
