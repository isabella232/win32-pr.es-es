---
title: Elemento BANNER
description: El elemento BANNER define una dirección URL a un archivo gráfico que aparecerá en el panel de información.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Elemento de pancarta Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700009"
---
# <a name="banner-element"></a>Elemento BANNER

El elemento **banner** define una dirección URL a un archivo gráfico que aparecerá en el panel de información.

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Dirección URL de un archivo gráfico que se muestra en el panel de información.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                   |
|-----------------|----------------------------|
| Elementos primarios | **ASX**, **entrada**         |
| Elementos secundarios  | **abstract**, **MOREINFO** |



 

## <a name="remarks"></a>Observaciones

Este elemento define una dirección URL a un archivo gráfico que aparece en el panel de información de Media Player de Windows, debajo del contenido del vídeo. Si el medio es solo audio, el gráfico de banner se muestra por sí mismo. Windows Media Player reserva un espacio de 32 píxeles de alto por 194 píxeles de ancho (la barra de pancarta) para el gráfico. Si el gráfico definido en la dirección URL es menor que ese, se muestra en su tamaño original. Si el gráfico es mayor que el espacio reservado, Windows Media Player recortará la imagen para que quepa en el espacio.

Puede usar un elemento **abstracto** dentro del ámbito del elemento **banner** para mostrar texto como información sobre herramientas cuando el usuario detiene el puntero del mouse sobre el gráfico del banner. Un elemento **MOREINFO** dentro de un elemento **banner** define una dirección URL a la que se realiza el usuario cuando el usuario hace clic en el gráfico de banner. (La dirección URL puede ser cualquier ruta de acceso o protocolo, como un vínculo de correo electrónico, una dirección URL del Protocolo de transferencia de hipertexto (HTTP) a un sitio web o incluso un comando de Microsoft JScript). Cuando el puntero se mueve sobre el gráfico, el gráfico se vuelve a relieve y tiene el aspecto de un botón.

Un elemento **banner** definido para un elemento **ASX** se muestra mientras se reproducen todos los clips de la lista de reproducción. Un elemento **banner** definido en un elemento **entry** solo se muestra mientras se reproduce el clip y, durante ese tiempo, reemplaza cualquier banner definido en el elemento **ASX** primario. Puede especificar cómo reserva Windows Media Player el espacio para el banner estableciendo el atributo **BANNERBAR** del elemento **ASX** .

Las imágenes de banner no son compatibles con los archivos DRM o cuando Windows Media Player está incrustado en una página web.

## <a name="examples"></a>Ejemplos

El siguiente es un ejemplo de un elemento **banner** sin elementos secundarios:


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



A continuación se incluye un ejemplo de un elemento **banner** que contiene elementos **abstractos** y **MOREINFO** .


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





