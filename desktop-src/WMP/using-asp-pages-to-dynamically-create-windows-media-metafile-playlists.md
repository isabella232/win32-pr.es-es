---
title: Usar páginas ASP para crear de forma dinámica listas de reproducción de metarchivos de Windows Media
description: Usar páginas ASP para crear de forma dinámica listas de reproducción de metarchivos de Windows Media
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Listas de reproducción de metarchivos de Windows Media, crear
- listas de reproducción de metarchivos, crear
- listas de reproducción, crear
- Listas de reproducción de metarchivos de Windows Media, creación dinámica
- listas de reproducción de metarchivos, creación dinámica
- listas de reproducción, creación dinámica
- Listas de reproducción de metarchivos de Windows Media, páginas ASP
- listas de reproducción de metarchivos, páginas ASP
- listas de reproducción, páginas ASP
- crear listas de reproducción de metarchivo de Windows Media
- creación dinámica de listas de reproducción de metarchivos de Windows Media
- páginas ASP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532073"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a>Usar páginas ASP para crear de forma dinámica listas de reproducción de metarchivos de Windows Media

Puede usar Active Server páginas (archivos ASP o. asp) para generar listas de reproducción de forma dinámica en función de la información proporcionada por los usuarios. Una página ASP es una página web dinámica que se usa junto con Microsoft Internet Information Services (IIS). ASP es un entorno en el que se pueden combinar HTML, scripts y componentes de servidor ActiveX reutilizables para crear soluciones empresariales dinámicas y eficaces basadas en Web. Las páginas ASP habilitan el scripting del lado servidor para IIS con compatibilidad nativa con Microsoft Visual Basic Scripting Edition (VBScript) y Microsoft JScript. En este debate se supone que está familiarizado con ASP y la definición de variables.

Toda la información de encabezado debe estar incluida en la primera línea de la cadena de página ASP devuelta a Windows Media Player.

Al usar páginas ASP para generar listas de reproducción, debe especificar los valores para el **ContentType** del objeto de **respuesta** y las propiedades **Expires** en la página ASP debido a problemas de latencia con Windows Media Player. El valor **Response. ContentType** debe ser una extensión de nombre de archivo válida para los metaarchivos de Windows Media. Entre los valores aceptables se incluyen WMA, Wax, WMV, WVX, ASF y ASX.

La propiedad **Response. Expires** especifica el período de tiempo, en segundos, que Windows Media Player almacena en caché el archivo de lista de reproducción. Si se especifica un valor de cero, Windows Media Player solicita una nueva lista de reproducción del servidor cada vez que el usuario actualiza la página.

Vea el SDK de la plataforma para obtener más información sobre cómo usar el objeto de **respuesta** en páginas de Active Server.

El código siguiente es un ejemplo de una página ASP que se usa para generar una lista de reproducción de metarchivo de Windows Media.


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

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> </dl>

 

 




