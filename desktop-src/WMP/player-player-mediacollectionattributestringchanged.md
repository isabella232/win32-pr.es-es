---
title: Evento Player.MediaCollectionAttributeStringChanged
description: El evento MediaCollectionAttributeStringChanged tiene lugar cuando se cambia un valor de atributo en la biblioteca. | Evento Player.MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Evento MediaCollectionAttributeStringChanged Reproductor de Windows Media
- Evento MediaCollectionAttributeStringChanged Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070976"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Evento Player.MediaCollectionAttributeStringChanged

El **evento MediaCollectionAttributeStringChanged** tiene lugar cuando se cambia un valor de atributo en la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Cadena** que especifica el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**Cadena** que especifica el valor anterior del atributo.

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**Cadena** que especifica el nuevo valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Cuando un usuario modifica los metadatos de la biblioteca, el **objeto MediaCollection** se actualiza y este evento se produce para cada atributo cambiado.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





