---
description: Transformaciones de preprocesamiento del descodificador de MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformaciones de preprocesamiento del descodificador de MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806440"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="52ad1-103">Transformaciones de preprocesamiento del descodificador de MPEG</span><span class="sxs-lookup"><span data-stu-id="52ad1-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="52ad1-104">**Panorámica y PanScan**</span><span class="sxs-lookup"><span data-stu-id="52ad1-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="52ad1-105">Para formar la imagen 4x3, puede rellenar la parte superior e inferior de la imagen (denominada imagen de pantalla ancha) o bien extraer una parte 4x3 de la imagen (denominada imagen de PanScan).</span><span class="sxs-lookup"><span data-stu-id="52ad1-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="52ad1-106">Los menús y los flujos de subimagens se superpondrán encima de la imagen de vídeo final.</span><span class="sxs-lookup"><span data-stu-id="52ad1-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="52ad1-107">Las imágenes de proporción de 16x9 se almacenan en un formato de 4x3 anamorphic.</span><span class="sxs-lookup"><span data-stu-id="52ad1-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="52ad1-108">La expansión del vídeo de origen de la relación de aspecto de anamorphic 4x3 720 x 480 a una relación de aspecto 16x9 forma la imagen de aspecto 16x9 original.</span><span class="sxs-lookup"><span data-stu-id="52ad1-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="52ad1-109">A continuación se muestra una descripción de cómo mostrar correctamente cada uno de los modos y sus aspectos destacados:</span><span class="sxs-lookup"><span data-stu-id="52ad1-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="52ad1-110">**Pantalla panorámica:** El vídeo de origen se expande en el área 16x9 más grande de la ventana de salida.</span><span class="sxs-lookup"><span data-stu-id="52ad1-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="52ad1-111">Los resaltados son relativos al interior del área 16x9.</span><span class="sxs-lookup"><span data-stu-id="52ad1-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="52ad1-112">Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 16x9.</span><span class="sxs-lookup"><span data-stu-id="52ad1-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="52ad1-113">**Examen panorámico:** En el vídeo 16x9, use el desplazamiento horizontal proporcionado en el flujo de MPEG2 para extraer una subventana de 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="52ad1-114">Coloque la subventana 4x3 en el área 4x3 mayor de la ventana del cliente de salida.</span><span class="sxs-lookup"><span data-stu-id="52ad1-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="52ad1-115">Las coordenadas del resaltado son relativas a la ventana de salida de 4x3 y no tienen ninguna relación con el vídeo de 16x9 de origen.</span><span class="sxs-lookup"><span data-stu-id="52ad1-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="52ad1-116">Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="52ad1-117">**Panorámica:** Calcule el área 4x3 más grande de la ventana de salida.</span><span class="sxs-lookup"><span data-stu-id="52ad1-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="52ad1-118">Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="52ad1-119">El vídeo de 4x3 de anamorphic de origen (que representa una imagen 16x9) se coloca en la subventana 16x9 más grande dentro del área 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="52ad1-120">Las barras negras se deben agregar a la parte superior e inferior de la subventana para mantener un área 16x9.</span><span class="sxs-lookup"><span data-stu-id="52ad1-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="52ad1-121">Las coordenadas del resaltado son relativas al área 4x3 y no tienen ninguna relación con el vídeo de 16x9 de origen.</span><span class="sxs-lookup"><span data-stu-id="52ad1-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="52ad1-122">Es posible que un disco especifique un resaltado que se encuentra fuera del área 16x9 (pero aún en la ventana 4x3).</span><span class="sxs-lookup"><span data-stu-id="52ad1-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="52ad1-123">En el caso de 4x3 video, el vídeo se coloca en el área de salida 4x3 más grande de la ventana del cliente de salida.</span><span class="sxs-lookup"><span data-stu-id="52ad1-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="52ad1-124">Las barras negras deben agregarse a la parte superior e inferior, o a los lados, para mantener un área 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="52ad1-125">**Preprocesamiento de MPEG con DVD Navigator y VMR**</span><span class="sxs-lookup"><span data-stu-id="52ad1-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="52ad1-126">Actualmente, se pasa al descodificador un \_ tipo de medio de vídeo MPEG2 de formato \_ (cuyo bloque de formato apunta a una estructura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ).</span><span class="sxs-lookup"><span data-stu-id="52ad1-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="52ad1-127">En los clavijas de salida, el descodificador genera un formato \_ VideoInfo2 tipo de medio, cuyo bloque Format apunta a una estructura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="52ad1-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="52ad1-128">Se ha cambiado el nombre del campo **dwReserved** de la estructura a marcas **dwControls** .</span><span class="sxs-lookup"><span data-stu-id="52ad1-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="52ad1-129">El miembro **dwControlFlags** contendrá ahora los nuevos bits.</span><span class="sxs-lookup"><span data-stu-id="52ad1-129">The **dwControlFlags** member will now contain the new bits.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="52ad1-130">AMCONTROL \_ usado</span><span class="sxs-lookup"><span data-stu-id="52ad1-130">AMCONTROL\_USED</span></span>          | <span data-ttu-id="52ad1-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="52ad1-131">0x00000001</span></span> |
| <span data-ttu-id="52ad1-132">AMCONTROL \_ Pad \_ a \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="52ad1-132">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="52ad1-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="52ad1-133">0x00000002</span></span> |
| <span data-ttu-id="52ad1-134">AMCONTROL \_ Pad \_ a \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="52ad1-134">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="52ad1-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="52ad1-135">0x00000004</span></span> |



 

