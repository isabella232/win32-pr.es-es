---
title: Referencia de metarchivos de Windows Media
description: Referencia de metarchivos de Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Metaarchivos de Windows Media, referencia
- metaarchivos, referencia
- referencia de los metaarchivos de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075686"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="4e4bd-106">Referencia de metarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="4e4bd-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="4e4bd-107">Esta referencia documenta elementos y extensiones de nombre de archivo para los metaarchivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="4e4bd-108">La referencia se divide en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="4e4bd-109">Sección</span><span class="sxs-lookup"><span data-stu-id="4e4bd-109">Section</span></span>                                                                                    | <span data-ttu-id="4e4bd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e4bd-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e4bd-111">Referencia de elementos de metarchivo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="4e4bd-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="4e4bd-112">Documenta los elementos de metarchivo, incluidas las definiciones, los atributos y sus valores, y las condiciones especiales relacionadas con cada elemento.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="4e4bd-113">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="4e4bd-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="4e4bd-114">Documenta las extensiones de nombre de archivo de metarchivo con reglas e instrucciones sobre su uso.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="4e4bd-115">Los metaarchivos de Windows Media son archivos de texto que proporcionan información acerca de una secuencia de archivos y su presentación.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="4e4bd-116">Los metaarchivos se basan en la sintaxis de lenguaje de marcado extensible (XML) y se componen de varios elementos similares a XML con sus etiquetas y atributos.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="4e4bd-117">Cada elemento define una configuración o una acción para el streaming multimedia.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="4e4bd-118">Hay dos conjuntos de etiquetas de elementos disponibles para los metaarchivos.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="4e4bd-119">Los metaarchivos del lado cliente tienen un conjunto de elementos y los metaarchivos del servidor tienen otro conjunto de elementos.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="4e4bd-120">Si una etiqueta de elemento no tiene ningún elemento secundario (los que modifican o están contenidos en otro elemento), se puede usar un carácter de barra diagonal (/) al final de la etiqueta de apertura en lugar de una etiqueta de cierre.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="4e4bd-121">Si los elementos secundarios no aparecen entre la etiqueta de apertura y cierre de un elemento, no son elementos secundarios de ese elemento y se omiten o causan un error en la sintaxis del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="4e4bd-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e4bd-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e4bd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e4bd-123">**Acerca de los metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4e4bd-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="4e4bd-124">**Guía de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4e4bd-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="4e4bd-125">**Metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4e4bd-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




