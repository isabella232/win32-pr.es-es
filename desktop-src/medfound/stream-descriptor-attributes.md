---
description: Atributos de descriptor de secuencia
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Atributos de descriptor de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811533"
---
# <a name="stream-descriptor-attributes"></a><span data-ttu-id="d3286-103">Atributos de descriptor de secuencia</span><span class="sxs-lookup"><span data-stu-id="d3286-103">Stream Descriptor Attributes</span></span>

## <a name="common-stream-descriptor-attributes"></a><span data-ttu-id="d3286-104">Atributos de descriptor de secuencia comunes</span><span class="sxs-lookup"><span data-stu-id="d3286-104">Common Stream Descriptor Attributes</span></span>

<span data-ttu-id="d3286-105">Los siguientes atributos se aplican a los descriptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="d3286-105">The following attributes apply to stream descriptors.</span></span>



| <span data-ttu-id="d3286-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="d3286-106">Attribute</span></span>                                                   | <span data-ttu-id="d3286-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3286-107">Description</span></span>                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3286-108">**\_idioma MF SD \_**</span><span class="sxs-lookup"><span data-stu-id="d3286-108">**MF\_SD\_LANGUAGE**</span></span>](mf-sd-language-attribute.md)        | <span data-ttu-id="d3286-109">Especifica el idioma de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="d3286-109">Specifies the language for a stream.</span></span>                                                  |
| [<span data-ttu-id="d3286-110">MF \_ SD \_ mutuamente \_ excluyente</span><span class="sxs-lookup"><span data-stu-id="d3286-110">MF\_SD\_MUTUALLY\_EXCLUSIVE</span></span>](mf-sd-mutually-exclusive.md) | <span data-ttu-id="d3286-111">Especifica si una secuencia es mutuamente excluyente con otras secuencias del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="d3286-111">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span> |
| [<span data-ttu-id="d3286-112">**MF \_ SD \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="d3286-112">**MF\_SD\_PROTECTED**</span></span>](mf-sd-protected-attribute.md)      | <span data-ttu-id="d3286-113">Especifica si una secuencia contiene contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="d3286-113">Specifies whether a stream contains protected content.</span></span>                                |
| [<span data-ttu-id="d3286-114">\_nombre de \_ flujo \_ SD MF</span><span class="sxs-lookup"><span data-stu-id="d3286-114">MF\_SD\_STREAM\_NAME</span></span>](mf-sd-stream-name.md)               | <span data-ttu-id="d3286-115">Contiene el nombre de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="d3286-115">Contains the name of a stream.</span></span>                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a><span data-ttu-id="d3286-116">ASF-Specific atributos del descriptor de flujo</span><span class="sxs-lookup"><span data-stu-id="d3286-116">ASF-Specific Stream Descriptor Attributes</span></span>

<span data-ttu-id="d3286-117">Los siguientes atributos se aplican a los descriptores de secuencia para los archivos de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="d3286-117">The following attributes apply to stream descriptors for Advanced Systems Format (ASF) files.</span></span>



| <span data-ttu-id="d3286-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="d3286-118">Attribute</span></span>                                                                                                                | <span data-ttu-id="d3286-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3286-119">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3286-120">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="d3286-120">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | <span data-ttu-id="d3286-121">Especifica el tamaño de búfer promedio necesario para una secuencia en un archivo ASF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d3286-121">Specifies the average buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="d3286-122">**\_velocidad de \_ \_ \_ bits promedio de \_ datos \_ ASF SD EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="d3286-122">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | <span data-ttu-id="d3286-123">Especifica la velocidad de bits de datos media de una secuencia en un archivo ASF, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3286-123">Specifies the average data bit rate of a stream in an ASF file, in bits per second.</span></span>        |
| [<span data-ttu-id="d3286-124">**\_Índice de \_ \_ \_ \_ ID. de idioma \_ de MF SD ASF EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="d3286-124">**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**</span></span>](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | <span data-ttu-id="d3286-125">Especifica el idioma usado por una secuencia en un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="d3286-125">Specifies the language used by a stream in an ASF file.</span></span>                                    |
| [<span data-ttu-id="d3286-126">**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**</span><span class="sxs-lookup"><span data-stu-id="d3286-126">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE**</span></span>](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | <span data-ttu-id="d3286-127">Especifica el tamaño de búfer máximo necesario para una secuencia en un archivo ASF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d3286-127">Specifies the maximum buffer size needed for a stream in an ASF file, in bytes.</span></span>            |
| [<span data-ttu-id="d3286-128">**\_velocidad de \_ \_ bits de \_ datos Max SD ASF EXTSTRMPROP máx \_ \_ .**</span><span class="sxs-lookup"><span data-stu-id="d3286-128">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | <span data-ttu-id="d3286-129">Especifica la velocidad de bits de datos máxima de una secuencia en un archivo ASF, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3286-129">Specifies the maximum data bit rate of a stream in an ASF file, in bits per second</span></span>         |
| [<span data-ttu-id="d3286-130">**\_plantilla de \_ \_ cumplimiento de dispositivos de metadatos ASF \_ \_ \_ de MF SD**</span><span class="sxs-lookup"><span data-stu-id="d3286-130">**MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE**</span></span>](mf-sd-asf-metadata-device-conformance-template-attribute.md) | <span data-ttu-id="d3286-131">Especifica la plantilla de conformidad de dispositivos de una secuencia en un archivo ASF, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3286-131">Specifies the device conformance template for a stream in an ASF file, in bits per second.</span></span> |
| [<span data-ttu-id="d3286-132">**\_velocidad de \_ bits de ASF SD ASF \_ STREAMBITRATES \_**</span><span class="sxs-lookup"><span data-stu-id="d3286-132">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | <span data-ttu-id="d3286-133">Especifica la velocidad de bits media de una secuencia en un archivo ASF, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="d3286-133">Specifies the average bit rate of a stream in an ASF file, in bits per second.</span></span>             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a><span data-ttu-id="d3286-134">Atributos de descriptor de flujo de origen de medios SAMI</span><span class="sxs-lookup"><span data-stu-id="d3286-134">SAMI Media Source Stream Descriptor Attributes</span></span>

<span data-ttu-id="d3286-135">El atributo siguiente se aplica al descriptor de flujo para el origen de medios SAMI.</span><span class="sxs-lookup"><span data-stu-id="d3286-135">The following attribute applies to the stream descriptor for the SAMI media source.</span></span>



| <span data-ttu-id="d3286-136">Atributo</span><span class="sxs-lookup"><span data-stu-id="d3286-136">Attribute</span></span>                                                       | <span data-ttu-id="d3286-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3286-137">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3286-138">**\_ \_ idioma sami MF \_ SD**</span><span class="sxs-lookup"><span data-stu-id="d3286-138">**MF\_SD\_SAMI\_LANGUAGE**</span></span>](mf-sd-sami-language-attribute.md) | <span data-ttu-id="d3286-139">Contiene el nombre del idioma de intercambio de medios accesibles (SAMI) sincronizado que se define para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d3286-139">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d3286-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3286-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3286-141">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d3286-141">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="d3286-142">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3286-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



