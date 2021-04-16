---
title: Método media. isIdentical
description: El método isIdentical recupera un valor que indica si el objeto proporcionado es igual que el actual. | Método media. isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- método isIdentical de Windows Media Player
- método isIdentical Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método isIdentical
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699816"
---
# <a name="mediaisidentical-method"></a>Método media. isIdentical

El método **isIdentical** recupera un valor que indica si el objeto proporcionado es igual que el actual.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*medios* \[ de de\]
</dt> <dd>

Objeto **multimedia** que se va a comparar con el objeto **multimedia** actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **isIdentical** para comprobar si un elemento multimedia con el nombre newMedia es el mismo que el elemento multimedia actual. Si no son iguales, se reproduce el nuevo elemento multimedia. De lo contrario, el medio actual sigue reproduciéndose sin interrupciones. El objeto **Player** se creó con ID = "Player".


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





