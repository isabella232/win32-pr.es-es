---
title: Usar vínculos relativos en los metaarchivos
description: Usar vínculos relativos en los metaarchivos
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Listas de reproducción de metarchivos de Windows Media, vínculos relativos
- listas de reproducción, vínculos relativos
- listas de reproducción de metarchivos, vínculos relativos
- metaarchivos, vínculos relativos
- Metaarchivos de Windows Media, vínculos relativos
- vínculos relativos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903323"
---
# <a name="using-relative-links-in-metafiles"></a><span data-ttu-id="ab897-109">Usar vínculos relativos en los metaarchivos</span><span class="sxs-lookup"><span data-stu-id="ab897-109">Using Relative Links in Metafiles</span></span>

<span data-ttu-id="ab897-110">Los vínculos relativos son una característica totalmente compatible de los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ab897-110">Relative links are a fully supported feature of Windows Media metafiles.</span></span> <span data-ttu-id="ab897-111">Puede usar vínculos relativos en los metaarchivos de forma muy parecida a como se usan en documentos HTML.</span><span class="sxs-lookup"><span data-stu-id="ab897-111">You can use relative links in metafiles much like you use them in HTML documents.</span></span> <span data-ttu-id="ab897-112">El uso de vínculos relativos le permite crear metarchivos que son portátiles, lo que significa que puede copiar o mover una estructura de directorios completa a otro servidor sin actualizar las rutas de acceso a los archivos de gráficos usados como pancartas o los atributos **href** de los elementos **MOREINFO** (si hacen referencia a archivos en el mismo servidor Web que el metarchivo almacenado).</span><span class="sxs-lookup"><span data-stu-id="ab897-112">The use of relative links enables you to create metafiles that are portable, meaning you can copy or move an entire directory structure to another server without updating the paths to graphic files used as banners or the **HREF** attributes of **MOREINFO** elements (if they reference files on the same web server as the stored metafile).</span></span> <span data-ttu-id="ab897-113">Los vínculos relativos funcionan, en cualquier aplicación que los admita, porque las partes de la dirección URL que no están incluidas en el atributo **href** de un elemento se incluyen en la dirección URL enviada por la aplicación al servidor cuando se solicita esa dirección URL.</span><span class="sxs-lookup"><span data-stu-id="ab897-113">Relative links work, in any application that supports them, because the parts of the URL not included in the **HREF** attribute of an element are included in the URL sent by the application to the server when that URL is requested.</span></span> <span data-ttu-id="ab897-114">Esto significa que el protocolo (como https://), el nombre del servidor y el directorio virtual en el que se encuentra el archivo que contiene el vínculo relativo están incluidos en la dirección URL que se envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="ab897-114">This means that the protocol (such as https://), the server name, and the virtual directory in which the file containing the relative link is located are all included in the URL that is sent to the server.</span></span> <span data-ttu-id="ab897-115">Si el archivo multimedia o la dirección URL a la que se vincula mediante un vínculo relativo no residen en el mismo servidor que el metarchivo, el vínculo relativo no es válido.</span><span class="sxs-lookup"><span data-stu-id="ab897-115">If the media file, or URL you link to using a relative link does not reside on the same server as the metafile, the relative link is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="ab897-116">Esta información sobre vínculos relativos solo es correcta cuando se usa un vínculo a los metaarchivos que se abren en el Media Player de Windows independiente.</span><span class="sxs-lookup"><span data-stu-id="ab897-116">This information on relative links is correct only when using a link to metafiles that are opened in the stand-alone Windows Media Player.</span></span> <span data-ttu-id="ab897-117">Cuando se usa el control Embedded Windows Media Player, todos los vínculos son relativos a la página en la que se hospeda el control, a menos que se use el elemento secundario **base** del elemento **ASX** para redirigir la ruta de acceso relativa.</span><span class="sxs-lookup"><span data-stu-id="ab897-117">When you use the embedded Windows Media Player control, all links are relative to the page on which the control is hosted, unless the **BASE** child element of the **ASX** element is used to redirect the relative path.</span></span>

 

<span data-ttu-id="ab897-118">Todos los vínculos relativos del metarchivo deben ser totalmente relativos, no relativos a la unidad, para los medios de streaming.</span><span class="sxs-lookup"><span data-stu-id="ab897-118">All relative links in the metafile must be fully relative, not drive-relative, for streaming media.</span></span> <span data-ttu-id="ab897-119">Cuando una dirección URL comienza con un \\ carácter "", el vínculo es relativo a la unidad.</span><span class="sxs-lookup"><span data-stu-id="ab897-119">When a URL begins with a "\\" character, the link is drive-relative.</span></span> <span data-ttu-id="ab897-120">Windows Media Player intenta abrir el archivo vinculado a en la unidad en la que se abrió el metarchivo, normalmente un servidor Web.</span><span class="sxs-lookup"><span data-stu-id="ab897-120">Windows Media Player attempts to open the file linked to on the drive where the metafile was opened from, usually a web server.</span></span> <span data-ttu-id="ab897-121">Dado que los servidores web usan directorios virtuales, Windows Media Player intenta encontrar el flujo especificado o el archivo multimedia en un subdirectorio de un directorio virtual del servidor web desde el que se abrió el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="ab897-121">Because web servers use virtual directories, Windows Media Player tries to find the specified stream or media file in a subdirectory of a virtual directory on the web server where the metafile was opened from.</span></span> <span data-ttu-id="ab897-122">Un usuario no tendría acceso a un directorio del servidor.</span><span class="sxs-lookup"><span data-stu-id="ab897-122">A user would not have access to a server directory.</span></span> <span data-ttu-id="ab897-123">En el ejemplo de esta sección se muestra el uso de un vínculo totalmente relativo.</span><span class="sxs-lookup"><span data-stu-id="ab897-123">The example in this section illustrates the use of a fully relative link.</span></span>

