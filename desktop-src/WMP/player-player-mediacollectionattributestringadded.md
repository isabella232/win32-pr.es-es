---
title: Evento Player. MediaCollectionAttributeStringAdded
description: El evento MediaCollectionAttributeStringAdded se produce cuando se agrega un valor de atributo a la biblioteca. | Evento Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Media Player MediaCollectionAttributeStringAdded de eventos de Windows
- Evento MediaCollectionAttributeStringAdded de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709134"
---
# <a name="playermediacollectionattributestringadded-event"></a>Evento Player. MediaCollectionAttributeStringAdded

El evento **MediaCollectionAttributeStringAdded** se produce cuando se agrega un valor de atributo a la biblioteca.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaCollectionAttributeStringAdded(
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

Cuando se agrega un elemento multimedia a la biblioteca, sus metadatos se agregan al objeto **MediaCollection** y este evento se desencadena para cada atributo agregado.

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

 

 





