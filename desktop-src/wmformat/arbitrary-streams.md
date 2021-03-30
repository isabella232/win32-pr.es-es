---
title: Flujos arbitrarios
description: Flujos arbitrarios
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- SDK de Windows Media Format, secuencias arbitrarias
- Advanced Systems Format (ASF), streams arbitrarios
- ASF (formato de sistemas avanzados), secuencias arbitrarias
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- flujos arbitrarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773405"
---
# <a name="arbitrary-streams"></a><span data-ttu-id="e7280-110">Flujos arbitrarios</span><span class="sxs-lookup"><span data-stu-id="e7280-110">Arbitrary Streams</span></span>

<span data-ttu-id="e7280-111">Además de las secuencias de audio y vídeo, y las secuencias de imágenes, un archivo ASF puede alojar secuencias que contengan una variedad de datos.</span><span class="sxs-lookup"><span data-stu-id="e7280-111">In addition to audio and video streams and image streams, an ASF file can accommodate streams containing a variety of data.</span></span> <span data-ttu-id="e7280-112">Los objetos del SDK de Windows Media Format proporcionan compatibilidad con secuencias de scripts, secuencias de transferencia de archivos, secuencias web y flujos de datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="e7280-112">The objects of the Windows Media Format SDK provide support for script streams, file transfer streams, Web streams, and arbitrary data streams.</span></span> <span data-ttu-id="e7280-113">Todos estos tipos de flujo son arbitrarios, lo que significa que el objeto de lectura no realiza ninguna validación de datos.</span><span class="sxs-lookup"><span data-stu-id="e7280-113">All of these stream types are arbitrary, meaning that no data validation is performed by the reading object.</span></span> <span data-ttu-id="e7280-114">Al incluir secuencias de estos tipos en los archivos, asegúrese de que la aplicación de lectura realiza la validación o la comprobación de datos para asegurarse de que el contenido no se ha dañado o se ha alterado intencionadamente por un tercero malintencionado.</span><span class="sxs-lookup"><span data-stu-id="e7280-114">When you include streams of these types in your files, be sure that the reading application performs validation or data checking to ensure that your content has not been corrupted or intentionally mangled by a malicious third party.</span></span>

<span data-ttu-id="e7280-115">Aunque los objetos de este SDK no comprueban ni validan datos en flujos arbitrarios, se admiten de forma nativa varios tipos de secuencias arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="e7280-115">Although the objects of this SDK do not verify or validate data in arbitrary streams, several types of arbitrary streams are natively supported.</span></span> <span data-ttu-id="e7280-116">En la tabla siguiente se enumeran los tipos de secuencia arbitrarios predefinidos.</span><span class="sxs-lookup"><span data-stu-id="e7280-116">The following table lists the predefined arbitrary stream types.</span></span> <span data-ttu-id="e7280-117">También se admiten secuencias de script, pero se tratan por separado en la sección [comandos de script](script-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="e7280-117">Script streams are also supported, but are discussed separately in the [Script Commands](script-commands.md) section.</span></span> <span data-ttu-id="e7280-118">Para obtener más información sobre la creación de tipos personalizados, vea [flujos de datos arbitrarios personalizados](custom-arbitrary-data-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e7280-118">For more information about creating custom types, see [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).</span></span>



| <span data-ttu-id="e7280-119">Tipo arbitrario</span><span class="sxs-lookup"><span data-stu-id="e7280-119">Arbitrary type</span></span>                   | <span data-ttu-id="e7280-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7280-120">Description</span></span>                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="e7280-121">Secuencias de texto</span><span class="sxs-lookup"><span data-stu-id="e7280-121">Text Streams</span></span>](text-streams.md) | <span data-ttu-id="e7280-122">Contienen cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="e7280-122">Contain text strings.</span></span>                                             |
| [<span data-ttu-id="e7280-123">Secuencias de archivo</span><span class="sxs-lookup"><span data-stu-id="e7280-123">File Streams</span></span>](file-streams.md) | <span data-ttu-id="e7280-124">Contener uno o más archivos de datos.</span><span class="sxs-lookup"><span data-stu-id="e7280-124">Contain one or more data files.</span></span>                                   |
| [<span data-ttu-id="e7280-125">Secuencias Web</span><span class="sxs-lookup"><span data-stu-id="e7280-125">Web Streams</span></span>](web-streams.md)   | <span data-ttu-id="e7280-126">Contienen archivos de datos equivalentes a la versión almacenada en caché de las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="e7280-126">Contain data files equivalent to the cached version of Web pages.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e7280-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7280-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7280-128">**Características de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="e7280-128">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="e7280-129">**Secuencias de audio y vídeo**</span><span class="sxs-lookup"><span data-stu-id="e7280-129">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="e7280-130">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="e7280-130">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