<span data-ttu-id="ab897-124">Puede usar vínculos relativos a unidades de disco al usar metaarchivos en un único equipo en el que todos los archivos multimedia a los que se ha vinculado en la lista de reproducción del metarchivo existen en un dispositivo de almacenamiento de ese equipo.</span><span class="sxs-lookup"><span data-stu-id="ab897-124">You can use drive-relative links when using metafiles on a single computer where all media files linked to in the metafile playlist exist on a storage device in that computer.</span></span> <span data-ttu-id="ab897-125">Sin embargo, no puede transmitir multimedia de esta manera.</span><span class="sxs-lookup"><span data-stu-id="ab897-125">However, you cannot stream media in this manner.</span></span>

<span data-ttu-id="ab897-126">Cuando se usa un vínculo a otro metarchivo para permitir vínculos relativos, el nombre mostrado como título por Windows Media Player es el título del metarchivo original.</span><span class="sxs-lookup"><span data-stu-id="ab897-126">When you use a link to another metafile to allow for relative links, the name displayed as the Title by Windows Media Player is the Title in the original metafile.</span></span>

<span data-ttu-id="ab897-127">Los vínculos relativos no se pueden usar para las direcciones URL en un servidor de streaming multimedia porque se usan protocolos diferentes para tener acceso al contenido multimedia de streaming.</span><span class="sxs-lookup"><span data-stu-id="ab897-127">Relative links cannot be used for URLs to a streaming media server because different protocols are used for accessing streaming media content.</span></span>

<span data-ttu-id="ab897-128">En la lista de reproducción de ejemplo siguiente, el primer **ENTRYREF** contiene una dirección URL para otra lista de reproducción, relative. Wax.</span><span class="sxs-lookup"><span data-stu-id="ab897-128">In the following example playlist, the first **ENTRYREF** contains a URL for another playlist, relative.wax.</span></span>


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



<span data-ttu-id="ab897-129">El siguiente ejemplo es el archivo relative. Wax, que contiene vínculos relativos.</span><span class="sxs-lookup"><span data-stu-id="ab897-129">The following example is the file relative.wax, which contains relative links.</span></span>


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



<span data-ttu-id="ab897-130">La dirección URL que contiene la referencia a la lista de reproducción, relative. Wax, puede existir en una lista de reproducción de metarchivo en cualquier lugar que sea accesible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ab897-130">The URL containing the reference to the playlist, relative.wax, can exist in a metafile playlist anywhere that is accessible to the user.</span></span> <span data-ttu-id="ab897-131">Para que la dirección URL se procese correctamente, debe haber un servidor Web denominado "example.microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="ab897-131">For the URL to be processed successfully, there must be a web server named "example.microsoft.com".</span></span> <span data-ttu-id="ab897-132">Ese servidor Web debe tener un directorio virtual definido como "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="ab897-132">That web server must have a virtual directory defined as "metafiles".</span></span> <span data-ttu-id="ab897-133">La lista de reproducción a la que se hace referencia, relative. Wax, debe existir en el servidor Web denominado "example.microsoft.com" en el directorio virtual "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="ab897-133">The referenced playlist, relative.wax, must exist on the web server named "example.microsoft.com" in the virtual directory "metafiles".</span></span>

<span data-ttu-id="ab897-134">En el caso de los archivos multimedia a los que se hace referencia en la lista de reproducción relativa. Wax para tener acceso y reproducirse correctamente, debe haber un directorio denominado "Graphics", que es un subdirectorio del directorio virtual del servidor "Metafiles".</span><span class="sxs-lookup"><span data-stu-id="ab897-134">For the referenced media files in the playlist relative.wax to be successfully accessed and played, there must be a directory named "Graphics" which is a subdirectory of the server's virtual directory "metafiles".</span></span> <span data-ttu-id="ab897-135">El archivo de gráficos Logo1.jpg, al que se hace referencia en el elemento **banner** , debe ser el subdirectorio denominado Graphics.</span><span class="sxs-lookup"><span data-stu-id="ab897-135">The graphics file Logo1.jpg, referenced in the **BANNER** element, must be the subdirectory named Graphics.</span></span>

<span data-ttu-id="ab897-136">Del mismo modo, un documento denominado Category1.htm debe residir en un subdirectorio denominado Category1.</span><span class="sxs-lookup"><span data-stu-id="ab897-136">Similarly a document named Category1.htm must reside in a subdirectory named Category1.</span></span> <span data-ttu-id="ab897-137">El directorio denominado Category1 debe existir como subdirectorio del directorio virtual "Metafiles" en el servidor Web example.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="ab897-137">The directory named Category1 must exist as a subdirectory of the virtual directory "metafiles" on the web server example.microsoft.com.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab897-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab897-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab897-139">**Crear listas de reproducción de metarchivo**</span><span class="sxs-lookup"><span data-stu-id="ab897-139">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ab897-140">**Listas de reproducción de metarchivos**</span><span class="sxs-lookup"><span data-stu-id="ab897-140">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="ab897-141">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ab897-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="ab897-142">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ab897-142">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




