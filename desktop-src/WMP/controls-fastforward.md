---
title: Método Controls.fastForward
description: El método fastForward inicia la reproducción rápida del elemento multimedia en la dirección hacia delante. | Método Controls.fastForward
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Método fastForward Reproductor de Windows Media
- Método fastForward Reproductor de Windows Media , Clase Controls
- Controla la clase Reproductor de Windows Media método , fastForward
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20d033b8b025955e57a9c3ebed00a6d7a92a666e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967703"
---
# <a name="controlsfastforward-method"></a>Método Controls.fastForward

El **método fastForward** inicia la reproducción rápida del elemento multimedia en la dirección hacia delante.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método fastForward** reproduce el clip a una velocidad cinco veces mayor que la normal. La invocación **de fastForward** cambia el *Configuración*. **propiedad** rate a 5,0. Si **posteriormente** se cambia la velocidad, o si se llama a **play** o **stop,** Reproductor de Windows Media el reenvío rápido.

El **método fastForward** no funciona para difusiones en directo y determinados tipos de medios. Para determinar si puede avanzar rápidamente en un clip, llame a **isAvailable**("FastForward").

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que usa **fastForward** para iniciar la reproducción rápida del elemento multimedia. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Configuración.rate**](settings-rate.md)
</dt> </dl>

 

 





