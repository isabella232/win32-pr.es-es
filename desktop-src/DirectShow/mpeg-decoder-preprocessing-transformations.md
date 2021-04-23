---
description: Transformaciones de preprocesamiento del descodificador MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformaciones de preprocesamiento del descodificador MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908903"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="9a220-103">Transformaciones de preprocesamiento del descodificador MPEG</span><span class="sxs-lookup"><span data-stu-id="9a220-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="9a220-104">**Letterbox y PanScan**</span><span class="sxs-lookup"><span data-stu-id="9a220-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="9a220-105">La imagen de 4x3 se puede formar mediante el relleno de la parte superior e inferior de la imagen (denominada imagen letterbox) o mediante la extracción de una parte 4x3 de la imagen (denominada imagen de PanScan).</span><span class="sxs-lookup"><span data-stu-id="9a220-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="9a220-106">Los menús y las secuencias de subimagen se sobrelagen encima de la imagen de vídeo final.</span><span class="sxs-lookup"><span data-stu-id="9a220-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="9a220-107">Las imágenes de proporción de 16 x 9 se almacenan en un formato anamórfico de 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="9a220-108">La extensión del vídeo de origen anamórfico de relación de aspecto 4x3 de 720 x 480 a una relación de aspecto de 16 x 9 forma la imagen de aspecto original de 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="9a220-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="9a220-109">A continuación se muestra una descripción de cómo mostrar correctamente cada uno de los modos y sus aspectos destacados:</span><span class="sxs-lookup"><span data-stu-id="9a220-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="9a220-110">**Widescreen:** El vídeo de origen se extendió en el área más grande de 16 x 9 de la ventana de salida.</span><span class="sxs-lookup"><span data-stu-id="9a220-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="9a220-111">Los resaltados son relativos al interior del área 16x9.</span><span class="sxs-lookup"><span data-stu-id="9a220-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="9a220-112">Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="9a220-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="9a220-113">**Examen de panorámica:** En el vídeo de 16x9, use el desplazamiento horizontal proporcionado en la secuencia MPEG2 para extraer una subventana 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="9a220-114">Coloque la subventana 4x3 en el área 4x3 más grande de la ventana del cliente de salida.</span><span class="sxs-lookup"><span data-stu-id="9a220-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="9a220-115">Las coordenadas del resaltado son relativas a la ventana de salida 4x3 y no tienen ninguna relación con el vídeo de origen 16x9.</span><span class="sxs-lookup"><span data-stu-id="9a220-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="9a220-116">Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="9a220-117">**Cuadro de letras:** Calcule el área 4x3 más grande de la ventana de salida.</span><span class="sxs-lookup"><span data-stu-id="9a220-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="9a220-118">Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="9a220-119">El vídeo anamórfico de origen 4x3 (que representa una imagen de 16 x 9) se coloca en la subventana 16x9 más grande dentro del área 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="9a220-120">Las barras negras se deben agregar a la parte superior e inferior de la subventana para mantener un área de 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="9a220-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="9a220-121">Las coordenadas del resaltado son relativas al área 4x3 y no tienen ninguna relación con el vídeo de origen 16x9.</span><span class="sxs-lookup"><span data-stu-id="9a220-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="9a220-122">Es posible que un disco especifique un resaltado que se encuentra fuera del área 16x9 (pero todavía en la ventana 4x3).</span><span class="sxs-lookup"><span data-stu-id="9a220-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="9a220-123">Para el vídeo 4x3, el vídeo se coloca en el área de salida 4x3 más grande de la ventana del cliente de salida.</span><span class="sxs-lookup"><span data-stu-id="9a220-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="9a220-124">Las barras negras se deben agregar a la parte superior e inferior o a los lados para mantener un área de 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="9a220-125">**Preprocesamiento MPEG con DVD Navigator y VMR**</span><span class="sxs-lookup"><span data-stu-id="9a220-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="9a220-126">Actualmente, al descodificador se le pasa un tipo de medio FORMAT \_ MPEG2 \_ VIDEO (cuyo bloque de formato apunta a una [**estructura MPEG2VIDEOINFO).**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)</span><span class="sxs-lookup"><span data-stu-id="9a220-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="9a220-127">En los pines de salida, el descodificador genera un tipo de medio FORMAT VideoInfo2, cuyo bloque de formato apunta \_ a una [**estructura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="9a220-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="9a220-128">Se ha cambiado el nombre del **campo dwReserved de** la estructura a **marcas dwControls.**</span><span class="sxs-lookup"><span data-stu-id="9a220-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="9a220-129">El **miembro dwControlFlags** ahora contendrá los nuevos bits.</span><span class="sxs-lookup"><span data-stu-id="9a220-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="9a220-130">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="9a220-130">Label</span></span> | <span data-ttu-id="9a220-131">Value</span><span class="sxs-lookup"><span data-stu-id="9a220-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="9a220-132">AMCONTROL \_ USADO</span><span class="sxs-lookup"><span data-stu-id="9a220-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="9a220-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9a220-133">0x00000001</span></span> |
| <span data-ttu-id="9a220-134">AMCONTROL \_ PAD \_ TO \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="9a220-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="9a220-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9a220-135">0x00000002</span></span> |
| <span data-ttu-id="9a220-136">AMCONTROL \_ PAD \_ TO \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="9a220-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="9a220-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9a220-137">0x00000004</span></span> |



 

