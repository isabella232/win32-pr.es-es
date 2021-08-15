---
title: Evento Player.CurrentItemChange
description: El evento CurrentItemChange tiene lugar cuando cambia Controls.currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- Evento CurrentItemChange Reproductor de Windows Media
- Evento CurrentItemChange Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , CurrentItemChange
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed0ca3c8333c7261c8332bcc124c905c5540f5cdf0dbefe3f34f121eb901cc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338131"
---
# <a name="playercurrentitemchange-event"></a>Evento Player.CurrentItemChange

El **evento CurrentItemChange** tiene lugar cuando *controla*. **currentItem** changes.

## <a name="syntax"></a>Sintaxis


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="examples"></a>Ejemplos

En el JScript siguiente se muestra un controlador de eventos para el *reproductor*. **evento currentItemChange.** El **objeto Player** se creó con id. = "Player".


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





