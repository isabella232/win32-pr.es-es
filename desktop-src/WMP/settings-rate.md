---
title: Configuración.rate
description: La propiedad rate especifica o recupera la velocidad de reproducción actual de los medios de vídeo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Configuración.rate Reproductor de Windows Media
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
ms.openlocfilehash: 01936462593b8b27a8d45f2e3e4090b9cf242d79e1d9b1c2cda00c152bd41182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646405"
---
# <a name="settingsrate"></a>Configuración.rate

La **propiedad rate** especifica o recupera la velocidad de reproducción actual de los medios de vídeo.

## <a name="syntax"></a>Syntax

player.settings.rate

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de **lectura** y escritura (**double**) con un valor predeterminado de 1,0.

## <a name="remarks"></a>Comentarios

Esta propiedad actúa como un valor multiplicador que permite reproducir un clip a una velocidad más rápida o más lenta. El valor predeterminado de 1,0 indica la velocidad de creación. Tenga en cuenta que una pista de audio resulta difícil de entender a velocidades inferiores a 0,5 o superiores a 1,5. Una velocidad de reproducción de 2 equivale al doble de la velocidad de reproducción normal.

Reproductor de Windows Media intentará usar los cuatro modos de reproducción diferentes más efectivos. Estos modos son una reproducción de vídeo fluida con un tono de audio mantenido, una reproducción de vídeo fluida con un tono de audio no mantenido, una reproducción de vídeo fluida sin audio y una reproducción de vídeo con fotogramas clave sin audio. El modo elegido por el reproductor depende de numerosos factores, como el tipo de archivo y la ubicación, el sistema operativo, la red y el servidor.

También se aplican otras consideraciones, en función del tipo de medio:

-   Windows Archivos DE FORMATO MULTIMEDIA (WMV) y ASF: los valores óptimos para esta propiedad van de 1 a 10 o de 1 a 10 para el juego inverso. Los valores de 0,5 a 1,0 o de -0,5 a -1,0 también pueden funcionar bien en los casos en los que se puede mantener el tono de audio, por ejemplo, al reproducir archivos ubicados en el equipo local. Se permiten valores con una magnitud absoluta mayor que 10, pero no son muy significativos.
-   Otros tipos de medios de vídeo: esta propiedad puede oscilar entre 0 y 9. No se permiten valores negativos. Los valores menores que 1 representan el movimiento lento. Se permiten valores por encima de 9, pero no son muy significativos.

Controles . **El método fastForward** cambia el valor de **rate** a 5,0, mientras que *el control .* **El método fastReverse** **cambia la velocidad** a 5,0.

No se puede modificar la velocidad de reproducción de algunos tipos de medios. Use el *Configuración*. **Método isAvailable** para determinar si esta propiedad se puede especificar para un elemento multimedia determinado.

**Reproductor de Windows Media 10 Mobile:** esta propiedad solo acepta o devuelve valores de -5.0, 1.0 o 5.0.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento SELECT HTML que permite al usuario cambiar la velocidad de reproducción del medio actual. Las opciones SELECT ofrecen velocidad normal, velocidad media y velocidad doble de reproducción. El **objeto Player** se creó con id. = "Player".


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



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Controls.fastForward**](controls-fastforward.md)
</dt> <dt>

[**Controls.fastReverse**](controls-fastreverse.md)
</dt> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> <dt>

[**Configuración.isAvailable**](settings-isavailable.md)
</dt> </dl>

 

 





