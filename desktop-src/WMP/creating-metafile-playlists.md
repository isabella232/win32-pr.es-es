---
title: Crear listas de reproducción de metarchivo
description: Crear listas de reproducción de metarchivo
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Listas de reproducción de metarchivos de Windows Media, crear
- listas de reproducción, crear
- listas de reproducción de metarchivos, crear
- crear listas de reproducción de metarchivo de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269127"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="836fa-107">Crear listas de reproducción de metarchivo</span><span class="sxs-lookup"><span data-stu-id="836fa-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="836fa-108">Puede crear una lista de reproducción mediante cualquier editor de texto, como el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="836fa-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="836fa-109">Abra el editor de texto.</span><span class="sxs-lookup"><span data-stu-id="836fa-109">Open your text editor.</span></span> <span data-ttu-id="836fa-110">Escriba las entradas de script que desea implementar.</span><span class="sxs-lookup"><span data-stu-id="836fa-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="836fa-111">Una vez que haya terminado de escribir en el Bloc de notas, guarde el archivo con un nombre de archivo y una extensión de nombre de archivo apropiados.</span><span class="sxs-lookup"><span data-stu-id="836fa-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="836fa-112">Para obtener más información acerca de las extensiones, consulte [instrucciones de extensión de metarchivo](metafile-extension-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="836fa-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="836fa-113">Normalmente, el nombre de archivo es el nombre del archivo o secuencia de Windows Media seguido de una extensión de. Wax,. wvx o. ASX.</span><span class="sxs-lookup"><span data-stu-id="836fa-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="836fa-114">Por ejemplo, si el contenido multimedia es un archivo de audio de Windows Media con la extensión. WMA, use la extensión. Wax al asignar un nombre a la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="836fa-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="836fa-115">Las listas de reproducción no deben incluir códigos de formato de un procesador de textos, como Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="836fa-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="836fa-116">Para asegurarse de que no se incluyen códigos de formato en la lista de reproducción, guarde el archivo como texto sin formato o como archivo ASCII.</span><span class="sxs-lookup"><span data-stu-id="836fa-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="836fa-117">Los elementos y los atributos no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="836fa-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="836fa-118">El texto que se utiliza en la lista de reproducción para definir un elemento o un atributo puede estar en mayúsculas o en minúsculas, o bien una combinación de ambos.</span><span class="sxs-lookup"><span data-stu-id="836fa-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="836fa-119">Si un elemento no tiene elementos secundarios (los que modifican o están contenidos en otro elemento), se puede usar un carácter de barra diagonal (/) al final de la etiqueta de apertura, justo antes de la ' > ', en lugar de una etiqueta de cierre.</span><span class="sxs-lookup"><span data-stu-id="836fa-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="836fa-120">Los elementos secundarios de un elemento deben aparecer entre la etiqueta de apertura y el cierre de ese elemento; de lo contrario, no son elementos secundarios de ese elemento y se omiten o causan un error en la sintaxis de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="836fa-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="836fa-121">Los cuatro primeros caracteres de una lista de reproducción deben ser " &lt; ASX".</span><span class="sxs-lookup"><span data-stu-id="836fa-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="836fa-122">El elemento **ASX** se usa en todas las listas de reproducción si su extensión es. Wax,. wvx o. ASX.</span><span class="sxs-lookup"><span data-stu-id="836fa-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="836fa-123">Solo debe haber un elemento **ASX** por cada lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="836fa-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="836fa-124">Este elemento identifica el archivo como una lista de reproducción de metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="836fa-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="836fa-125">No especifica el tipo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="836fa-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="836fa-126">El elemento **ASX** tiene tres atributos posibles:</span><span class="sxs-lookup"><span data-stu-id="836fa-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="836fa-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="836fa-127">**VERSION**</span></span>

