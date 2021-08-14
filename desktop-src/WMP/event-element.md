---
title: Elemento EVENT (SDK de WMP)
description: El elemento EVENT define un comportamiento o una acción que Reproductor de Windows Media cuando recibe un comando de script etiquetado como evento.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Elemento EVENT Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9119d0c40d1e114e060c1fa2bff239c846274788f8aaa3587dc709b0bdf10ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118837831"
---
# <a name="event-element"></a>ELEMENTO EVENT

El **elemento EVENT** define un comportamiento o una acción que Reproductor de Windows Media cuando recibe un comando de script etiquetado como evento.

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>Atributos

**NAME** (obligatorio)

Nombre del evento.

**WHENDONE** (obligatorio)

Valor que define lo que Reproductor de Windows Media después de reproducir el contenido al que se hace referencia.

Los valores siguientes son posibles.



| Valor  | Descripción                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | La entrada actual (el clip interrumpido por el evento) reanuda la reproducción. Si el contenido está almacenado, se reanuda en el mismo punto donde se detuvo. si el contenido se difunde, se reanuda en la posición actual.        |
| NEXT   | El siguiente **elemento ENTRY** se reproduce como si el evento no se hubiera producido y Reproductor de Windows Media hubiera alcanzado el final del clip actual.                                                                                             |
| BREAK  | Si la entrada actual está dentro de un **bucle REPEAT,** el bucle finaliza como si se hubiera completado el recuento de repeticiones. De lo contrario, Reproductor de Windows Media salta al final de la lista de reproducción como si la entrada final se hubiera completado como de costumbre. |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                |
|-----------------|-------------------------|
| Elementos primarios | **Asx**                 |
| Elementos secundarios  | **ENTRY**, **ENTRYREF** |



 

## <a name="remarks"></a>Comentarios

Este elemento define un comportamiento o una acción que Reproductor de Windows Media cuando recibe un comando de script etiquetado como un evento. Un evento es un tipo determinado de comando de script insertado en una secuencia enviada a Reproductor de Windows Media que consta de una cadena doble. La primera cadena es la palabra "event" y la segunda cadena es el nombre del evento. El nombre del evento de la segunda cadena debe coincidir con el nombre de evento definido en el metarchivo. (La coincidencia no distingue mayúsculas de minúsculas). Los eventos se pueden enviar a Reproductor de Windows Media recibir una secuencia en tiempo real o se pueden guardar en un archivo .asf, .wma o .wmv que se entrega como una secuencia de unidifusión a petición. Cuando Reproductor de Windows Media recibe el comando de script, procesa el evento tal como lo define el **elemento EVENT.**

Este elemento define un ámbito de **elementos ENTRY** o **ENTRYREF** que se procesan siempre Reproductor de Windows Media recibe el comando de script con el evento con nombre. **ENTRYREF puede** ser una dirección URL que apunta a una página ASP. Con este elemento, puede especificar un comportamiento para el cambio de secuencia casi en tiempo real, en lugar de los cambios de secuencias previamente escritos mediante referencias a otros fragmentos de contenido o metadatos de Windows Multimedia.

Cuando se usan páginas ASP para generar listas de reproducción, debe especificar un valor para la *respuesta*. **La propiedad ContentType** y la *respuesta*. **expira la** propiedad en la página ASP debido a problemas de latencia con Reproductor de Windows Media. Respuesta . **ContentType debe** ser una extensión de nombre de archivo válida para Windows metarchivos multimedia. Los tipos válidos incluyen .asf, .asx, .wma, .wmv, .wmv y .wvx.

Consulte Platform SDK para obtener más información sobre el uso del **objeto Response** en ASP.

Este elemento puede aparecer en cualquier lugar dentro del **elemento ASX.** Si varios **elementos EVENT** dentro de un elemento **ASX** tienen valores idénticos para sus atributos **NAME,** Reproductor de Windows Media usa la primera aparición dentro del elemento **ASX** y omite todos los demás. Cuando **los elementos EVENT** tienen atributos **NAME** distintos, su orden dentro del **elemento ASX** no importa.

Reproductor de Windows Media descarta los eventos que recibe al procesar otro evento. No se admite el anidamiento de eventos. Cuando Reproductor de Windows Media está en modo de vista previa, el contenido del evento no está restringido por el **elemento PREVIEWDURATION;** la longitud completa del contenido del evento puede reproducirse incluso si la duración de la versión preliminar del elemento **ENTRY** activo expira antes del final del evento.

## <a name="examples"></a>Ejemplos

En este ejemplo, cuando Reproductor de Windows Media el comando de script EVENT y la cadena de comandos "Adlink" en el medio de streaming que está representando, busca en la lista de reproducción un evento **EVENTNAME** "Adlink". Reproductor de Windows Media cambia de la secuencia que está representando y reproduce el contenido al que se hace referencia en **EVENT**, https://example.microsoft.com/adlink.htm " ".

**El** atributo **ENTRY CLIENTSKIP** se establece en NO para evitar que se opa el clip **EVENT.** Debe reproducirse.

El script indica a Reproductor de Windows Media que reanude la reproducción del medio anterior desde el que cambió en cuanto `WHENDONE="RESUME"` adlink.asf finaliza.


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



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> <dt>

[**Reproductor de Windows Media Modelo de objetos**](windows-media-player-object-model.md)
</dt> </dl>

 

 





