---
title: Elemento BANNER
description: El elemento BANNER define una dirección URL a un archivo gráfico que aparecerá en el panel de presentación.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento BANNER Reproductor de Windows Media
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91b3de50c1360337c1344a1af1a0696361614dbc293390470e7c196e53528a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135968"
---
# <a name="banner-element"></a>Elemento BANNER

El **elemento BANNER** define una dirección URL a un archivo gráfico que aparecerá en el panel de presentación.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Dirección URL a un archivo gráfico que se muestra en el panel de presentación.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                   |
|-----------------|----------------------------|
| Elementos primarios | **ASX**, **ENTRY**         |
| Elementos secundarios  | **ABSTRACT**, **MOREINFO** |



 

## <a name="remarks"></a>Comentarios

Este elemento define una dirección URL a un archivo gráfico que aparece en el panel Reproductor de Windows Media pantalla, debajo del contenido del vídeo. Si el medio es solo audio, el gráfico del banner se muestra por sí solo. Reproductor de Windows Media reserva un espacio de 32 píxeles de alto por 194 píxeles de ancho (la barra de banner) para el gráfico. Si el gráfico definido en la dirección URL es menor que ese, se muestra en su tamaño original. Si el gráfico es mayor que el espacio reservado, Reproductor de Windows Media recortará la imagen para ajustarla al espacio.

Puede usar un elemento **ABSTRACT dentro** del ámbito del elemento **BANNER** para mostrar texto como información sobre herramientas cuando el usuario pausa el puntero del mouse sobre el gráfico del banner. Un **elemento MOREINFO** dentro de un **elemento BANNER** define una dirección URL a la que se toma el usuario cuando el usuario hace clic en el gráfico del banner. (La dirección URL puede ser cualquier ruta de acceso o protocolo, como un vínculo de correo electrónico, una dirección URL del Protocolo de transferencia de hipertexto (HTTP) a un sitio web o incluso un comando JScript Microsoft). Cuando el puntero se mueve sobre el gráfico, el gráfico se vuelve relieve y tiene el aspecto de un botón.

Se muestra un elemento **BANNER** definido para un **elemento ASX** mientras se reproducen todos los clips de la lista de reproducción. Un **elemento BANNER** definido en un elemento **ENTRY** solo se muestra mientras se reproduce ese clip y, durante ese tiempo, invalida cualquier banner definido dentro del elemento **ASX** primario. Puede especificar cómo se Reproductor de Windows Media espacio para el banner estableciendo el atributo **BANNERBAR** del **elemento ASX.**

Las imágenes de banner no se admiten con archivos DRM o cuando Reproductor de Windows Media está insertado en una página web.

## <a name="examples"></a>Ejemplos

A continuación se muestra un ejemplo de un **elemento BANNER** sin elementos secundarios:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



A continuación se muestra un ejemplo de **un elemento BANNER** que contiene elementos **ABSTRACT** **y MOREINFO.**


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





