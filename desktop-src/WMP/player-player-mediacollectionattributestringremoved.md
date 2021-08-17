---
title: Evento Player.MediaCollectionAttributeStringRemoved
description: El evento MediaCollectionAttributeStringRemoved se produce cuando se quita un valor de atributo de la biblioteca. | Evento Player.MediaCollectionAttributeStringRemoved
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Evento MediaCollectionAttributeStringRemoved Reproductor de Windows Media
- Evento MediaCollectionAttributeStringRemoved Reproductor de Windows Media clase , Player
- Clase player Reproductor de Windows Media evento , MediaCollectionAttributeStringRemoved
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
ms.openlocfilehash: 8b89e46d4dbe86f185fb636b5c8de453e2addbf83c92d1231b5f067ce0b3b1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747411"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Evento Player.MediaCollectionAttributeStringRemoved

El **evento MediaCollectionAttributeStringRemoved** tiene lugar cuando se quita un valor de atributo de la biblioteca.

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

**Cadena** que especifica el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo .](attribute-reference.md)

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Cadena** que especifica el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Cuando se quita un elemento multimedia de la biblioteca, sus metadatos se quitan del **objeto MediaCollection** y este evento se desencadena para cada atributo quitado.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

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

 

 





