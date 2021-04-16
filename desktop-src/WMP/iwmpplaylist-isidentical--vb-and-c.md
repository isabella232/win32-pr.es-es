---
title: IWMPPlaylist. isIdentical (VB y C)
description: La propiedad isIdentical (el \_ método get isIdentical de C \) obtiene un valor que indica si la lista de reproducción especificada es idéntica a la lista de reproducción actual.
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist. isIdentical (VB y C) Windows Media Player
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
ms.openlocfilehash: bee30441e8f0275bba06f71a01095c39da8eae9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690038"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist. isIdentical (VB y C#)

La propiedad **isIdentical** (el método **Get \_ isIdentical** en C#) obtiene un valor que indica si la lista de reproducción especificada es idéntica a la lista de reproducción actual.


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

Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción que este método compara con la lista de reproducción actual.

## <a name="property-value"></a>Valor de propiedad

Un **valor de tipo System. Boolean** que indica si las listas de reproducción comparadas son idénticas.

## <a name="remarks"></a>Observaciones

**IWMPPlaylist. isIdentical** es una propiedad de Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist. Get \_ isIdentical** .

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

 

 





