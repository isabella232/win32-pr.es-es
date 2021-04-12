---
title: Proporcionar una interfaz de usuario
description: Proporcionar una interfaz de usuario
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Complementos de Windows Media Player, páginas de propiedades
- complementos, páginas de propiedades
- Complementos de procesamiento de señal digital, páginas de propiedades
- Complementos DSP, páginas de propiedades
- Complementos de procesamiento de señal digital, interfaz de usuario
- Complementos DSP, interfaz de usuario
- páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269183"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="24561-110">Proporcionar una interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="24561-110">Providing a User Interface</span></span>

<span data-ttu-id="24561-111">Los complementos DSP pueden proporcionar una página de propiedades para crear una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="24561-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="24561-112">Para ello, el complemento debe incluir un objeto de página de propiedades que proporcione una implementación de una interfaz **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="24561-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="24561-113">El objeto de complemento DSP debe implementar **ISpecifyPropertyPages:: GetPages**, que permite a Windows Media Player buscar e identificar la página de propiedades correcta para el complemento.</span><span class="sxs-lookup"><span data-stu-id="24561-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="24561-114">**Mostrar un gráfico de estado**</span><span class="sxs-lookup"><span data-stu-id="24561-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="24561-115">Los complementos de DSP pueden mostrar un gráfico pequeño, o una serie de gráficos, en el área de estado de Windows Media Player para notificar al usuario que hay un complemento activo.</span><span class="sxs-lookup"><span data-stu-id="24561-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="24561-116">Para admitir esta característica, el complemento debe implementar la interfaz **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="24561-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="24561-117">Windows Media Player llama a **IPropertyBag:: Read**, proporcionando un puntero al nombre de propiedad solicitado "IconStreams", que distingue entre mayúsculas y minúsculas, y un puntero a una estructura **Variant** que recibe los datos para el gráfico.</span><span class="sxs-lookup"><span data-stu-id="24561-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="24561-118">El complemento crea un objeto **IStream** (o un SafeArray de objetos **IStream** si hay varios gráficos), después carga los datos gráficos, incluida la información de encabezado, en la secuencia y, a continuación, devuelve un puntero al objeto **IStream** mediante el miembro **punkVal** de la estructura **Variant** .</span><span class="sxs-lookup"><span data-stu-id="24561-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="24561-119">Si el complemento solo proporciona un gráfico, especifica el miembro **VT** de la estructura **variante** como VT \_ desconocido.</span><span class="sxs-lookup"><span data-stu-id="24561-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="24561-120">Si el complemento proporciona varios objetos de **IStream** de gráficos mediante SafeArray, especifica el miembro **VT** de la estructura **Variant** como \_ matriz VT.</span><span class="sxs-lookup"><span data-stu-id="24561-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="24561-121">Los gráficos pueden almacenarse en diversos formatos de archivo, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="24561-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="24561-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="24561-122">**BMP**</span></span>

<span data-ttu-id="24561-123">Las imágenes de mapa de bits de Microsoft Windows no están comprimidas.</span><span class="sxs-lookup"><span data-stu-id="24561-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="24561-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="24561-124">**JPEG**</span></span>

<span data-ttu-id="24561-125">Formato de imagen comprimido que se usa habitualmente para las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="24561-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="24561-126">Normalmente, los archivos de formato JPEG tienen extensiones de nombre de archivo. jpg.</span><span class="sxs-lookup"><span data-stu-id="24561-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="24561-127">**GIF**</span><span class="sxs-lookup"><span data-stu-id="24561-127">**GIF**</span></span>

<span data-ttu-id="24561-128">Formato de imagen comprimido que se usa habitualmente para las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="24561-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="24561-129">**PNG**</span><span class="sxs-lookup"><span data-stu-id="24561-129">**PNG**</span></span>

<span data-ttu-id="24561-130">Formato de imagen comprimido que se usa habitualmente para las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="24561-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="24561-131">Las dimensiones máximas de los gráficos de complementos de DSP son de 38 píxeles de ancho y de 14 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="24561-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="24561-132">La secuencia de bytes **IStream** que contiene el gráfico de Estado debe incluir información de encabezado.</span><span class="sxs-lookup"><span data-stu-id="24561-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="24561-133">Sin información de encabezado, Windows Media Player no puede identificar correctamente el tipo de gráfico y, por lo tanto, no cargará la imagen.</span><span class="sxs-lookup"><span data-stu-id="24561-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24561-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="24561-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24561-135">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="24561-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




