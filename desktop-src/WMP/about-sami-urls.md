---
title: Acerca de las direcciones URL de SAMI
description: Acerca de las direcciones URL de SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
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
- Intercambio de multimedia accesible sincronizado (SAMI), direcciones URL
- SAMI (intercambio de multimedia accesible sincronizado), direcciones URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268591"
---
# <a name="about-sami-urls"></a><span data-ttu-id="83fba-114">Acerca de las direcciones URL de SAMI</span><span class="sxs-lookup"><span data-stu-id="83fba-114">About SAMI URLs</span></span>

<span data-ttu-id="83fba-115">Los archivos SAMI se pueden asociar a archivos multimedia digitales mediante una sola dirección URL.</span><span class="sxs-lookup"><span data-stu-id="83fba-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="83fba-116">Esto se logra mediante *el parámetro de* dirección URL Sami.</span><span class="sxs-lookup"><span data-stu-id="83fba-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="83fba-117">El parámetro de dirección URL está precedido por la dirección URL base y un signo?</span><span class="sxs-lookup"><span data-stu-id="83fba-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="83fba-118">.</span><span class="sxs-lookup"><span data-stu-id="83fba-118">character.</span></span> <span data-ttu-id="83fba-119">Una dirección URL con un parámetro *Sami* sigue esta sintaxis:</span><span class="sxs-lookup"><span data-stu-id="83fba-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="83fba-120">¿ *Dirección URL*? *Sami* = *captionsURL*.</span><span class="sxs-lookup"><span data-stu-id="83fba-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="83fba-121">El valor del parámetro URL sigue el nombre del parámetro y un signo igual, como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="83fba-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="83fba-122">Esta sintaxis de URL se usa normalmente en un hipervínculo o un metarchivo de Windows Media para vincular directamente a las ubicaciones del archivo multimedia digital y del archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="83fba-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="83fba-123">Cuando el usuario hace clic en el hipervínculo, Windows Media Player se inicia en modo completo y reproduce el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="83fba-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="83fba-124">Si no se especifica el parámetro de dirección URL *Sami* , Windows Media Player buscará un archivo Sami que esté en la misma ubicación que el archivo multimedia digital y que tenga el mismo nombre de archivo, excepto la extensión de nombre de archivo, que debe ser. SMI.</span><span class="sxs-lookup"><span data-stu-id="83fba-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="83fba-125">Si este tipo de archivo está presente, se abrirá automáticamente si se ha habilitado la presentación de títulos en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="83fba-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="83fba-126">Para habilitar los subtítulos en Windows Media Player, haga clic en el menú **reproducir** , haga clic en **subtítulos y subtítulos optativos** y, a continuación, haga clic **en activado**.</span><span class="sxs-lookup"><span data-stu-id="83fba-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="83fba-127">Si los subtítulos están habilitados, se mostrarán los títulos contenidos en el archivo SAMI mientras se reproduce el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="83fba-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83fba-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83fba-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83fba-129">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="83fba-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




