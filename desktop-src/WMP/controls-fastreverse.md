---
title: Controls. fastReverse (método)
description: El método fastReverse inicia el examen rápido del elemento multimedia en la dirección inversa.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- método fastReverse de Windows Media Player
- método fastReverse Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método fastReverse
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
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699566"
---
# <a name="controlsfastreverse-method"></a>Controls. fastReverse (método)

El método **fastReverse** inicia el examen rápido del elemento multimedia en la dirección inversa.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método **fastReverse** recorre el clip en orden inverso cinco veces la velocidad normal, mostrando solo los fotogramas clave si se trata de un archivo de vídeo. Al invocar **fastReverse** se cambia la *configuración*. propiedad **Rate** en 5,0. Si la **velocidad** se cambia posteriormente, o si se llama a **Play** o **Stop** , Windows Media Player dejará de ser inversa rápido.

Si el elemento forma parte de una lista de reproducción, **fastReverse** se detiene al principio de la pista actual. Por ejemplo, si el seguimiento 3 está en **fastReverse**, cuando se alcanza el comienzo de la pista 3, Windows Media Player no irá al seguimiento 2. El recuento de reproducción no se incrementa al llamar a **fastReverse**.

Si llama a **fastForward** mientras **fastReverse** está en vigor, **fastReverse** se detendrá y se iniciará **fastForward** .

Este método no funciona para las difusiones en vivo y determinados tipos de medios. Para determinar si puede usar Fast Reverse en un clip, llame a **isavailable**("FastReverse").

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que usa **fastReverse** para iniciar la reproducción rápida y inversa del elemento multimedia. El objeto **Player** se creó con ID = "Player".


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



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. isAvailable**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. STOP**](controls-stop.md)
</dt> <dt>

[**Settings. rate**](settings-rate.md)
</dt> </dl>

 

 





