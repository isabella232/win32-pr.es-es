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
# <a name="personalizing-media-delivery"></a><span data-ttu-id="4ed6d-111">Personalización de la entrega de contenido multimedia</span><span class="sxs-lookup"><span data-stu-id="4ed6d-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="4ed6d-112">A diferencia de la comunicación unidireccional que difunde contenido idéntico a una audiencia masiva, las tecnologías de Windows Media le proporcionan las herramientas necesarias para usar los datos demográficos para individualizar las difusiones.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="4ed6d-113">Con Internet, la comunicación bidireccional a gran escala está disponible fácilmente.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="4ed6d-114">Este intercambio dinámico de información permite a los proveedores de contenido conocer su audiencia y responder con presentaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="4ed6d-115">En el ejemplo siguiente, con una empresa ficticia, se muestra cómo se puede personalizar la entrega de contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="4ed6d-116">En este debate se supone que está familiarizado con Active Server páginas (archivos ASP o. asp) y la definición de variables.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="4ed6d-117">News Network es una organización de noticias de difusión ficticia que ha ampliado sus operaciones para incluir un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="4ed6d-118">La característica principal del sitio es una sección en la que los usuarios pueden crear sus propios newscasts personalizados.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="4ed6d-119">En lugar de ver una newscast tradicional que está destinada a una audiencia masiva, un usuario ve un programa de noticias completo que solo contiene temas de interés personal.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="4ed6d-120">La siguiente secuencia describe una experiencia de usuario típica.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="4ed6d-121">Un nuevo usuario va al sitio y hace clic en **crear su newscast personal**.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="4ed6d-122">Se abre un formulario de preferencias.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-122">A preference form opens.</span></span> <span data-ttu-id="4ed6d-123">En este formulario, el usuario responde preguntas relacionadas con las preferencias personales, como historias de noticias favoritas, menos historias de noticias favoritas, aficiones y el método habitual de recibir noticias diarias.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="4ed6d-124">El usuario envía esta información y unos segundos más tarde ve un newscast personal completo, de 15 minutos, que contiene el contenido del programa, las transiciones y los comerciales.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="4ed6d-125">La selección de cada elemento multimedia, incluidos los comerciales, se basa en el perfil de usuario y se realiza de forma automática con los componentes de las tecnologías de Windows Media y las herramientas de Internet estándar.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="4ed6d-126">En la siguiente lista se describe cómo interactúan las diversas herramientas para crear un newscast personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="4ed6d-127">El formulario de preferencias que el usuario rellena es una página de Active Server (ASP) (Choices. asp).</span><span class="sxs-lookup"><span data-stu-id="4ed6d-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="4ed6d-128">Dos componentes de servidor analizan los datos obtenidos del formulario de preferencias.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="4ed6d-129">Un componente utiliza la información para consultar una base de datos Microsoft SQL Server de historias de noticias.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="4ed6d-130">El otro componente es un servidor de ad que utiliza un conjunto complejo de reglas basadas en los requisitos contractuales y los datos demográficos para programar anuncios adecuados para el usuario en ese momento.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="4ed6d-131">Las dos bases de datos devuelven distintas partes de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="4ed6d-132">La base de datos de casos de noticias devuelve un conjunto de entradas de historias adecuadas y el servidor de ad devuelve un conjunto de entradas comerciales adecuadas.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="4ed6d-133">Una segunda página ASP (PlayShow. asp) recibe las entradas de la base de datos de noticias y el servidor de anuncios, y las combina con las entradas estándar de abrir, cerrar y transición.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="4ed6d-134">A continuación, todas las entradas se colocan según la plantilla proporcionada por PlayShow. asp y la página ASP devuelve al usuario una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="4ed6d-135">El control Embedded Windows Media Player en el equipo del usuario reproduce la lista de reproducción de principio a fin y el usuario ve un newscast personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="4ed6d-136">El ejemplo siguiente es una parte de un archivo de lista de reproducción que un usuario podría recibir.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="4ed6d-137">Se han agregado a ella titulares de anuncios, vínculos de MOREINFO y resúmenes.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


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



-   <span data-ttu-id="4ed6d-138">Las empresas, las organizaciones, los productos, las personas y los eventos usados en los ejemplos son ficticios.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="4ed6d-139">No se entenderá o deducirá ninguna asociación con ninguna empresa, organización, producto, persona o acontecimiento reales.</span><span class="sxs-lookup"><span data-stu-id="4ed6d-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ed6d-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ed6d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ed6d-141">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="4ed6d-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4ed6d-142">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="4ed6d-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4ed6d-143">**Usar listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="4ed6d-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="4ed6d-144">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4ed6d-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4ed6d-145">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4ed6d-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




