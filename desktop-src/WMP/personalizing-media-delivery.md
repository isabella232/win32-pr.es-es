---
title: Personalización de la entrega de contenido multimedia
description: Personalización de la entrega de contenido multimedia
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Listas de reproducción de metarchivos de Windows Media, personalizar la entrega de contenido multimedia
- listas de reproducción, personalización de la entrega de contenido multimedia
- listas de reproducción de metarchivos, personalización de la entrega de contenido multimedia
- Listas de reproducción de metarchivos de Windows Media, personalización de entrega multimedia
- listas de reproducción, personalización de entrega multimedia
- listas de reproducción de metarchivos, personalización de entrega de medios
- Personalización de la entrega multimedia
- Personalización de la entrega de contenido multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268363"
---
# <a name="personalizing-media-delivery"></a>Personalización de la entrega de contenido multimedia

A diferencia de la comunicación unidireccional que difunde contenido idéntico a una audiencia masiva, las tecnologías de Windows Media le proporcionan las herramientas necesarias para usar los datos demográficos para individualizar las difusiones. Con Internet, la comunicación bidireccional a gran escala está disponible fácilmente. Este intercambio dinámico de información permite a los proveedores de contenido conocer su audiencia y responder con presentaciones personalizadas.

En el ejemplo siguiente, con una empresa ficticia, se muestra cómo se puede personalizar la entrega de contenido de streaming. En este debate se supone que está familiarizado con Active Server páginas (archivos ASP o. asp) y la definición de variables.

News Network es una organización de noticias de difusión ficticia que ha ampliado sus operaciones para incluir un sitio Web. La característica principal del sitio es una sección en la que los usuarios pueden crear sus propios newscasts personalizados. En lugar de ver una newscast tradicional que está destinada a una audiencia masiva, un usuario ve un programa de noticias completo que solo contiene temas de interés personal. La siguiente secuencia describe una experiencia de usuario típica.

1.  Un nuevo usuario va al sitio y hace clic en **crear su newscast personal**.
2.  Se abre un formulario de preferencias. En este formulario, el usuario responde preguntas relacionadas con las preferencias personales, como historias de noticias favoritas, menos historias de noticias favoritas, aficiones y el método habitual de recibir noticias diarias.
3.  El usuario envía esta información y unos segundos más tarde ve un newscast personal completo, de 15 minutos, que contiene el contenido del programa, las transiciones y los comerciales. La selección de cada elemento multimedia, incluidos los comerciales, se basa en el perfil de usuario y se realiza de forma automática con los componentes de las tecnologías de Windows Media y las herramientas de Internet estándar.

En la siguiente lista se describe cómo interactúan las diversas herramientas para crear un newscast personalizado.

1.  El formulario de preferencias que el usuario rellena es una página de Active Server (ASP) (Choices. asp). Dos componentes de servidor analizan los datos obtenidos del formulario de preferencias. Un componente utiliza la información para consultar una base de datos Microsoft SQL Server de historias de noticias. El otro componente es un servidor de ad que utiliza un conjunto complejo de reglas basadas en los requisitos contractuales y los datos demográficos para programar anuncios adecuados para el usuario en ese momento.
2.  Las dos bases de datos devuelven distintas partes de una lista de reproducción. La base de datos de casos de noticias devuelve un conjunto de entradas de historias adecuadas y el servidor de ad devuelve un conjunto de entradas comerciales adecuadas.
3.  Una segunda página ASP (PlayShow. asp) recibe las entradas de la base de datos de noticias y el servidor de anuncios, y las combina con las entradas estándar de abrir, cerrar y transición. A continuación, todas las entradas se colocan según la plantilla proporcionada por PlayShow. asp y la página ASP devuelve al usuario una lista de reproducción.
4.  El control Embedded Windows Media Player en el equipo del usuario reproduce la lista de reproducción de principio a fin y el usuario ve un newscast personalizado.

El ejemplo siguiente es una parte de un archivo de lista de reproducción que un usuario podría recibir. Se han agregado a ella titulares de anuncios, vínculos de MOREINFO y resúmenes.


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   Las empresas, las organizaciones, los productos, las personas y los eventos usados en los ejemplos son ficticios. No se entenderá o deducirá ninguna asociación con ninguna empresa, organización, producto, persona o acontecimiento reales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




