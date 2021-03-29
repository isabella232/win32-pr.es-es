---
title: Formatos de entrada, configuración de entrada y extensiones de unidad de datos
description: Formatos de entrada, configuración de entrada y extensiones de unidad de datos
ms.assetid: 8e8a0ec8-cb7c-4483-86b0-142ea9f2b835
keywords:
- SDK de Windows Media Format, formatos y configuraciones de entrada
- Windows Media Format SDK, extensiones de unidad de datos
- SDK de Windows Media Format, sistemas de extensión de carga
- Advanced Systems Format (ASF), formatos de entrada y configuraciones
- ASF (formato de sistemas avanzados), formatos y configuraciones de entrada
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- Advanced Systems Format (ASF), sistemas de extensión de carga útil
- ASF (formato de sistemas avanzados), sistemas de extensión de carga útil
- extensiones de unidad de datos, acerca de
- sistemas de extensión de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c590895fca23a3c668a19ac4e6c5437a35ddb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994471"
---
# <a name="input-formats-input-settings-and-data-unit-extensions"></a><span data-ttu-id="9e99e-114">Formatos de entrada, configuración de entrada y extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="9e99e-114">Input Formats, Input Settings, and Data Unit Extensions</span></span>

<span data-ttu-id="9e99e-115">El objeto escritor admite la configuración de entrada, los formatos de entrada y las extensiones de unidad de datos, que permiten controlar las características del escritor.</span><span class="sxs-lookup"><span data-stu-id="9e99e-115">The writer object supports input settings, input formats, and data unit extensions, all of which enable you to control features of the writer.</span></span> <span data-ttu-id="9e99e-116">No siempre es obvio qué métodos usar para controlar una característica específica.</span><span class="sxs-lookup"><span data-stu-id="9e99e-116">It is not always obvious which methods to use to control a specific feature.</span></span>

<span data-ttu-id="9e99e-117">Los formatos de entrada son formatos multimedia que describen las propiedades básicas de los medios que se pasan al escritor para la codificación.</span><span class="sxs-lookup"><span data-stu-id="9e99e-117">Input formats are media formats that describe the basic properties of the media that you pass to the writer for encoding.</span></span> <span data-ttu-id="9e99e-118">Por ejemplo, el tamaño de fotogramas y el espacio de color del vídeo de entrada se describen mediante el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="9e99e-118">For example, the frame size and color space of input video is described by the input format.</span></span>

<span data-ttu-id="9e99e-119">Los valores de entrada son características de los datos de entrada más allá de los conceptos básicos o información sobre las transformaciones que se deben realizar en los datos.</span><span class="sxs-lookup"><span data-stu-id="9e99e-119">Input settings are characteristics of the input data beyond the basics, or information about transforms to perform on the data.</span></span> <span data-ttu-id="9e99e-120">La configuración de vídeo entrelazada e información sobre un sistema de marca de agua son ejemplos de configuración de entrada.</span><span class="sxs-lookup"><span data-stu-id="9e99e-120">Interlaced video settings and information about a watermarking system are examples of input settings.</span></span>

<span data-ttu-id="9e99e-121">Las extensiones de unidad de datos, también denominadas sistemas de extensión de carga, son valores que se adjuntan a ejemplos individuales en la sección de datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="9e99e-121">Data unit extensions, also called payload extension systems, are values that are attached to individual samples in the data section of the file.</span></span> <span data-ttu-id="9e99e-122">Los códigos de tiempo de SMPTE y la información de píxeles no cuadrados son ejemplos de extensiones de unidad de datos.</span><span class="sxs-lookup"><span data-stu-id="9e99e-122">SMPTE time codes and non-square pixel information are examples of data unit extensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e99e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e99e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e99e-124">**Configuración de extensiones de unidades de datos**</span><span class="sxs-lookup"><span data-stu-id="9e99e-124">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="9e99e-125">**Extensiones de unidad de datos**</span><span class="sxs-lookup"><span data-stu-id="9e99e-125">**Data Unit Extensions**</span></span>](data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="9e99e-126">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="9e99e-126">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="9e99e-127">**Enumeración de formato de entrada**</span><span class="sxs-lookup"><span data-stu-id="9e99e-127">**Input Format Enumeration**</span></span>](input-format-enumeration.md)
</dt> <dt>

[<span data-ttu-id="9e99e-128">**Configuración de entrada**</span><span class="sxs-lookup"><span data-stu-id="9e99e-128">**Input Settings**</span></span>](input-settings.md)
</dt> <dt>

[<span data-ttu-id="9e99e-129">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="9e99e-129">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




