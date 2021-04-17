---
title: Evento Player. MediaCollectionAttributeStringRemoved
description: El evento MediaCollectionAttributeStringRemoved se produce cuando se quita un valor de atributo de la biblioteca. | Evento Player. MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Media Player MediaCollectionAttributeStringRemoved de eventos de Windows
- Evento MediaCollectionAttributeStringRemoved de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionAttributeStringRemoved
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708164"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Evento Player. MediaCollectionAttributeStringRemoved

El evento **MediaCollectionAttributeStringRemoved** se produce cuando se quita un valor de atributo de la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Cadena** que especifica el nombre del atributo. Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Cadena** que especifica el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Cuando se quita un elemento multimedia de la biblioteca, sus metadatos se quitan del objeto **MediaCollection** y este evento se desencadena para cada atributo que se ha quitado.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player. mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





