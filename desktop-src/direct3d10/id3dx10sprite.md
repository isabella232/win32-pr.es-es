---
description: La interfaz ID3DX10Sprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D. Esta interfaz puede funcionar en un conjunto de muchos sprites.
ms.assetid: 3703f272-f631-41c0-a0d5-e7cf2d4ae145
title: Interfaz ID3DX10Sprite (D3DX10. h)
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
ms.openlocfilehash: 7b21cab26ac0929882727028775849329ac10db7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718547"
---
# <a name="id3dx10sprite-interface"></a>Interfaz ID3DX10Sprite

La interfaz ID3DX10Sprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D. Esta interfaz puede funcionar en un conjunto de muchos sprites.

## <a name="members"></a>Miembros

La interfaz **ID3DX10Sprite** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10Sprite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX10Sprite** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comenzar**](id3dx10sprite-begin.md)                                   | Preparar un dispositivo para dibujar sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md)       | Agregue una matriz de sprites al lote de sprites que se va a representar. Se debe llamar a este método entre las llamadas a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) y [**ID3DX10Sprite:: end**](id3dx10sprite-end.md), y se debe llamar a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) antes de que finalice el envío de todos los sprites por lotes al dispositivo para su representación. Este método draw es muy útil cuando se dibuja un número pequeño de sprites que se desea almacenar en el búfer en un lote grande, como las fuentes.<br/>                                                                                                                                                                              |
| [**DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md)     | Dibuja una matriz de objetos Sprite. Esto enviará inmediatamente los sprites al dispositivo para su representación, que es diferente de [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , que solo agrega una matriz de sprites a un lote de sprites que se representará cuando se llame a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) . Este método draw es muy útil cuando se dibuja un gran número de sprites que ya se han ordenado en la CPU (o no es necesario ordenarlos), como en un sistema de partículas. Se debe llamar a este método entre las llamadas a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) y [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).<br/> |
| [**Fin**](id3dx10sprite-end.md)                                       | Llame a este método después de ID3DX10Sprite:: flush. Si \_ \_ \_ se especificó el estado de guardado de Sprite de D3DX10 cuando se llamó a ID3DX10Sprite:: Begin, esta API restaurará el estado del dispositivo al modo en que se encontraba antes de que se llamara a ID3DX10Sprite:: Begin.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Vaciar**](id3dx10sprite-flush.md)                                   | Forzar el envío de todos los sprites por lotes al dispositivo. Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a ID3DX10Sprite:: Begin. A continuación, se borra la lista de sprites por lotes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**GetDevice**](id3dx10sprite-getdevice.md)                           | Recupere el dispositivo asociado al objeto Sprite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**GetProjectionTransform**](id3dx10sprite-getprojectiontransform.md) | Obtiene la matriz de proyección de Sprite que se aplica a todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetViewTransform**](id3dx10sprite-getviewtransform.md)             | Obtiene la transformación de la vista que se aplica a todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SetProjectionTransform**](id3dx10sprite-setprojectiontransform.md) | Establezca la matriz de proyección para todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**SetViewTransform**](id3dx10sprite-setviewtransform.md)             | Establezca la transformación de la vista que se aplica a todos los sprites.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Observaciones

La interfaz ID3DX10Sprite se obtiene mediante una llamada a la función [**D3DX10CreateSprite**](d3dx10createsprite.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
