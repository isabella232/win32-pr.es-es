---
title: Settings. rate
description: La propiedad Rate especifica o recupera la velocidad de reproducción actual de los medios de vídeo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Configuración. rate Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653573"
---
# <a name="settingsrate"></a>Settings. rate

La propiedad **Rate** especifica o recupera la velocidad de reproducción actual de los medios de vídeo.

## <a name="syntax"></a>Sintaxis

Player. Settings. rate

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura/escritura (**Double**) con un valor predeterminado de 1,0.

## <a name="remarks"></a>Observaciones

Esta propiedad actúa como un valor de multiplicador que permite reproducir un clip a una velocidad mayor o menor. El valor predeterminado de 1,0 indica la velocidad de creación. Tenga en cuenta que una pista de audio es difícil de comprender a las tarifas inferiores a 0,5 o superior a 1,5. Una velocidad de reproducción de 2 equivale a dos veces la velocidad de reproducción normal.

Windows Media Player intentará usar los cuatro modos de reproducción más efectivos. Estos modos son la reproducción de vídeo sin problemas con el paso de audio, la reproducción fluida de vídeo con el tono de audio no mantenido, la reproducción de vídeo suave sin audio y la reproducción de vídeo de fotogramas clave sin audio. El modo elegido por el reproductor depende de numerosos factores, como el tipo de archivo y la ubicación, el sistema operativo, la red y el servidor.

También se aplican otras consideraciones, según el tipo de medio:

-   Windows Media Format (WMV) y archivos ASF: los valores óptimos para esta propiedad son de 1 a 10, o de 1 a 10 para la reproducción inversa. Los valores de 0,5 a 1,0 o de-0,5 a-1,0 también pueden funcionar bien en los casos en los que se pueda mantener el tono de audio, por ejemplo, al reproducir archivos ubicados en el equipo local. Se permiten los valores con una magnitud absoluta mayor que 10, pero no son muy significativos.
-   Otros tipos de medios de vídeo: esta propiedad puede oscilar entre 0 y 9. No se permiten valores negativos. Los valores menores que 1 representan un movimiento lento. Los valores por encima de 9 están permitidos, pero no son muy significativos.

*Controles*. el método **fastForward** cambia el valor de **Rate** a 5,0, mientras que los *controles*. el método **fastReverse** cambia la **velocidad** a 5,0.

No se puede modificar la velocidad de reproducción de algunos tipos de medios. Utilice la *configuración*. método **isavailable** para determinar si esta propiedad se puede especificar para un elemento multimedia determinado.

**Windows Media Player 10 Mobile**: esta propiedad solo acepta o devuelve valores de-5,0, 1,0 o 5,0.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento SELECT de HTML que permite al usuario cambiar la velocidad de reproducción del medio actual. Las opciones SELECT ofrecen velocidades normales, velocidad media y velocidad de reproducción de velocidad doble. El objeto **Player** se creó con ID = "Player".


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls. fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls. fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Settings. isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