<span data-ttu-id="9a220-138">AMCONTROL \_ USED se usa para probar si se admiten estas nuevas marcas.</span><span class="sxs-lookup"><span data-stu-id="9a220-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="9a220-139">Un filtro de origen debe establecer la marca AMCONTROL USED y ver si QueryAccept(MediaType) se realiza correctamente \_ en la marca de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="9a220-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="9a220-140">Si se rechaza, no se pueden usar las marcas AMCONTROL y dwReserved1 debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="9a220-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="9a220-141">AMCONTROL PAD TO 4x3 indica que la imagen se debe agregar y \_ mostrar en un área de \_ \_ 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="9a220-142">AMCONTROL PAD TO 16x9 indica que la imagen se debe agregar y \_ mostrar en un área de \_ \_ 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="9a220-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="9a220-143">El descodificador debe copiar o procesar los bits de forma invidente.</span><span class="sxs-lookup"><span data-stu-id="9a220-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="9a220-144">Si el descodificador realiza la conversión de letras por sí mismo, debe modificar la relación de aspecto de los píxeles, agregar la imagen y quitar los bits de AMCONTROL \_ \* correspondientes.</span><span class="sxs-lookup"><span data-stu-id="9a220-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="9a220-145">MPEG2VIDEOINFO.dwFlags ahora contiene tres marcas para controlar cómo se debe mostrar el contenido:</span><span class="sxs-lookup"><span data-stu-id="9a220-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="9a220-146">`AMMPEG2_DoPanScan (0x00000001)`: si se establece esta marca, el descodificador de vídeo MPEG-2 debe recortar la imagen de salida en función de los vectores de examen pan en la extensión de visualización de imagen y cambiar la relación de aspecto de la imagen a \_ \_ 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="9a220-147">El VMR no debe recibir un ejemplo de 16 x 9 con esta marca.</span><span class="sxs-lookup"><span data-stu-id="9a220-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="9a220-148">Una implementación simple podría modificar el rectángulo de origen para indicar una región de origen de 540 anchos con un borde izquierdo igual al desplazamiento de presentación en la extensión de visualización \_ de \_ imagen.</span><span class="sxs-lookup"><span data-stu-id="9a220-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="9a220-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: cuando un descodificador de hardware muestra esta secuencia en una salida de vídeo (normalmente un conector SVIDEO en la tarjeta), debe aplicar las reglas para mostrar un ejemplo de 16x9 en una pantalla de 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="9a220-150">Un descodificador de software (o un descodificador de hardware que genera la salida enviada al VMR) tiene dos opciones al procesar imágenes:</span><span class="sxs-lookup"><span data-stu-id="9a220-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="9a220-151">Ignore esta marca y pase el contenido de VideoInfoHeader2 a VMR (la marca AMCONTROL \_ PAD \_ TO \_ 4x3 [](dvd-navigator-filter.md) ya la establecerá el navegador de DVD en el ejemplo).</span><span class="sxs-lookup"><span data-stu-id="9a220-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="9a220-152">El VMR encontrará un ejemplo de vídeo de 16 x 9 con la marca AMCONTROL PAD TO 4x3 establecida y una secuencia \_ \_ de \_ subapicture 4x3.</span><span class="sxs-lookup"><span data-stu-id="9a220-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="9a220-153">La aplicación debe establecer los rectángulos de destino normalizados de salida de las dos secuencias para que sean del mismo ancho.</span><span class="sxs-lookup"><span data-stu-id="9a220-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="9a220-154">Convierta la secuencia anamórfica en una imagen de 4x3 mediante el relleno de la parte superior e inferior de la imagen y el establecimiento de la relación de aspecto de la imagen en 4x3 (consulte Letterbox más arriba) y quitando el PANEL DE AMCONTROL a \_ \_ \_ 4x3 bits de VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="9a220-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="9a220-155">Los descodificadores de DirectXVA que mezclan los flujos de vídeo y subpicture tendrán que procesar esta marca.</span><span class="sxs-lookup"><span data-stu-id="9a220-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="9a220-156">Si el hardware no puede escalar la subaspección mezclada, el descodificador debe generar una secuencia de subimagen independiente para que vmr se mezcle con el vídeo.</span><span class="sxs-lookup"><span data-stu-id="9a220-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="9a220-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: cuando un descodificador de hardware muestra esta secuencia en una salida de vídeo (normalmente un conector SVIDEO en la tarjeta), debe suponer una pantalla 16x9 (anamórfica).</span><span class="sxs-lookup"><span data-stu-id="9a220-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="9a220-158">Un descodificador de software (o un descodificador de hardware que genera la salida enviada al VMR) tiene dos opciones al procesar una imagen anamórfica:</span><span class="sxs-lookup"><span data-stu-id="9a220-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="9a220-159">Ignore esta marca y copie el contenido de VideoInfoHeader2 en vmr.</span><span class="sxs-lookup"><span data-stu-id="9a220-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="9a220-160">La VMR va a usar imágenes de 4 x 3 a 16 x 9 si tienen establecido AMCONTROL \_ PAD \_ TO \_ 16x9.</span><span class="sxs-lookup"><span data-stu-id="9a220-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="9a220-161">Ajádala a una imagen de 16 x 9 y quite el PAD DE AMCONTROL \_ \_ A \_ 16 x 9 bits.</span><span class="sxs-lookup"><span data-stu-id="9a220-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="9a220-162">La mayoría de los descodificadores deben usar **GetMediaType** para detectar un cambio multimedia en el pin de entrada y copiar el contenido **de VIDEOINFOHEADER2** (incluido en **MPEG2INFOHEADER)** en el pin de salida.</span><span class="sxs-lookup"><span data-stu-id="9a220-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="9a220-163">Probablemente solo procesarán el bit PanScan.</span><span class="sxs-lookup"><span data-stu-id="9a220-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="9a220-164">En el código de ejemplo siguiente se muestra cómo copiar el contenido **de VIDEOINFOHEADER2** de un pin de entrada a un pin de salida.</span><span class="sxs-lookup"><span data-stu-id="9a220-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



