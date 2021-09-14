---
title: Evento Player.MediaCollectionAttributeStringAdded
description: El evento MediaCollectionAttributeStringAdded tiene lugar cuando se agrega un valor de atributo a la biblioteca. | Evento Player.MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- MediaCollectionAttributeStringAdded event Reproductor de Windows Media
- MediaCollectionAttributeStringAdded event Reproductor de Windows Media , Player class
- Clase de reproductor Reproductor de Windows Media evento , MediaCollectionAttributeStringAdded
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070977"
---
# <a name="playermediacollectionattributestringadded-event"></a>Evento Player.MediaCollectionAttributeStringAdded

El **evento MediaCollectionAttributeStringAdded** tiene lugar cuando se agrega un valor de atributo a la biblioteca.

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

**Cadena** que especifica el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Cadena** que especifica el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Cuando se agrega un elemento multimedia a la biblioteca, sus metadatos se agregan al objeto **MediaCollection** y este evento se desencadena para cada atributo agregado.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





