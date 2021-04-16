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
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a><span data-ttu-id="83671-115">Usar páginas ASP para crear de forma dinámica listas de reproducción de metarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="83671-115">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>

<span data-ttu-id="83671-116">Puede usar Active Server páginas (archivos ASP o. asp) para generar listas de reproducción de forma dinámica en función de la información proporcionada por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="83671-116">You can use Active Server Pages (ASP, or .asp files) to dynamically generate playlists based on information provided by users.</span></span> <span data-ttu-id="83671-117">Una página ASP es una página web dinámica que se usa junto con Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="83671-117">An ASP page is a dynamic webpage used in conjunction with Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="83671-118">ASP es un entorno en el que se pueden combinar HTML, scripts y componentes de servidor ActiveX reutilizables para crear soluciones empresariales dinámicas y eficaces basadas en Web.</span><span class="sxs-lookup"><span data-stu-id="83671-118">ASP is an environment in which you can combine HTML, scripts, and reusable ActiveX server components to create dynamic and powerful Web-based business solutions.</span></span> <span data-ttu-id="83671-119">Las páginas ASP habilitan el scripting del lado servidor para IIS con compatibilidad nativa con Microsoft Visual Basic Scripting Edition (VBScript) y Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="83671-119">ASP pages enable server-side scripting for IIS with native support for both Microsoft Visual Basic Scripting Edition (VBScript) and Microsoft JScript.</span></span> <span data-ttu-id="83671-120">En este debate se supone que está familiarizado con ASP y la definición de variables.</span><span class="sxs-lookup"><span data-stu-id="83671-120">This discussion assumes that you are familiar with ASP and defining variables.</span></span>

<span data-ttu-id="83671-121">Toda la información de encabezado debe estar incluida en la primera línea de la cadena de página ASP devuelta a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="83671-121">All header information must be contained on the first line of the ASP page string returned to Windows Media Player.</span></span>

<span data-ttu-id="83671-122">Al usar páginas ASP para generar listas de reproducción, debe especificar los valores para el **ContentType** del objeto de **respuesta** y las propiedades **Expires** en la página ASP debido a problemas de latencia con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="83671-122">When you use ASP pages to generate playlists, you must specify values for the **Response** object's **ContentType** and **expires** properties in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="83671-123">El valor **Response. ContentType** debe ser una extensión de nombre de archivo válida para los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83671-123">The **Response.ContentType** value must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="83671-124">Entre los valores aceptables se incluyen WMA, Wax, WMV, WVX, ASF y ASX.</span><span class="sxs-lookup"><span data-stu-id="83671-124">Acceptable values include wma, wax, wmv, wvx, asf, and asx.</span></span>

<span data-ttu-id="83671-125">La propiedad **Response. Expires** especifica el período de tiempo, en segundos, que Windows Media Player almacena en caché el archivo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="83671-125">The **Response.expires** property specifies the length of time, in seconds, that Windows Media Player caches the playlist file.</span></span> <span data-ttu-id="83671-126">Si se especifica un valor de cero, Windows Media Player solicita una nueva lista de reproducción del servidor cada vez que el usuario actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="83671-126">Specifying a value of zero results in Windows Media Player requesting a new playlist from the server each time the user refreshes the page.</span></span>

<span data-ttu-id="83671-127">Vea el SDK de la plataforma para obtener más información sobre cómo usar el objeto de **respuesta** en páginas de Active Server.</span><span class="sxs-lookup"><span data-stu-id="83671-127">See the Platform SDK for details about using the **Response** object in Active Server Pages.</span></span>

<span data-ttu-id="83671-128">El código siguiente es un ejemplo de una página ASP que se usa para generar una lista de reproducción de metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83671-128">The following code is an example of an ASP page used to generate a Windows Media metafile playlist.</span></span>


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="83671-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83671-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83671-130">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="83671-130">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




