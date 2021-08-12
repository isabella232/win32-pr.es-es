---
title: Método Controls.fastReverse
description: El método fastReverse inicia el examen rápido del elemento multimedia en la dirección inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Método fastReverse Reproductor de Windows Media
- método fastReverse Reproductor de Windows Media , clase Controls
- Controla la clase Reproductor de Windows Media , método fastReverse
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4643525f66102cbd7b017a4a48f1068489062ec0849f197f1f55df45fc6f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580281"
---
# <a name="controlsfastreverse-method"></a>Método Controls.fastReverse

El **método fastReverse** inicia el examen rápido del elemento multimedia en la dirección inversa.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **método fastReverse** examina el clip en orden inverso a una velocidad cinco veces mayor que la velocidad normal, mostrando solo los fotogramas clave si es un archivo de vídeo. La invocación **de fastReverse** cambia el *Configuración*. **propiedad** rate a 5,0. Si **posteriormente** se cambia la velocidad, o si se llama a **play** o **stop,** Reproductor de Windows Media dejará de invertirse rápidamente.

Si el elemento forma parte de una lista de reproducción, **fastReverse** se detiene al principio de la pista actual. Por ejemplo, si la pista 3 está en **fastReverse**, cuando se alcanza el principio de la pista 3, Reproductor de Windows Media irá a la pista 2. El recuento de reproducción no se incrementa al llamar **a fastReverse**.

Si llama a **fastForward mientras** **fastReverse** está en vigor, se detendrán **fastReverse** y se iniciará **fastForward.**

Este método no funciona para difusiones en directo y determinados tipos de medios. Para determinar si puede usar un inverso rápido en un clip, llame a **isAvailable**("FastReverse").

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML BUTTON que usa **fastReverse** para iniciar la reproducción inversa rápida del elemento multimedia. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls.play**](controls-play.md)
</dt> <dt>

[**Controls.stop**](controls-stop.md)
</dt> <dt>

[**Configuración.rate**](settings-rate.md)
</dt> </dl>

 

 





