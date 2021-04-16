---
title: Evento Player. MediaChange
description: El evento MediaChange se produce cuando cambia un elemento multimedia. | Evento Player. MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Media Player MediaChange de eventos de Windows
- Evento MediaChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento MediaChange
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709135"
---
# <a name="playermediachange-event"></a>Evento Player. MediaChange

El evento **MediaChange** se produce cuando cambia un elemento multimedia.

## <a name="syntax"></a>Sintaxis


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Elemento* 
</dt> <dd>

Objeto **multimedia** que representa el elemento que ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa un elemento HTML DIV, denominado MEDIANAME, para mostrar el nombre del elemento multimedia actual. El código actualiza el texto en el DIV con cada aparición del evento **mediaChange** . El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





