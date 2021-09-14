---
title: Personalización de la entrega multimedia
description: Personalización de la entrega multimedia
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Listas de reproducción de metarchivos multimedia, personalización de la entrega multimedia
- listas de reproducción, personalización de la entrega multimedia
- listas de reproducción de metarchivo, personalización de la entrega multimedia
- Windows Listas de reproducción de metarchivo multimedia, personalización de entrega multimedia
- listas de reproducción, personalización de entrega multimedia
- listas de reproducción de metarchivo, personalización de entrega multimedia
- personalización de entrega multimedia
- personalizar la entrega multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242499"
---
# <a name="personalizing-media-delivery"></a>Personalización de la entrega multimedia

A diferencia de la comunicación unida que difunde contenido idéntico a una audiencia masiva, Windows Media Technologies proporciona las herramientas para usar datos demográficos para individualizar las difusión. Con Internet, la comunicación bidireccional a gran escala está disponible fácilmente. Este intercambio dinámico de información permite a los proveedores de contenido conocer su audiencia y responder con presentaciones personalizadas.

En el ejemplo siguiente, con una empresa ficticia, se muestra cómo se puede personalizar la entrega de contenido de streaming. En esta explicación se supone que está familiarizado con Active Server Pages (archivos ASP o .asp) y la definición de variables.

News Network es una organización ficticia de noticias de difusión que ha ampliado sus operaciones para incluir un sitio web. La característica principal del sitio es una sección en la que los usuarios pueden crear sus propios noticies personalizados. En lugar de ver un noticiero tradicional dirigido a una audiencia masiva, un usuario ve un programa de noticias completo que solo contiene temas de interés personal. En la secuencia siguiente se describe una experiencia de usuario típica.

1.  Un nuevo usuario va al sitio y hace clic en **Crear su newscast personal.**
2.  Se abre un formulario de preferencias. En este formulario, el usuario responde a preguntas relacionadas con las preferencias personales, como noticias favoritas, noticias menos favoritas, aficiones y el método habitual de recibir noticias diarias.
3.  El usuario envía esta información y, unos segundos después, ve un noticiero personal completo de 15 minutos que contiene contenido del programa, transiciones y anuncios comerciales. La selección de cada elemento multimedia, incluidos los anuncios, se basa en el perfil de usuario y se realiza automáticamente con los componentes de Windows Media Technologies y herramientas de Internet estándar.

En la lista siguiente se describe cómo interactúan las distintas herramientas para crear un noticiero personalizado.

1.  El formulario de preferencias que el usuario rellena es Active Server Page (ASP) (Choices.asp). Dos componentes de servidor analizan los datos obtenidos del formulario de preferencias. Un componente usa la información para consultar una base de Microsoft SQL Server de noticias. El otro componente es un servidor de anuncios que usa un conjunto complejo de reglas basadas en requisitos contractuales y datos demográficos para programar anuncios adecuados para el usuario en ese momento.
2.  Las dos bases de datos devuelven partes diferentes de una lista de reproducción. La base de datos de noticias devuelve un conjunto de entradas de caso adecuadas y el servidor de anuncios devuelve un conjunto de entradas comerciales adecuadas.
3.  Una segunda página ASP (PlayShow.asp) recibe las entradas de la base de datos de noticias y el servidor de anuncios, y las combina con entradas estándar de apertura, cierre y transición. Todas las entradas se disponen según la plantilla proporcionada por PlayShow.asp y la página ASP devuelve una lista de reproducción al usuario.
4.  El control Reproductor de Windows Media integrado en el equipo del usuario reproduce la lista de reproducción de principio a fin y el usuario ve un noticiero personalizado.

El ejemplo siguiente es una parte de un archivo de lista de reproducción que un usuario podría recibir. Se le han agregado banners de anuncios, vínculos MOREINFO y RESÚMENES.


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

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




