---
title: Evento Player.MediaChange
description: El evento MediaChange tiene lugar cuando cambia un elemento multimedia. | Evento Player.MediaChange
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Evento MediaChange Reproductor de Windows Media
- Evento MediaChange Reproductor de Windows Media clase , Player
- Clase de reproductor Reproductor de Windows Media evento , MediaChange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070978"
---
# <a name="playermediachange-event"></a>Evento Player.MediaChange

El **evento MediaChange** tiene lugar cuando cambia un elemento multimedia.

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

**Objeto** multimedia que representa el elemento que ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede tener acceso a un método de un archivo JScript importado mediante el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la inclusión en mayúsculas.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se usa un elemento DIV HTML, denominado MediaName, para mostrar el nombre del elemento multimedia actual. El código actualiza el texto de div con cada aparición del **evento mediaChange.** El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





