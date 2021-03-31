---
title: Acerca de los archivos SAMI
description: Acerca de los archivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de contenido multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio de multimedia accesible sincronizado), archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903535"
---
# <a name="about-sami-files"></a><span data-ttu-id="c1395-112">Acerca de los archivos SAMI</span><span class="sxs-lookup"><span data-stu-id="c1395-112">About SAMI Files</span></span>

<span data-ttu-id="c1395-113">Los archivos SAMI son archivos de texto que tienen una extensión de nombre de archivo. SMI o. Sami.</span><span class="sxs-lookup"><span data-stu-id="c1395-113">SAMI files are text files that have an .smi or .sami file name extension.</span></span> <span data-ttu-id="c1395-114">Contienen las cadenas de texto que se usan para subtítulos cerrados, subtítulos y descripciones de audio sincronizados.</span><span class="sxs-lookup"><span data-stu-id="c1395-114">They contain the text strings used for synchronized closed captions, subtitles, and audio descriptions.</span></span> <span data-ttu-id="c1395-115">También especifican los parámetros de tiempo utilizados por el control de Media Player de Windows para sincronizar el texto de subtítulos con el contenido de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="c1395-115">They also specify the timing parameters used by the Windows Media Player control to synchronize closed caption text with audio or video content.</span></span> <span data-ttu-id="c1395-116">Cuando un archivo multimedia digital alcanza una hora designada en el archivo SAMI, el texto cambia en consecuencia en el área de presentación de la leyenda cerrada de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="c1395-116">When a digital media file reaches a time designated in the SAMI file, the text changes accordingly in the closed caption display area of the webpage.</span></span>

<span data-ttu-id="c1395-117">Aparte de un simple editor de texto (como el Bloc de notas de Microsoft), no se requiere software especial para crear un archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="c1395-117">Other than a simple text editor (such as Microsoft Notepad), special software is not required to create a SAMI file.</span></span> <span data-ttu-id="c1395-118">SAMI y HTML comparten elementos comunes, como las <HEAD> etiquetas y <BODY> .</span><span class="sxs-lookup"><span data-stu-id="c1395-118">SAMI and HTML share common elements, such as the <HEAD> and <BODY> tags.</span></span> <span data-ttu-id="c1395-119">Como en HTML, las etiquetas utilizadas en los archivos SAMI siempre deben usarse en pares.</span><span class="sxs-lookup"><span data-stu-id="c1395-119">As in HTML, tags used in SAMI files must always be used in pairs.</span></span> <span data-ttu-id="c1395-120">Por ejemplo, un elemento BODY comienza con una <BODY> etiqueta y siempre debe terminar con una </BODY> etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c1395-120">For example, a BODY element begins with a <BODY> tag and must always end with a </BODY> tag.</span></span>

<span data-ttu-id="c1395-121">Un archivo SAMI básico requiere tres etiquetas fundamentales: <SAMI> , <HEAD> y <BODY> .</span><span class="sxs-lookup"><span data-stu-id="c1395-121">A basic SAMI file requires three fundamental tags: <SAMI>, <HEAD>, and <BODY>.</span></span>

<span data-ttu-id="c1395-122">La <SAMI> etiqueta identifica el documento como un documento Sami para que otras aplicaciones puedan reconocer su formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="c1395-122">The <SAMI> tag identifies the document as a SAMI document so other applications can recognize its file format.</span></span>

<span data-ttu-id="c1395-123">Entre las etiquetas <HEAD> y </HEAD> , se definen las instrucciones básicas y otra información de formato para el documento Sami, como el título del documento, la información general y las propiedades de estilo de los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="c1395-123">Between the <HEAD> and </HEAD> tags, you define basic guidelines and other format information for the SAMI document, such as the document title, general information, and style properties for closed captions.</span></span> <span data-ttu-id="c1395-124">Como HTML, el contenido declarado en el elemento de encabezado no se muestra como salida.</span><span class="sxs-lookup"><span data-stu-id="c1395-124">Like HTML, content declared within the HEAD element does not display as output.</span></span>

<span data-ttu-id="c1395-125">Los elementos y atributos definidos entre las etiquetas <BODY> y </BODY> muestran el contenido que el usuario ha visualizado.</span><span class="sxs-lookup"><span data-stu-id="c1395-125">Elements and attributes defined between the <BODY> and </BODY> tags display content seen by the user.</span></span> <span data-ttu-id="c1395-126">En SAMI, el elemento BODY contiene los parámetros para la sincronización y las cadenas de texto que se usan para los subtítulos cerrados.</span><span class="sxs-lookup"><span data-stu-id="c1395-126">In SAMI, the BODY element contains the parameters for synchronization and the text strings used for closed captions.</span></span>

<span data-ttu-id="c1395-127">Definido en el elemento de encabezado, el elemento de estilo proporciona la funcionalidad agregada en SAMI.</span><span class="sxs-lookup"><span data-stu-id="c1395-127">Defined within the HEAD element, the STYLE element provides for added functionality in SAMI.</span></span> <span data-ttu-id="c1395-128">Entre las etiquetas <STYLE> y </STYLE> , puede definir varios selectores de hoja de estilos en cascada (CSS) para el estilo y el diseño.</span><span class="sxs-lookup"><span data-stu-id="c1395-128">Between the <STYLE> and </STYLE> tags, you can define several Cascading Style Sheet (CSS) selectors for style and layout.</span></span> <span data-ttu-id="c1395-129">Las propiedades de estilo, como las fuentes, los tamaños y las alineaciones, se pueden personalizar para proporcionar una experiencia de usuario enriquecida, al tiempo que se fomenta la accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="c1395-129">Style properties such as fonts, sizes, and alignments can be customized to provide a rich user experience while also promoting accessibility.</span></span> <span data-ttu-id="c1395-130">Por ejemplo, la definición de una clase de estilo de fuente de texto grande puede mejorar la legibilidad de los usuarios que tienen dificultades para leer texto pequeño.</span><span class="sxs-lookup"><span data-stu-id="c1395-130">For example, defining a large text font style class can improve the readability for users who have difficulty reading small text.</span></span> <span data-ttu-id="c1395-131">Además, al definir varias clases de lenguaje diferentes, puede ayudar a los usuarios internacionales a entender mejor el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="c1395-131">In addition, by defining several different language classes, you can help international users better understand the digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1395-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1395-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1395-133">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="c1395-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




