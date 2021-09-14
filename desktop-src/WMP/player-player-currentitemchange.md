---
title: Evento Player.CurrentItemChange
description: El evento CurrentItemChange se produce cuando cambia Controls.currentItem.
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
ms.openlocfilehash: e4c425184bf4b338177ec892ed5362c085dd8cb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071002"
---
# <a name="playercurrentitemchange-event"></a>Evento Player.CurrentItemChange

El **evento CurrentItemChange** se produce cuando *controla*. **currentItem** changes.

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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls.currentItem**](controls-currentitem.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





