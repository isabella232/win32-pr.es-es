---
description: El descodificador MPEG-4 V3 de Windows Media descodifica secuencias de vídeo MPEG-4 V3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Descodificador MPEG-4 V3 de Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717359"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a><span data-ttu-id="91a44-103">Descodificador MPEG-4 V3 de Windows Media</span><span class="sxs-lookup"><span data-stu-id="91a44-103">Windows Media MPEG-4 V3 Decoder</span></span>

<span data-ttu-id="91a44-104">El descodificador MPEG-4 V3 de Windows Media descodifica secuencias de vídeo MPEG-4 V3.</span><span class="sxs-lookup"><span data-stu-id="91a44-104">The Windows Media MPEG-4 V3 decoder decodes MPEG-4 V3 video streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="91a44-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="91a44-105">Class Identifier</span></span>

<span data-ttu-id="91a44-106">El identificador de clase (CLSID) del descodificador MPEG-4 V3 de Windows se representa mediante la constante **\_ CMpeg43DecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="91a44-106">The class identifier (CLSID) for the Windows MPEG-4 V3 decoder is represented by the constant **CLSID\_CMpeg43DecMediaObject**.</span></span> <span data-ttu-id="91a44-107">Puede crear una instancia del descodificador MPEG-4 V3 llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="91a44-107">You can create an instance of the MPEG-4 V3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="formats"></a><span data-ttu-id="91a44-108">Formatos</span><span class="sxs-lookup"><span data-stu-id="91a44-108">Formats</span></span>

<span data-ttu-id="91a44-109">El descodificador MPEG-4 V3 de Windows Media admite los siguientes tipos de medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="91a44-109">The Windows Media MPEG-4 V3 decoder supports the following input media types.</span></span>

-   <span data-ttu-id="91a44-110">MEDIASUBTYPE \_ mp43</span><span class="sxs-lookup"><span data-stu-id="91a44-110">MEDIASUBTYPE\_MP43</span></span>
-   <span data-ttu-id="91a44-111">MEDIASUBTYPE \_ mp43</span><span class="sxs-lookup"><span data-stu-id="91a44-111">MEDIASUBTYPE\_mp43</span></span>

<span data-ttu-id="91a44-112">El descodificador MPEG-4 V3 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="91a44-112">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="91a44-113">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="91a44-113">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="91a44-114">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="91a44-114">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="91a44-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="91a44-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="91a44-116">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="91a44-116">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="91a44-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="91a44-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="91a44-118">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="91a44-118">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="91a44-119">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="91a44-119">MEDIASUBTYPE\_RGB555</span></span>

<span data-ttu-id="91a44-120">El descodificador MPEG-4 V3 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="91a44-120">The Windows Media MPEG-4 V3 decoder supports the following output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="91a44-121">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="91a44-121">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="91a44-122">MFVideoFormat \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="91a44-122">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="91a44-123">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="91a44-123">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="91a44-124">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="91a44-124">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="91a44-125">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="91a44-125">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="91a44-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="91a44-126">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="91a44-127">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="91a44-127">MFVideoFormat\_RGB555</span></span>

## <a name="remarks"></a><span data-ttu-id="91a44-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91a44-128">Remarks</span></span>

<span data-ttu-id="91a44-129">El objeto descodificador MPEG-4 V3 de Windows Media expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="91a44-129">The Windows Media MPEG-4 V3 decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="91a44-130">El objeto tiene el mismo identificador de clase (CLSID) independientemente de si actúa como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="91a44-130">The object has the same class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span>

<span data-ttu-id="91a44-131">El descodificador MPEG-4 V3 se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="91a44-131">The MPEG-4 V3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="91a44-132">En la tabla siguiente se muestran las condiciones en las que un descodificador MPEG-4 V3 se comporta como DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="91a44-132">The following table shows the conditions under which an MPEG-4 V3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="91a44-133">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="91a44-133">Operating system</span></span>            | <span data-ttu-id="91a44-134">Comportamiento del descodificador</span><span class="sxs-lookup"><span data-stu-id="91a44-134">Decoder behavior</span></span>                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a44-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91a44-135">Windows XP</span></span>                  | <span data-ttu-id="91a44-136">El descodificador MPEG-4 V3 siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="91a44-136">The MPEG-4 V3 decoder always behaves as a DMO.</span></span>                                                                                                                      |
| <span data-ttu-id="91a44-137">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="91a44-137">Windows Vista and Windows 7</span></span> | <span data-ttu-id="91a44-138">De forma predeterminada, el descodificador MPEG-4 V3 se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="91a44-138">By default, the MPEG-4 V3 decoder behaves as a DMO.</span></span> <span data-ttu-id="91a44-139">Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en el descodificador MPEG-4 V3, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="91a44-139">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on the MPEG-4 V3 decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="91a44-140">Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un descodificador actúa como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="91a44-140">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="91a44-141">Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un descodificador actúa como un DMO o una MFT.</span><span class="sxs-lookup"><span data-stu-id="91a44-141">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="91a44-142">Para obtener información sobre los GUID que representan subtipos de medios, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="91a44-142">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91a44-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a44-143">Requirements</span></span>



| <span data-ttu-id="91a44-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a44-144">Requirement</span></span> | <span data-ttu-id="91a44-145">Value</span><span class="sxs-lookup"><span data-stu-id="91a44-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91a44-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91a44-146">Minimum supported client</span></span><br/> | <span data-ttu-id="91a44-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="91a44-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="91a44-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91a44-148">Minimum supported server</span></span><br/> | <span data-ttu-id="91a44-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91a44-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91a44-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91a44-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a44-151"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a44-151"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="91a44-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91a44-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91a44-153"><dt>MP43DECD.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91a44-153"><dt>MP43DECD.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a44-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="91a44-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a44-155">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="91a44-155">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
