---
description: Combinación alfa
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Combinación alfa (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152565"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="34e3f-103">Combinación alfa (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="34e3f-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="34e3f-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="34e3f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="34e3f-105">En este artículo se describe la combinación alfa en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="34e3f-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="34e3f-106">Alfa mide la transparencia de un píxel o imagen.</span><span class="sxs-lookup"><span data-stu-id="34e3f-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="34e3f-107">En vídeo RGB sin comprimir de 32 bits, cuatro componentes definen cada píxel: un canal alfa (A) y tres componentes de color (RGB).</span><span class="sxs-lookup"><span data-stu-id="34e3f-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="34e3f-108">Un píxel con un valor alfa de cero es completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="34e3f-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="34e3f-109">Un píxel con un valor alfa de 255 es opaco.</span><span class="sxs-lookup"><span data-stu-id="34e3f-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="34e3f-110">Entre estos valores, el píxel tiene varios grados de transparencia.</span><span class="sxs-lookup"><span data-stu-id="34e3f-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="34e3f-111">DirectShow define dos tipos de medios para vídeo RGB de 32 bits:</span><span class="sxs-lookup"><span data-stu-id="34e3f-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="34e3f-112">**MEDIASUBTYPE \_ ARGB32**: el vídeo es RGB de 32 bits con un canal alfa válido.</span><span class="sxs-lookup"><span data-stu-id="34e3f-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="34e3f-113">**MEDIASUBTYPE \_ RGB32**: los píxeles son de 32 bits, pero el canal alfa no es necesariamente válido.</span><span class="sxs-lookup"><span data-stu-id="34e3f-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="34e3f-114">Para realizar la combinación alfa en DES, establezca el tipo de medio sin comprimir del grupo de vídeos en MEDIASUBTYPE \_ ARGB32.</span><span class="sxs-lookup"><span data-stu-id="34e3f-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="34e3f-115">En C++, llame al método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="34e3f-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="34e3f-116">En el formato XTL, al establecer el atributo [**bitdepth**](bitdepth-attribute.md) del elemento [**Group**](group-element.md) en 32 también se consigue esto.</span><span class="sxs-lookup"><span data-stu-id="34e3f-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="34e3f-117">A continuación, necesita datos de vídeo que contengan un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="34e3f-118">Hay varias opciones:</span><span class="sxs-lookup"><span data-stu-id="34e3f-118">There are several options:</span></span>

-   <span data-ttu-id="34e3f-119">Puede usar un archivo AVI que ya tiene vídeo RGB de 32 bits con datos alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="34e3f-120">Actualmente, no se admite Alpha para los archivos de código fuente MPEG o Microsoft Windows Media Format (WMF).</span><span class="sxs-lookup"><span data-stu-id="34e3f-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="34e3f-121">DES admite archivos de mapa de bits de 32 bits (. bmp) y Targa (. TGA) con datos alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="34e3f-122">Puede escribir un filtro de origen personalizado que cree datos RGB de 32 bits con alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="34e3f-123">El tipo de medio de salida debe ser **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="34e3f-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="34e3f-124">Use el filtro como el subobjeto en un objeto de origen de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="34e3f-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="34e3f-125">Si el origen de vídeo no tiene alfa, puede usar un efecto que cree datos alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="34e3f-126">El [efecto](alpha-setter-effect.md) establecedor alfa establece el canal alfa de la imagen completa en un valor constante.</span><span class="sxs-lookup"><span data-stu-id="34e3f-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="34e3f-127">Para variar el alfa a lo largo del tiempo, use la interfaz [**IPropertySetter**](ipropertysetter.md) con el efecto del establecedor alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="34e3f-128">El origen original no tiene que ser de 32 bits, siempre que el tipo de medio sin comprimir del grupo sea **MEDIASUBTYPE \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="34e3f-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="34e3f-129">Por último, pase el vídeo a un efecto o transición que realice la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="34e3f-130">La [transición del compositor](compositor-transition.md) realiza la combinación alfa y la transición de la [clave](key-transition.md) puede clave mediante el valor alfa.</span><span class="sxs-lookup"><span data-stu-id="34e3f-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="34e3f-131">En el siguiente proyecto de XTL de ejemplo se realiza la combinación alfa:</span><span class="sxs-lookup"><span data-stu-id="34e3f-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="34e3f-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34e3f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34e3f-133">Usar servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="34e3f-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



