---
title: Propiedad de recuento de IWMPPlaylist
description: La propiedad Count obtiene el número de elementos multimedia de una lista de reproducción.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- propiedad Count de Windows Media Player
- propiedad Count de Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, propiedad Count
topic_type:
- apiref
api_name:
- IWMPPlaylist.count
- IWMPPlaylist.get_count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d988fefc436b65652d2b0765320ca289417c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709050"
---
# <a name="iwmpplaylistcount-property"></a>IWMPPlaylist:: Count (propiedad)

La propiedad **Count** obtiene el número de elementos multimedia de una lista de reproducción.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el número de elementos multimedia de la lista de reproducción.

## <a name="remarks"></a>Observaciones

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Vea la propiedad [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para ver el código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





