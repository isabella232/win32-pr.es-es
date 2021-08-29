---
title: IWMPPlaylist.attributeName (VB y C )
description: La propiedad attributeName (el método get attributeName en C\) obtiene el nombre de un atributo de lista de \_ reproducción especificado por un índice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist.attributeName (VB y C ) Reproductor de Windows Media
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
ms.openlocfilehash: 8b495554e4159214cbd5b1f7fa823dfeb373a11a1bfe2514d9ad07da497fa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135388"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>IWMPPlaylist.attributeName (VB y C#)

La **propiedad attributeName** (el **método get \_ attributeName** en C#) obtiene el nombre de un atributo de lista de reproducción especificado por un índice.


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

*Lindex*

**System.Int32 que** es el índice del atributo de lista de reproducción.

## <a name="return-value"></a>Valor devuelto

**System.String que** es el nombre del atributo de lista de reproducción.

## <a name="remarks"></a>Comentarios

**IWMPPlaylist.attributeName** es una propiedad de solo lectura en Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist.get \_ attributeName.**

La propiedad **IWMPPlaylist.attributeCount** devuelve el número de atributos asociados a una lista de reproducción.

El nombre devuelto por esta propiedad se puede proporcionar a los métodos **setItemInfo** o **getItemInfo** para especificar o recuperar un valor para el atributo con nombre.

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Para obtener más información sobre los atributos admitidos por Reproductor de Windows Media, vea la [Referencia de atributos](attribute-reference.md).

## <a name="examples"></a>Ejemplos

Vea la [propiedad attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obtener código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.attributeCount (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.getItemInfo (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.setItemInfo (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