<span data-ttu-id="836fa-128">El atributo **version** es necesario y debe seguir inmediatamente después del elemento **ASX** , por ejemplo "<ASX version =" 3,0 " &gt; ".</span><span class="sxs-lookup"><span data-stu-id="836fa-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="836fa-129">El número de versión actual es 3,0.</span><span class="sxs-lookup"><span data-stu-id="836fa-129">The current version number is 3.0.</span></span> <span data-ttu-id="836fa-130">Windows Media Player es compatible con todas las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="836fa-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="836fa-131">Los valores aceptables para el atributo **version** incluyen 3,0 y 3 (sin separador decimal).</span><span class="sxs-lookup"><span data-stu-id="836fa-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="836fa-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="836fa-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="836fa-133">El atributo **PREVIEWMODE** es opcional.</span><span class="sxs-lookup"><span data-stu-id="836fa-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="836fa-134">Proporciona otro mecanismo para especificar cuánto tiempo se debe representar un clip.</span><span class="sxs-lookup"><span data-stu-id="836fa-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="836fa-135">Si el valor del atributo **PREVIEWMODE** es Yes, Windows Media Player representará cada clip durante la duración especificada por el elemento **PREVIEWDURATION**.</span><span class="sxs-lookup"><span data-stu-id="836fa-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="836fa-136">Cada clip puede tener un **PREVIEWDURATION** especificado.</span><span class="sxs-lookup"><span data-stu-id="836fa-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="836fa-137">**BANNERBAR**</span><span class="sxs-lookup"><span data-stu-id="836fa-137">**BANNERBAR**</span></span>

<span data-ttu-id="836fa-138">El atributo **BANNERBAR** opcional define si el control de Media Player de Windows Reserva espacio para un gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="836fa-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="836fa-139">(Use el elemento **banner** para especificar el gráfico que se va a mostrar). Si el valor de **BANNERBAR** es fijo, Windows Media Player reserva el espacio de banner para la presentación y para cada clip, independientemente de si la lista de reproducción del metarchivo especifica un banner para el programa o el clip.</span><span class="sxs-lookup"><span data-stu-id="836fa-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="836fa-140">Esto hará que el tamaño de la ventana de Media Player de Windows sea el mismo (excepto cuando el tamaño del vídeo cambie) independientemente de la ausencia o la presencia de un gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="836fa-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="836fa-141">Si el programa o el clip no tienen un encabezado asociado, el espacio reservado para uno es negro.</span><span class="sxs-lookup"><span data-stu-id="836fa-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="836fa-142">Si el valor del atributo **BANNERBAR** es auto, Windows Media Player Reserva espacio para el banner solo cuando el programa o el clip incluye uno.</span><span class="sxs-lookup"><span data-stu-id="836fa-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="836fa-143">Para obtener más información sobre los tres atributos del elemento **ASX** , vea la entrada de referencia para el [elemento ASX](asx-element.md).</span><span class="sxs-lookup"><span data-stu-id="836fa-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="836fa-144">Un elemento **ASX** contiene elementos secundarios **entry** que definen información sobre los archivos multimedia a los que se va a obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="836fa-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="836fa-145">Cada elemento **entry** debe contener un elemento **ref** que especifique la ruta de acceso al archivo multimedia que se va a transmitir.</span><span class="sxs-lookup"><span data-stu-id="836fa-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="836fa-146">Debe haber al menos un elemento **entry** o **ENTRYREF** dentro de un elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="836fa-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="836fa-147">Otros elementos definidos dentro del ámbito del elemento **ASX** , como **title** y **Author**, se asocian con los metadatos que muestra Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="836fa-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="836fa-148">Las listas de reproducción más sencillas se crean agregando varios elementos de **entrada** con un solo elemento **ref** a un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="836fa-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="836fa-149">Cada elemento de **entrada** de una lista de reproducción de metarchivo se representa en el orden en que aparece en el archivo como si el usuario hubiera abierto manualmente cada clip.</span><span class="sxs-lookup"><span data-stu-id="836fa-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="836fa-150">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="836fa-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="836fa-151">Asegúrese de que la lista de reproducción funcione haciendo doble clic en él en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="836fa-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="836fa-152">Windows Media Player debe abrir y comenzar a transmitir por secuencias el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="836fa-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="836fa-153">Una vez que haya confirmado que la lista de reproducción funciona, guárdela en el servidor web junto con las páginas web y vincúlela por medio de un elemento **href** o insértela en una página web mediante el elemento de **objeto** Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="836fa-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="836fa-154">Las secciones siguientes contienen más información:</span><span class="sxs-lookup"><span data-stu-id="836fa-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="836fa-155">Anidar metaarchivos</span><span class="sxs-lookup"><span data-stu-id="836fa-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="836fa-156">Usar páginas ASP para crear de forma dinámica listas de reproducción de metarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="836fa-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="836fa-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="836fa-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="836fa-158">**Elemento BANNER**</span><span class="sxs-lookup"><span data-stu-id="836fa-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="836fa-159">**Listas de reproducción de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="836fa-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="836fa-160">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="836fa-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="836fa-161">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="836fa-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




