---
description: La interfaz ID3DXSprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interfaz ID3DXSprite (D3dx9core.h)
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
ms.openlocfilehash: 7d5786096fb9c38188d73d613fd11efd97c2401e9f8ae9c7eb4a05dfe1dc1e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729251"
---
# <a name="id3dxsprite-interface"></a>Interfaz ID3DXSprite

La interfaz ID3DXSprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.

## <a name="members"></a>Miembros

La **interfaz ID3DXSprite** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXSprite** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXSprite** tiene estos métodos.



| Método                                                | Descripción                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comenzar**](id3dxsprite--begin.md)                   | Prepara un dispositivo para dibujar sprites.<br/>                                                                                                                                                                            |
| [**Dibujar**](id3dxsprite--draw.md)                     | Agrega un sprite a la lista de sprites por lotes.<br/>                                                                                                                                                                     |
| [**End**](id3dxsprite--end.md)                       | Llama [**a ID3DXSprite::Flush**](id3dxsprite--flush.md) y restaura el estado del dispositivo a como estaba antes de llamar a [**ID3DXSprite::Begin.**](id3dxsprite--begin.md)<br/>                                            |
| [**Vaciar**](id3dxsprite--flush.md)                   | Obliga a que todos los sprites por lotes se envían al dispositivo. Los estados del dispositivo permanecen como estaban después de la última llamada a [**ID3DXSprite::Begin**](id3dxsprite--begin.md). A continuación, se borra la lista de sprites por lotes.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Recupera el dispositivo asociado al objeto sprite.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Obtiene la transformación sprite.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Use este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los bloques de estado. Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Use este método para volver a adquirir recursos y guardar el estado inicial.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Establece la transformación de sprite.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Establece la transformación de la vista del mundo de la izquierda para un sprite. Se requiere una llamada a este método antes de agrupar u ordenar sprites.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Establece la transformación de la vista del mundo de la mano derecha para un sprite. Se requiere una llamada a este método antes de agrupar u ordenar sprites.<br/>                                                                                |



 

## <a name="remarks"></a>Comentarios

La **interfaz ID3DXSprite** se obtiene mediante una llamada a la función [**D3DXCreateSprite.**](d3dxcreatesprite.md)

Normalmente, la aplicación llama primero a [**ID3DXSprite::Begin,**](id3dxsprite--begin.md)lo que permite controlar el estado de representación del dispositivo, la mezcla alfa y la transformación y ordenación de sprites. A continuación, para que se muestre cada sprite, llame [**a ID3DXSprite::D raw**](id3dxsprite--draw.md). Se puede llamar a **ID3DXSprite::D raw** repetidamente para almacenar cualquier número de sprites. Para mostrar los sprites por lotes en el dispositivo, llame a [**ID3DXSprite::End**](id3dxsprite--end.md) o [**ID3DXSprite::Flush**](id3dxsprite--flush.md).

El tipo LPD3DXSPRITE se define como un puntero a la **interfaz ID3DXSprite.**


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
