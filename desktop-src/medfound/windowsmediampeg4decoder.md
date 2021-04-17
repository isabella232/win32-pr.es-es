---
description: El descodificador MPEG4 v1/v2 de Windows Media descodifica transmisiones de vídeo MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Descodificador MPEG4 v1/v2 de Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717343"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a><span data-ttu-id="68cd2-103">Descodificador MPEG4 v1/v2 de Windows Media</span><span class="sxs-lookup"><span data-stu-id="68cd2-103">Windows Media MPEG4 V1/V2 Decoder</span></span>

<span data-ttu-id="68cd2-104">El descodificador MPEG4 v1/v2 de Windows Media descodifica transmisiones de vídeo MPEG4 v1/v2.</span><span class="sxs-lookup"><span data-stu-id="68cd2-104">The Windows Media MPEG4 V1/V2 decoder decodes MPEG4 V1/V2 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="68cd2-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="68cd2-105">Class Identifier</span></span>

<span data-ttu-id="68cd2-106">El identificador de clase (CLSID) del descodificador MPEG4 v1/v2 de Windows Media se representa mediante la constante **\_ CMpeg4DecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="68cd2-106">The class identifier (CLSID) for the Windows Media MPEG4 V1/V2 decoder is represented by the constant **CLSID\_CMpeg4DecMediaObject**.</span></span> <span data-ttu-id="68cd2-107">Puede crear una instancia del descodificador MPEG4 v1/v2 llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="68cd2-107">You can create an instance of the MPEG4 V1/V2 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="68cd2-108">Formatos</span><span class="sxs-lookup"><span data-stu-id="68cd2-108">Formats</span></span>

<span data-ttu-id="68cd2-109">El descodificador MPEG4 v1/v2 de Windows Media admite los siguientes tipos de medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="68cd2-109">The Windows Media MPEG4 V1/V2 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="68cd2-110">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="68cd2-110">MEDIASUBTYPE\_MPG4</span></span>
-   <span data-ttu-id="68cd2-111">MEDIASUBTYPE \_ MPG4</span><span class="sxs-lookup"><span data-stu-id="68cd2-111">MEDIASUBTYPE\_mpg4</span></span>
-   <span data-ttu-id="68cd2-112">MEDIASUBTYPE \_ mp42</span><span class="sxs-lookup"><span data-stu-id="68cd2-112">MEDIASUBTYPE\_MP42</span></span>
-   <span data-ttu-id="68cd2-113">MEDIASUBTYPE \_ mp42</span><span class="sxs-lookup"><span data-stu-id="68cd2-113">MEDIASUBTYPE\_mp42</span></span>

<span data-ttu-id="68cd2-114">El descodificador MPEG4 v1/v2 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="68cd2-114">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="68cd2-115">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="68cd2-115">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="68cd2-116">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="68cd2-116">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="68cd2-117">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="68cd2-117">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="68cd2-118">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="68cd2-118">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="68cd2-119">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="68cd2-119">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="68cd2-120">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="68cd2-120">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="68cd2-121">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="68cd2-121">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="68cd2-122">El descodificador MPEG4 v1/v2 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="68cd2-122">The Windows Media MPEG4 V1/V2 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="68cd2-123">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="68cd2-123">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="68cd2-124">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="68cd2-124">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="68cd2-125">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="68cd2-125">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="68cd2-126">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="68cd2-126">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="68cd2-127">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="68cd2-127">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="68cd2-128">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="68cd2-128">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="68cd2-129">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="68cd2-129">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="68cd2-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68cd2-130">Remarks</span></span>

<span data-ttu-id="68cd2-131">El objeto descodificador MPEG4 v1/v2 de Windows Media expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="68cd2-131">The Windows Media MPEG4 V1/V2 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="68cd2-132">El objeto tiene el mismo identificador de clase (CLSID) independientemente de si actúa como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="68cd2-132">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="68cd2-133">Un descodificador MPEG4 v1/v2 se comporta como un DMO o una MFT en función de las interfaces que se obtengan y de la versión de Windows que se esté ejecutando.</span><span class="sxs-lookup"><span data-stu-id="68cd2-133">An MPEG4 V1/V2 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="68cd2-134">En la tabla siguiente se muestran las condiciones en las que un descodificador MPEG4 v1/v2 se comporta como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="68cd2-134">The following table shows the conditions under which an MPEG4 V1/V2 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="68cd2-135">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="68cd2-135">Operating system</span></span>            | <span data-ttu-id="68cd2-136">Comportamiento del descodificador</span><span class="sxs-lookup"><span data-stu-id="68cd2-136">Decoder behavior</span></span>                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68cd2-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="68cd2-137">Windows XP</span></span>                  | <span data-ttu-id="68cd2-138">Un descodificador MPEG4 v1/v2 siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="68cd2-138">An MPEG4 V1/V2 decoder always behaves as a DMO.</span></span>                                                                                                                                 |
| <span data-ttu-id="68cd2-139">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="68cd2-139">Windows Vista and Windows 7</span></span> | <span data-ttu-id="68cd2-140">De forma predeterminada, un descodificador MPEG4 v1/v2 se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="68cd2-140">By default, an MPEG4 V1/V2 decoder behaves as a DMO.</span></span> <span data-ttu-id="68cd2-141">Si obtiene una interfaz de [GUID de subtipo de vídeo](video-subtype-guids.md) en un descodificador MPEG4 v1/v2, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="68cd2-141">If you obtain an [Video Subtype GUIDs](video-subtype-guids.md) interface on an MPEG4 V1/V2 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="68cd2-142">Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un descodificador actúa como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="68cd2-142">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="68cd2-143">Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un descodificador actúa como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="68cd2-143">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="68cd2-144">Para obtener información sobre los GUID que representan subtipos de vídeo, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="68cd2-144">For information about the GUIDs that represent video subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68cd2-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68cd2-145">Requirements</span></span>



| <span data-ttu-id="68cd2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="68cd2-146">Requirement</span></span> | <span data-ttu-id="68cd2-147">Value</span><span class="sxs-lookup"><span data-stu-id="68cd2-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68cd2-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68cd2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="68cd2-149">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="68cd2-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="68cd2-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68cd2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="68cd2-151">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="68cd2-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="68cd2-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68cd2-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="68cd2-153"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68cd2-153"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="68cd2-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68cd2-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68cd2-155"><dt>MPG4DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68cd2-155"><dt>MPG4DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68cd2-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="68cd2-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68cd2-157">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="68cd2-157">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
