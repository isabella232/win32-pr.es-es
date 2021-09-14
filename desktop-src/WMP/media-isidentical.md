---
title: Método Media.isIdentical
description: El método isIdentical recupera un valor que indica si el objeto proporcionado es el mismo que el actual. | Método Media.isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- Método isIdentical Reproductor de Windows Media
- Método isIdentical Reproductor de Windows Media , Clase Media
- Clase media Reproductor de Windows Media , método isIdentical
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068404"
---
# <a name="mediaisidentical-method"></a>Método Media.isIdentical

El **método isIdentical** recupera un valor que indica si el objeto proporcionado es el mismo que el actual.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*medios* \[ En\]
</dt> <dd>

**Objeto** multimedia que se compara con el objeto **Multimedia** actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano**.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **isIdentical para** comprobar si un elemento multimedia denominado newMedia es el mismo que el elemento multimedia actual. Si no son iguales, se reproduce el nuevo elemento multimedia. De lo contrario, los medios actuales se siguen reproducendo sin interrupciones. El **objeto Player** se creó con id. = "Player".


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
| Version<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> </dl>

 

 





