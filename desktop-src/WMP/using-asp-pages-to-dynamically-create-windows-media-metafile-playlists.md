---
title: Usar asp pages para crear dinámicamente listas de Windows de metarchivo multimedia
description: Usar asp pages para crear dinámicamente listas de Windows de metarchivo multimedia
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Listas de reproducción de metarchivos multimedia, creación
- listas de reproducción de metarchivo, crear
- listas de reproducción, crear
- Windows Listas de reproducción de metarchivos multimedia, creación dinámica
- listas de reproducción de metarchivo, creación dinámica
- listas de reproducción, creación dinámica
- Windows Listas de reproducción de metarchivos multimedia, páginas ASP
- listas de reproducción de metarchivo, páginas ASP
- listas de reproducción, páginas ASP
- crear listas Windows de metarchivo multimedia
- crear dinámicamente listas Windows de metarchivo multimedia
- páginas ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568204"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Usar asp pages para crear dinámicamente listas de Windows de metarchivo multimedia

Puede usar Active Server Pages (archivos ASP o .asp) para generar dinámicamente listas de reproducción basadas en la información proporcionada por los usuarios. Una página ASP es una página web dinámica que se usa junto con Microsoft Internet Information Services (IIS). ASP es un entorno en el que puede combinar HTML, scripts y componentes de servidor ActiveX reutilizables para crear soluciones empresariales dinámicas y eficaces basadas en web. Las páginas ASP habilitan el scripting del lado servidor para IIS con compatibilidad nativa con Microsoft Visual Basic Scripting Edition (VBScript) y Microsoft JScript. En esta explicación se da por supuesto que está familiarizado con ASP y que define variables.

Toda la información de encabezado debe estar contenida en la primera línea de la cadena de página ASP devuelta a Reproductor de Windows Media.

Cuando se usan páginas ASP para generar listas  de reproducción, debe  especificar valores para **contentType** del objeto Response y expiran las propiedades de la página ASP debido a problemas de latencia con Reproductor de Windows Media. El **valor Response.ContentType** debe ser una extensión de nombre de archivo válida para Windows metarchivos multimedia. Los valores aceptables incluyen wma, wma, wmv, wvx, asf y asx.

La **propiedad Response.expires** especifica el tiempo, en segundos, que Reproductor de Windows Media almacena en caché el archivo de lista de reproducción. Si se especifica un valor de cero, Reproductor de Windows Media solicitar una nueva lista de reproducción del servidor cada vez que el usuario actualiza la página.

Consulte Platform SDK para obtener más información sobre el uso del **objeto Response** en Active Server Pages.

El código siguiente es un ejemplo de una página ASP que se usa para generar una lista de reproducción Windows metarchivo multimedia.


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> </dl>

 

 