<span data-ttu-id="52ad1-136">AMCONTROL \_ Used se usa para comprobar si se admiten estas nuevas marcas.</span><span class="sxs-lookup"><span data-stu-id="52ad1-136">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="52ad1-137">Un filtro de origen debe establecer la \_ marca AMCONTROL Used y ver si QueryAccept (mediatype) se realiza correctamente en el PIN de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="52ad1-137">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="52ad1-138">Si se rechaza, no se pueden usar las marcas AMCONTROL y dwReserved1 debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="52ad1-138">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="52ad1-139">AMCONTROL \_ Pad \_ to \_ 4x3 indica que la imagen se debe rellenar y mostrar en un área de 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-139">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="52ad1-140">AMCONTROL \_ Pad \_ to \_ 16x9 indica que la imagen se debe rellenar y mostrar en un área de 16x9.</span><span class="sxs-lookup"><span data-stu-id="52ad1-140">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="52ad1-141">El descodificador debe copiar o procesar ciegamente los bits.</span><span class="sxs-lookup"><span data-stu-id="52ad1-141">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="52ad1-142">Si el descodificador realiza la panorámica, debe modificar la relación de aspecto de los píxeles, rellenar la imagen y quitar los bits AMCONTROL correspondientes \_ \* .</span><span class="sxs-lookup"><span data-stu-id="52ad1-142">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="52ad1-143">MPEG2VIDEOINFO. dwFlags contiene ahora tres marcas para controlar el modo en que se debe mostrar el contenido:</span><span class="sxs-lookup"><span data-stu-id="52ad1-143">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="52ad1-144">`AMMPEG2_DoPanScan (0x00000001)`: Si se establece esta marca, el descodificador de vídeo MPEG-2 debe recortar la imagen de salida basada en vectores de recorrido panorámico en la extensión de presentación de imágenes \_ \_ y cambiar la relación de aspecto de la imagen a 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-144">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="52ad1-145">VMR no debe recibir un ejemplo 16x9 con esta marca.</span><span class="sxs-lookup"><span data-stu-id="52ad1-145">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="52ad1-146">Una implementación sencilla podría modificar el rectángulo de origen para indicar una región de origen de 540 de ancho con un borde izquierdo igual al desplazamiento de visualización de la extensión de presentación de imágenes \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="52ad1-146">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="52ad1-147">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: Cuando un descodificador de hardware muestra este flujo en una salida de vídeo (normalmente un conector de SVIDEO en la tarjeta), debe aplicar las reglas para mostrar un ejemplo de 16x9 en una pantalla de 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-147">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="52ad1-148">Un descodificador de software (o un descodificador de hardware que genera una salida enviada a la VMR) tiene dos opciones al procesar imágenes:</span><span class="sxs-lookup"><span data-stu-id="52ad1-148">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="52ad1-149">Omitir esta marca y pasar el contenido de VideoInfoHeader2 a VMR (la \_ marca de AMCONTROL \_ a \_ 4x3 ya se establecerá mediante el [navegador de DVD](dvd-navigator-filter.md) en el ejemplo).</span><span class="sxs-lookup"><span data-stu-id="52ad1-149">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="52ad1-150">El VMR encontrará un ejemplo de vídeo 16x9 con el panel de AMCONTROL \_ \_ en el \_ marcador de 4x3 establecido y una secuencia de subimagen de 4x3.</span><span class="sxs-lookup"><span data-stu-id="52ad1-150">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="52ad1-151">La aplicación debe establecer los rectángulos de destino normalizados de salida de los dos flujos para que tengan el mismo ancho.</span><span class="sxs-lookup"><span data-stu-id="52ad1-151">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="52ad1-152">Convierta el flujo anamorphic en una imagen de 4x3. para ello, rellene la parte superior e inferior de la imagen y establezca la relación de aspecto de la imagen en 4x3 (vea la panorámica anterior) y quite el \_ panel \_ de AMCONTROL \_ de 4X3 bit del VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="52ad1-152">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="52ad1-153">Los descodificadores de DirectXVA que combinan el vídeo y las secuencias de subimagen tendrán que procesar esta marca.</span><span class="sxs-lookup"><span data-stu-id="52ad1-153">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="52ad1-154">Si el hardware no puede escalar la subimagen combinada, el descodificador debe generar una secuencia de subimagen independiente para que la VMR se fusione con el vídeo.</span><span class="sxs-lookup"><span data-stu-id="52ad1-154">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="52ad1-155">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: Cuando un descodificador de hardware muestra esta secuencia en una salida de vídeo (normalmente un conector de SVIDEO en la tarjeta), debe suponer una presentación de 16x9 (anamorphic).</span><span class="sxs-lookup"><span data-stu-id="52ad1-155">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="52ad1-156">Un descodificador de software (o un descodificador de hardware que genera una salida enviada a la VMR) tiene dos opciones al procesar una imagen de anamorphic:</span><span class="sxs-lookup"><span data-stu-id="52ad1-156">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="52ad1-157">Omita esta marca y copie el contenido de VideoInfoHeader2 en VMR.</span><span class="sxs-lookup"><span data-stu-id="52ad1-157">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="52ad1-158">La VMR rellenará las imágenes de 4x3 en 16x9 si tienen el \_ Panel AMCONTROL \_ en \_ 16x9 establecido.</span><span class="sxs-lookup"><span data-stu-id="52ad1-158">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="52ad1-159">Rellene la imagen de salida a una imagen de 16x9 y quite el panel de AMCONTROL \_ \_ a \_ 16x9 bit.</span><span class="sxs-lookup"><span data-stu-id="52ad1-159">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="52ad1-160">La mayoría de los descodificadores deben usar **GetMediaType** para detectar un cambio de medios en el PIN de entrada y copiar el contenido de **VIDEOINFOHEADER2** (contenido en **MPEG2INFOHEADER**) en el terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="52ad1-160">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="52ad1-161">Probablemente solo procesarán el bit PanScan.</span><span class="sxs-lookup"><span data-stu-id="52ad1-161">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="52ad1-162">En el ejemplo de código siguiente se muestra cómo copiar el contenido de **VIDEOINFOHEADER2** de un PIN de entrada en un terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="52ad1-162">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


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



 

 



