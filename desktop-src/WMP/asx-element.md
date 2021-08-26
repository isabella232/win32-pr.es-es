---
title: Elemento ASX
description: El elemento ASX define un archivo como metarchivo.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Elemento ASX Reproductor de Windows Media
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 509cdbc25c57c6d0b556433c3bee8b1e68083248c8356769a31529b83c2df1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902835"
---
# <a name="asx-element"></a>Elemento ASX

El **elemento ASX** define un archivo como metarchivo.

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>Atributos

`VERSION` (obligatorio)

Número decimal que representa el número de versión de la sintaxis del metarchivo. Establezca en 3 o 3.0.

**PREVIEWMODE** (opcional)

Valor que indica si Reproductor de Windows Media entra en modo de vista previa antes de reproducir el primer clip.

Debe ser uno de los siguientes valores:



| Value | Descripción                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| SÍ   | Reproductor de Windows Media entra en modo de vista previa antes de reproducir el primer clip.                            |
| No    | Valor predeterminado. Reproductor de Windows Media no entra en modo de vista previa antes de reproducir el primer clip. |



 

**BANNERBAR** (opcional)

Valor que indica si Reproductor de Windows Media espacio para un gráfico de banner.

Debe ser uno de los siguientes valores:



| Value | Descripción                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Valor predeterminado. Reproductor de Windows Media reserva espacio para la barra de banner solo cuando un fragmento de contenido incluye uno.                       |
| FIXED | Reproductor de Windows Media reserva un espacio fijo para un gráfico de banner para cada fragmento de contenido reproducdo, independientemente de si hay un banner asociado. |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios | Ninguno. El **elemento ASX** debe ser el primer elemento de cada metarchivo.                                                                                                 |
| Elementos secundarios  | **ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE** |



 

## <a name="remarks"></a>Comentarios

Los cuatro primeros caracteres de una lista de reproducción de metarchivo deben ser "<ASX". Otros elementos definidos dentro del ámbito del elemento **ASX,** como **TITLE** y **AUTHOR**, están asociados a la información de presentación mostrada por Reproductor de Windows Media.

Por Reproductor de Windows Media, el número de versión de sintaxis es 3.0. Reproductor de Windows Media admite todas las versiones anteriores de la sintaxis de metarchivo. Los valores aceptables para **el atributo VERSION** incluyen 3.0 y 3 (sin separador decimal).

Si el valor del atributo **PREVIEWMODE** es YES, Reproductor de Windows Media entrar inmediatamente en modo de vista previa antes de reproducir el primer clip. Cuando Reproductor de Windows Media entra en modo de vista previa, se muestra una vista previa de cada clip al que se hace referencia en el metarchivo. El **elemento PREVIEWDURATION** determina la duración de cada vista previa.

El **atributo BANNERBAR** define si Reproductor de Windows Media espacio para un gráfico de banner. Un banner es un gráfico que se muestra en el área de visualización del vídeo mientras se reproduce el contenido multimedia. (Use el **elemento BANNER** para agregar un banner al contenido). Si el valor de **BANNERBAR** es FIXED, Reproductor de Windows Media espacio de banner para cada fragmento de contenido multimedia, independientemente de si el contenido multimedia tiene un banner. Si un fragmento de contenido multimedia no tiene un banner asociado, el espacio reservado para uno es negro. Si el valor del atributo **BANNERBAR** es AUTO, Reproductor de Windows Media espacio para el banner solo cuando el contenido multimedia incluye uno.

Si crea un metarchivo con varios clips (elementos **ENTRY** o **ENTRYREF)** y establece el valor del atributo **BANNERBAR** en AUTO, Reproductor de Windows Media podría cambiar de tamaño para permitir el espacio para un gráfico de banner para un clip y, a continuación, cambiar el tamaño de nuevo si el siguiente clip no contiene un gráfico de banner. Si desea que el tamaño de la ventana permanezca igual (excepto cuando cambia el tamaño del vídeo), use el valor FIXED para el **atributo BANNERBAR.**

El espacio reservado para un gráfico de banner es de 32 píxeles de alto por 194 píxeles de ancho. El espacio reservado aparece debajo de cualquier contenido de vídeo representado y 6 píxeles por encima del borde inferior del área de vídeo, lo que permite espacio para el borde del área de vídeo de 6 píxeles. El espacio reservado del banner se centra horizontalmente.

Reproductor de Windows Media representa el gráfico a partir del píxel situado más a la izquierda del espacio del banner. Si el gráfico rellena todo el espacio, aparecerá centrado horizontalmente. De lo contrario, habrá espacio final. Tenga en cuenta que el ancho mínimo de Reproductor de Windows Media es siempre más ancho que el tamaño del clip de vídeo, independientemente del valor del **atributo BANNERBAR.**

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





