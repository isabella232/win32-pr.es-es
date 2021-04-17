---
title: EVENT (elemento, WMP SDK)
description: El elemento de evento define un comportamiento o una acción realizada por Windows Media Player cuando recibe un comando de script con la etiqueta de un evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Elemento de evento Media Player de Windows
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698678"
---
# <a name="event-element"></a>Elemento EVENT

El elemento de **evento** define un comportamiento o una acción realizada por Windows Media Player cuando recibe un comando de script con la etiqueta de un evento.

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>Atributos

**Nombre** (obligatorio)

Nombre del evento.

**WHENDONE** (obligatorio)

Valor que define qué hace Windows Media Player después de reproducir el contenido al que se hace referencia.

Los valores siguientes son posibles.



| Value  | Descripción                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | La entrada actual (el clip interrumpido por el evento) se reanuda la reproducción. Si el contenido se almacena en el contenido, se reanuda en el mismo punto en el que se detuvo; Si el contenido se emite, se reanuda en la posición actual.        |
| NEXT   | El siguiente elemento de **entrada** se reproduce como si no se hubiera producido el evento y Windows Media Player había alcanzado el final del clip actual.                                                                                             |
| BREAK  | Si la entrada actual está dentro de un bucle de **repetición** , el bucle finaliza como si se hubiera completado el recuento de repeticiones. De lo contrario, Windows Media Player salta al final de la lista de reproducción como si la entrada final se hubiera completado como de costumbre. |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                |
|-----------------|-------------------------|
| Elementos primarios | **ASX**                 |
| Elementos secundarios  | **entry**, **ENTRYREF** |



 

## <a name="remarks"></a>Observaciones

Este elemento define un comportamiento o una acción realizada por Windows Media Player cuando recibe un comando de script con la etiqueta de un evento. Un evento es un tipo determinado de comando de script incrustado en una secuencia enviada a Windows Media Player que consta de una cadena doble. La primera cadena es la palabra "Event" y la segunda cadena es el nombre del evento. El nombre del evento en la segunda cadena debe coincidir con el nombre del evento definido en el metarchivo. (La coincidencia no distingue entre mayúsculas y minúsculas). Los eventos se pueden enviar a Windows Media Player recibir un flujo en tiempo real, o bien se pueden guardar en un archivo. ASF,. WMA o. wmv que se entrega como una secuencia de unidifusión a petición. Cuando Windows Media Player recibe el comando de script, procesa el evento tal y como se define en el elemento de **evento** .

Este elemento define un ámbito de elementos **entry** o **ENTRYREF** que se procesan siempre que Windows Media Player recibe el comando de script con el evento con nombre. **ENTRYREF** puede ser una dirección URL que apunta a una página ASP. Con este elemento, puede especificar un comportamiento para el cambio de flujo casi en tiempo real, en lugar de los cambios de flujo previamente creados mediante referencias a otras partes de contenido o a los metaarchivos de Windows Media.

Al usar páginas ASP para generar listas de reproducción, debe especificar un valor para la *respuesta*. Propiedad **ContentType** y la *respuesta*. propiedad **Expires** en la página ASP debido a problemas de latencia con Windows Media Player. La *respuesta*. **ContentType** debe ser una extensión de nombre de archivo válida para los metaarchivos de Windows Media. Entre los tipos válidos se incluyen. ASF,. ASX,. WMA,. Wax,. WMV y. wvx.

Vea el SDK de la plataforma para obtener más información sobre cómo usar el objeto de **respuesta** en ASP.

Este elemento puede aparecer en cualquier parte del elemento **ASX** . Si varios elementos **Event** dentro de un elemento **ASX** tienen valores idénticos para sus atributos **Name** , Windows Media Player usa la primera aparición dentro del elemento **ASX** y omite el resto. Cuando los elementos de **evento** tienen atributos de **nombre** distintos, no importa su orden dentro del elemento **ASX** .

Windows Media Player descarta los eventos que recibe mientras procesa otro evento. No se admite el anidamiento de eventos. Cuando Windows Media Player está en modo de vista previa, el contenido del evento no está restringido por el elemento **PREVIEWDURATION** ; la longitud total del contenido del evento puede reproducirse incluso si la duración de la vista previa del elemento de **entrada** activo expira antes del final del evento.

## <a name="examples"></a>Ejemplos

En este ejemplo, cuando Windows Media Player recibe el evento de comando de script y la cadena de comando "Adlink" en el medio de streaming que se está representando, busca un **EVENTNAME** "Adlink" en la lista de reproducción. Windows Media Player cambia desde el flujo que se está representando y reproduce el contenido al que se hace referencia en el **evento**, " https://example.microsoft.com/adlink.htm ".

El atributo de **entrada** **CLIENTSKIP** está establecido en no para evitar que se omita el clip de **eventos** . Debe reproducirse.

El script `WHENDONE="RESUME"` indica a Windows Media Player que reanude la reproducción del medio anterior que cambió desde el momento en que se ha finalizado Adlink. ASF.


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Modelo de objetos de Media Player de Windows**](windows-media-player-object-model.md)
</dt> </dl>

 

 





