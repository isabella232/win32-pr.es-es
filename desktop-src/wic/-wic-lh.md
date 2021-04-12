---
description: Windows Imaging Component
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Windows Imaging Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277772"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="3a10c-103">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="3a10c-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="3a10c-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="3a10c-104">Purpose</span></span>

<span data-ttu-id="3a10c-105">El componente de creación de imágenes de Windows (WIC) es una plataforma extensible que proporciona una API de bajo nivel para imágenes digitales.</span><span class="sxs-lookup"><span data-stu-id="3a10c-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="3a10c-106">WIC admite los formatos de imagen web estándar, imágenes de rango dinámico alto y datos de cámara sin procesar.</span><span class="sxs-lookup"><span data-stu-id="3a10c-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="3a10c-107">WIC también admite características adicionales, como:</span><span class="sxs-lookup"><span data-stu-id="3a10c-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="3a10c-108">Compatibilidad integrada con formatos de metadatos estándar</span><span class="sxs-lookup"><span data-stu-id="3a10c-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="3a10c-109">Marco extensible para códecs de imagen, formatos de píxeles y formatos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3a10c-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="3a10c-110">Gran variedad de compatibilidad con el formato de píxeles.</span><span class="sxs-lookup"><span data-stu-id="3a10c-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="3a10c-111">Compatibilidad de alto color; incluye formatos de intervalo extendido de 30 bits, alta precisión de 30 bits y alta precisión de 48 bits y de gama ancha.</span><span class="sxs-lookup"><span data-stu-id="3a10c-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="3a10c-112">Descodificación de imágenes progresivas.</span><span class="sxs-lookup"><span data-stu-id="3a10c-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3a10c-113">Audiencia de los desarrolladores</span><span class="sxs-lookup"><span data-stu-id="3a10c-113">Developer Audience</span></span>

<span data-ttu-id="3a10c-114">WIC está diseñado para satisfacer las necesidades de las siguientes clases de desarrolladores:</span><span class="sxs-lookup"><span data-stu-id="3a10c-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="3a10c-115">Desarrolladores que leen y escriben datos de imagen en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a10c-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="3a10c-116">Desarrolladores que leen y escriben metadatos de imagen en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a10c-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="3a10c-117">Desarrolladores que desean la detección de códecs en tiempo de ejecución para códecs de imagen recién diseñados o implementados.</span><span class="sxs-lookup"><span data-stu-id="3a10c-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="3a10c-118">Desarrolladores que diseñan o implementan nuevos códecs de imagen y formatos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3a10c-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="3a10c-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="3a10c-119">In this section</span></span>



| <span data-ttu-id="3a10c-120">Tema</span><span class="sxs-lookup"><span data-stu-id="3a10c-120">Topic</span></span>                                                                 | <span data-ttu-id="3a10c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a10c-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="3a10c-122">Novedades de WIC</span><span class="sxs-lookup"><span data-stu-id="3a10c-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="3a10c-123">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="3a10c-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="3a10c-124">Describe cómo usar las API de WIC.</span><span class="sxs-lookup"><span data-stu-id="3a10c-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="3a10c-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="3a10c-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="3a10c-126">Contiene la referencia de las API de WIC.</span><span class="sxs-lookup"><span data-stu-id="3a10c-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="3a10c-127">Ejemplos de WIC</span><span class="sxs-lookup"><span data-stu-id="3a10c-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="3a10c-128">Proporciona ejemplos para WIC.</span><span class="sxs-lookup"><span data-stu-id="3a10c-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="3a10c-129">Glosario</span><span class="sxs-lookup"><span data-stu-id="3a10c-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="3a10c-130">Define los términos que se usan en WIC.</span><span class="sxs-lookup"><span data-stu-id="3a10c-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




