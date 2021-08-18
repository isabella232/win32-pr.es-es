---
title: IWMPPlaylist.isIdentical (VB y C)
description: La propiedad isIdentical (el método get isIdentical en C\) obtiene un valor que indica si la lista de reproducción especificada es idéntica a la \_ lista de reproducción actual.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist.isIdentical (VB y C ) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca62b1667250b049cf47e797d59bdddea0444c6ea8803ca0fc8daf526289eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119030"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist.isIdentical (VB y C#)

La **propiedad isIdentical** (el método **get \_ isIdentical** en C#) obtiene un valor que indica si la lista de reproducción especificada es idéntica a la lista de reproducción actual.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a>Parámetros

*pIWMPPlaylist*

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción que este método compara con la lista de reproducción actual.

## <a name="property-value"></a>Valor de propiedad

**System.Boolean que** indica si las listas de reproducción comparadas son idénticas.

## <a name="remarks"></a>Comentarios

**IWMPPlaylist.isIdentical** es una propiedad de Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist.get \_ isIdentical.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





