---
title: IWMPPlaylist count, propiedad
description: La propiedad count obtiene el número de elementos multimedia de una lista de reproducción.
ms.assetid: dbff3c86-2d42-4d47-a5cb-b8199efac728
keywords:
- recuento de propiedades Reproductor de Windows Media
- count property Reproductor de Windows Media , IWMPPlaylist (interfaz)
- Interfaz IWMPPlaylist Reproductor de Windows Media propiedad , count
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467011"
---
# <a name="iwmpplaylistcount-property"></a>IWMPPlaylist::count, propiedad

La **propiedad count** obtiene el número de elementos multimedia de una lista de reproducción.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 count {get;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el número de elementos multimedia de la lista de reproducción.

## <a name="remarks"></a>Observaciones

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Vea la [propiedad attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obtener código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





