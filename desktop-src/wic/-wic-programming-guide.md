---
title: Guía de programación de WIC
description: Describe cómo usar las API de WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423947"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="52574-103">Guía de programación de WIC</span><span class="sxs-lookup"><span data-stu-id="52574-103">WIC programming guide</span></span>

<span data-ttu-id="52574-104">Esta sección contiene temas conceptuales que describen cómo usar las API de Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="52574-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="52574-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="52574-105">In this section</span></span>



| <span data-ttu-id="52574-106">Tema</span><span class="sxs-lookup"><span data-stu-id="52574-106">Topic</span></span>                                                                                 | <span data-ttu-id="52574-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="52574-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52574-108">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="52574-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="52574-109">WIC proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes.</span><span class="sxs-lookup"><span data-stu-id="52574-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="52574-110">Información general sobre la API WIC</span><span class="sxs-lookup"><span data-stu-id="52574-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="52574-111">WIC proporciona una API basada en el modelo de objetos componentes (COM) para su uso en C y C++.</span><span class="sxs-lookup"><span data-stu-id="52574-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="52574-112">Descodificación de imágenes digitales</span><span class="sxs-lookup"><span data-stu-id="52574-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="52574-113">Esta sección contiene temas conceptuales y de procedimientos que describen los descodificadores de mapas de bits de WIC que se usan en la descodificación de imágenes digitales.</span><span class="sxs-lookup"><span data-stu-id="52574-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="52574-114">Uso de datos de imagen</span><span class="sxs-lookup"><span data-stu-id="52574-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="52574-115">Esta sección contiene temas conceptuales y de procedimientos que describen los orígenes de mapas de bits de WIC y cómo manipularlos.</span><span class="sxs-lookup"><span data-stu-id="52574-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="52574-116">Codificar datos de imagen</span><span class="sxs-lookup"><span data-stu-id="52574-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="52574-117">Esta sección contiene temas conceptuales y de procedimientos que describen los codificadores de mapas de bits de WIC que se usan para codificar imágenes digitales.</span><span class="sxs-lookup"><span data-stu-id="52574-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="52574-118">Códecs WIC nativos</span><span class="sxs-lookup"><span data-stu-id="52574-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="52574-119">Esta sección contiene información sobre los códecs de imágenes nativas disponibles en WIC.</span><span class="sxs-lookup"><span data-stu-id="52574-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="52574-120">Procesamiento de metadatos de imagen</span><span class="sxs-lookup"><span data-stu-id="52574-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="52574-121">Esta sección contiene temas conceptuales que describen el sistema de metadatos de WIC.</span><span class="sxs-lookup"><span data-stu-id="52574-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="52574-122">Compatibilidad con JPEG YCbCr</span><span class="sxs-lookup"><span data-stu-id="52574-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="52574-123">A partir de Windows 8.1, el códec JPEG de [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) admite la lectura y escritura de datos de imagen en su forma nativa<sub>de C</sub><sub>r</sub> de YC.</span><span class="sxs-lookup"><span data-stu-id="52574-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="52574-124">Administración del color</span><span class="sxs-lookup"><span data-stu-id="52574-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="52574-125">WIC simplifica la administración del color proporcionando la interfaz [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) y la interfaz [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .</span><span class="sxs-lookup"><span data-stu-id="52574-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="52574-126">Desarrollo de componentes</span><span class="sxs-lookup"><span data-stu-id="52574-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="52574-127">WIC es una plataforma extensible que proporciona una API de bajo nivel para imágenes digitales.</span><span class="sxs-lookup"><span data-stu-id="52574-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="52574-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="52574-128">See Also</span></span>

[<span data-ttu-id="52574-129">Referencia de WIC</span><span class="sxs-lookup"><span data-stu-id="52574-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="52574-130">Ejemplos de WIC</span><span class="sxs-lookup"><span data-stu-id="52574-130">WIC Samples</span></span>](-wic-samples.md)


 

 




