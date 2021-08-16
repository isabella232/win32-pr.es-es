---
title: Método Controls.fastForward
description: El método fastForward inicia la reproducción rápida del elemento multimedia en la dirección hacia delante. | Controls.fastForward (método)
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- Método fastForward Reproductor de Windows Media
- Método fastForward Reproductor de Windows Media , clase Controls
- Clase Controls Reproductor de Windows Media , método fastForward
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
ms.openlocfilehash: a8b35c2a31c26259a12638d09c968b90ea42f93c692bf4c24af9dc987a6df3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341821"
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

## <a name="remarks"></a>Comentarios

El **método fastForward** reproduce el clip cinco veces la velocidad normal. La invocación **de fastForward** cambia el *Configuración*. **propiedad** rate a 5,0. Si **posteriormente** se cambia la velocidad, o si se llama a **play** o **stop,** Reproductor de Windows Media el reenvío rápido.

El **método fastForward** no funciona para difusión en vivo y determinados tipos de medios. Para determinar si puede avanzar rápidamente en un clip, llame a **isAvailable**("FastForward").

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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Configuración.rate**](settings-rate.md)
</dt> </dl>

 

 





