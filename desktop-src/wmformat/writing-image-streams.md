---
title: Escribir secuencias de imagen
description: Escribir secuencias de imagen
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF), escribir secuencias de imágenes
- ASF (formato de sistemas avanzados), escribir secuencias de imágenes
- Advanced Systems Format (ASF), stream Image
- ASF (formato de sistemas avanzados), flujos de imagen
- flujos de imagen, escritura
- secuencias, escribir secuencias de imagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994950"
---
# <a name="writing-image-streams"></a><span data-ttu-id="d5621-109">Escribir secuencias de imagen</span><span class="sxs-lookup"><span data-stu-id="d5621-109">Writing Image Streams</span></span>

<span data-ttu-id="d5621-110">Las entradas de un flujo de imagen deben ser imágenes de mapa de bits con formato RGB.</span><span class="sxs-lookup"><span data-stu-id="d5621-110">The inputs for an image stream must be RGB-formatted bitmap images.</span></span> <span data-ttu-id="d5621-111">El escritor coordina la compresión de los ejemplos de imagen de entrada con el formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="d5621-111">The writer coordinates the compression of input image samples using the JPEG format.</span></span> <span data-ttu-id="d5621-112">Antes de empezar a escribir un archivo que contiene una secuencia de imagen, debe establecer una calidad de imagen para la entrada mediante el \_ valor g wszJPEGCompressionQuality.</span><span class="sxs-lookup"><span data-stu-id="d5621-112">Before you begin writing a file containing an image stream, you must set an image quality for the input, using the g\_wszJPEGCompressionQuality setting.</span></span> <span data-ttu-id="d5621-113">Use [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para establecer la calidad en un valor **DWORD** comprendido entre 1 y 100.</span><span class="sxs-lookup"><span data-stu-id="d5621-113">Use [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) to set the quality to a **DWORD** value ranging from 1 to 100.</span></span> <span data-ttu-id="d5621-114">Los valores bajos representan una alta relación de compresión a costa de la calidad, mientras que los valores altos producen imágenes de alta calidad que requieren más espacio.</span><span class="sxs-lookup"><span data-stu-id="d5621-114">Low values represent a high compression ratio at the expense of quality, while high values produce high quality images that require more space.</span></span>

<span data-ttu-id="d5621-115">Los flujos de imágenes suelen requerir ventanas de búfer más grandes que las secuencias de vídeo normales.</span><span class="sxs-lookup"><span data-stu-id="d5621-115">Image streams often require larger buffer windows than ordinary video streams.</span></span> <span data-ttu-id="d5621-116">El tamaño exacto necesario depende del tipo de imagen y de la calidad de la imagen, entre otros factores.</span><span class="sxs-lookup"><span data-stu-id="d5621-116">The exact size required depends on the type of image and the image quality, among other factors.</span></span> <span data-ttu-id="d5621-117">Use la prueba y el error para determinar el tamaño adecuado para las imágenes que desea procesar.</span><span class="sxs-lookup"><span data-stu-id="d5621-117">Use trial and error to determine the appropriate size for the images you intend to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5621-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5621-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5621-119">**Flujos de imagen**</span><span class="sxs-lookup"><span data-stu-id="d5621-119">**Image Streams**</span></span>](image-streams.md)
</dt> <dt>

[<span data-ttu-id="d5621-120">**Para establecer la configuración de entrada**</span><span class="sxs-lookup"><span data-stu-id="d5621-120">**To Set Input Settings**</span></span>](to-set-input-settings.md)
</dt> <dt>

[<span data-ttu-id="d5621-121">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="d5621-121">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




