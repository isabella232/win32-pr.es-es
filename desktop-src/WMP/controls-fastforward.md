---
title: Controls. fastForward (método)
description: El método fastForward inicia la reproducción rápida del elemento multimedia en la dirección de avance. | Controls. fastForward (método)
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- método fastForward de Windows Media Player
- método fastForward Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método fastForward
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699567"
---
# <a name="controlsfastforward-method"></a>Controls. fastForward (método)

El método **fastForward** inicia la reproducción rápida del elemento multimedia en la dirección de avance.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **fastForward** vuelve a reproducir el clip cinco veces la velocidad normal. Al invocar **fastForward** se cambia la *configuración*. propiedad **Rate** en 5,0. Si la **velocidad** se cambia posteriormente, o si se llama a **Play** o **Stop** , Windows Media Player dejará de reenviarse rápidamente.

El método **fastForward** no funciona para las difusiones en vivo y determinados tipos de medios. Para determinar si puede avanzar rápidamente en un clip, llame a **isavailable**("Fastforward").

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que usa **fastForward** para iniciar la reproducción rápida del elemento multimedia. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls. isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. STOP**](controls-stop.md)
</dt> <dt>

[**Settings. rate**](settings-rate.md)
</dt> </dl>

 

 





