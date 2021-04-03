---
description: La interfaz ID3DXSprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interfaz ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914753"
---
# <a name="id3dxsprite-interface"></a>Interfaz ID3DXSprite

La interfaz ID3DXSprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.

## <a name="members"></a>Miembros

La interfaz **ID3DXSprite** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSprite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXSprite** tiene estos métodos.



| Método                                                | Descripción                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comenzar**](id3dxsprite--begin.md)                   | Prepara un dispositivo para dibujar sprites.<br/>                                                                                                                                                                            |
| [**Dibujar**](id3dxsprite--draw.md)                     | Agrega un objeto Sprite a la lista de objetos Sprite por lotes.<br/>                                                                                                                                                                     |
| [**Fin**](id3dxsprite--end.md)                       | Llama a [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) y restaura el estado del dispositivo al modo en que se encontraba antes de que se llamara a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .<br/>                                            |
| [**Vaciar**](id3dxsprite--flush.md)                   | Obliga a que todos los sprites por lotes se envíen al dispositivo. Los Estados de los dispositivos permanecen tal como estaban después de la última llamada a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md). A continuación, se borra la lista de sprites por lotes.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Recupera el dispositivo asociado al objeto Sprite.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Obtiene la transformación de Sprite.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks. Se debe llamar a este método siempre que se pierda un dispositivo o antes de restablecer un dispositivo.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Establece la transformación de Sprite.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Establece la transformación de vista universal que se entrega a la izquierda de un objeto Sprite. Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Establece la transformación de vista mundial de la mano derecha para un Sprite. Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.<br/>                                                                                |



 

## <a name="remarks"></a>Observaciones

La interfaz **ID3DXSprite** se obtiene mediante una llamada a la función [**D3DXCreateSprite**](d3dxcreatesprite.md) .

Normalmente, la aplicación llama a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), que permite controlar el estado de representación del dispositivo, la combinación alfa y la transformación y ordenación de sprites. A continuación, para que se muestre cada Sprite, llame a [**ID3DXSprite::D RAW**](id3dxsprite--draw.md). **ID3DXSprite:** se puede llamar a:D RAW repetidamente para almacenar cualquier número de objetos Sprite. Para mostrar los sprites por lotes en el dispositivo, llame a [**ID3DXSprite:: end**](id3dxsprite--end.md) o [**ID3DXSprite:: Flush**](id3dxsprite--flush.md).

El tipo LPD3DXSPRITE se define como un puntero a la interfaz **ID3DXSprite** .


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
