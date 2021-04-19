---
title: IWMPPlaylist. attributeName (VB y C)
description: La propiedad attributeName (el \_ método get attributeName en C \) obtiene el nombre de un atributo de lista de reproducción especificado por un índice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689959"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>IWMPPlaylist. attributeName (VB y C#)

La propiedad **attributeName** (el método **Get \_ attributeName** en C#) obtiene el nombre de un atributo de lista de reproducción especificado por un índice.


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>Parámetros

*lIndex*

**System. Int32** que es el índice del atributo de la lista de reproducción.

## <a name="return-value"></a>Valor devuelto

**System. String** que es el nombre del atributo de la lista de reproducción.

## <a name="remarks"></a>Observaciones

**IWMPPlaylist. attributeName** es una propiedad de solo lectura en Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist. Get \_ attributeName** .

La propiedad **IWMPPlaylist. attributeCount** devuelve el número de atributos asociado a una lista de reproducción.

El nombre devuelto por esta propiedad se puede proporcionar a los métodos **setItemInfo** o **getItemInfo** para especificar o recuperar un valor para el atributo con nombre.

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener más información sobre los atributos compatibles con Windows Media Player, vea la [referencia de atributo](attribute-reference.md).

## <a name="examples"></a>Ejemplos

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
</dt> <dt>

[**IWMPPlaylist. attributeCount (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. getItemInfo (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





