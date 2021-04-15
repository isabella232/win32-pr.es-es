---
description: El descodificador de pantalla de Windows Media Video 9 descodifica los flujos codificados por el codificador de pantalla de Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Descodificador de pantalla de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708860"
---
# <a name="windows-media-video-9-screen-decoder"></a><span data-ttu-id="1e276-103">Descodificador de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1e276-103">Windows Media Video 9 Screen Decoder</span></span>

<span data-ttu-id="1e276-104">El descodificador de pantalla de Windows Media Video 9 descodifica los flujos codificados por el [**codificador de pantalla de Windows Media Video 9**](windowsmediavideo9screenencoder.md).</span><span class="sxs-lookup"><span data-stu-id="1e276-104">The Windows Media Video 9 Screen decoder decodes streams that were encoded by the [**Windows Media Video 9 Screen Encoder**](windowsmediavideo9screenencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1e276-105">Identificador de clase</span><span class="sxs-lookup"><span data-stu-id="1e276-105">Class Identifier</span></span>

<span data-ttu-id="1e276-106">El identificador de clase (CLSID) para el descodificador de pantalla de Windows Media Video 9 se representa mediante la constante **\_ CMSSCDecMediaObject de CLSID**.</span><span class="sxs-lookup"><span data-stu-id="1e276-106">The class identifier (CLSID) for the Windows Media Video 9 Screen decoder is represented by the constant **CLSID\_CMSSCDecMediaObject**.</span></span> <span data-ttu-id="1e276-107">Puede crear una instancia del descodificador llamando a **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1e276-107">You can create an instance of the decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="1e276-108">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="1e276-108">Input Types</span></span>

<span data-ttu-id="1e276-109">El código de cuatro caracteres (FOURCC) para el contenido codificado en pantalla de la versión 9 de Windows Media Video es "MSS2".</span><span class="sxs-lookup"><span data-stu-id="1e276-109">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="1e276-110">El descodificador de pantalla de la versión 9 admite los siguientes tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="1e276-110">The following input types are supported by the Version 9 Screen decoder.</span></span>

-   <span data-ttu-id="1e276-111">MEDIASUBTYPE \_ MSS2</span><span class="sxs-lookup"><span data-stu-id="1e276-111">MEDIASUBTYPE\_MSS2</span></span>

## <a name="output-types"></a><span data-ttu-id="1e276-112">Tipos de salida</span><span class="sxs-lookup"><span data-stu-id="1e276-112">Output Types</span></span>

<span data-ttu-id="1e276-113">El descodificador de pantalla de la versión 9 admite los siguientes tipos de salida cuando se usa como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="1e276-113">The following output types are supported by the Version 9 Screen decoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="1e276-114">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="1e276-114">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="1e276-115">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1e276-115">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="1e276-116">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="1e276-116">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="1e276-117">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1e276-117">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="1e276-118">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1e276-118">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="1e276-119">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1e276-119">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="1e276-120">El descodificador de pantalla de la versión 9 admite los siguientes tipos de salida cuando se utiliza como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="1e276-120">The following output types are supported by the Version 9 Screen decoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="1e276-121">MFVideoFormat \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="1e276-121">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="1e276-122">MFVideoFormat \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="1e276-122">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="1e276-123">MFVideoFormat \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="1e276-123">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="1e276-124">MFVideoFormat \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="1e276-124">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="1e276-125">MFVideoFormat \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="1e276-125">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="1e276-126">MFVideoFormat \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="1e276-126">MFVideoFormat\_RGB8</span></span>

## <a name="remarks"></a><span data-ttu-id="1e276-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e276-127">Remarks</span></span>

<span data-ttu-id="1e276-128">Un objeto de descodificador de pantalla expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto pueda usarse como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="1e276-128">A screen decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="1e276-129">Un descodificador de pantalla se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1e276-129">A screen decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="1e276-130">En la tabla siguiente se muestran las condiciones en las que un descodificador de pantalla se comporta como un DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="1e276-130">The following table shows the conditions under which a screen decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="1e276-131">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1e276-131">Operating system</span></span>            | <span data-ttu-id="1e276-132">Comportamiento del descodificador</span><span class="sxs-lookup"><span data-stu-id="1e276-132">Decoder behavior</span></span>                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e276-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e276-133">Windows XP</span></span>                  | <span data-ttu-id="1e276-134">Un descodificador de pantalla de Windows Media siempre se comporta como DMO.</span><span class="sxs-lookup"><span data-stu-id="1e276-134">A Windows Media Screen decoder always behaves as a DMO.</span></span>                                                                                                                 |
| <span data-ttu-id="1e276-135">Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e276-135">Windows Vista and Windows 7</span></span> | <span data-ttu-id="1e276-136">De forma predeterminada, un descodificador de pantalla de Windows Media se comporta como un DMO.</span><span class="sxs-lookup"><span data-stu-id="1e276-136">By default, a Windows Media Screen decoder behaves as a DMO.</span></span> <span data-ttu-id="1e276-137">Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de pantalla, se comporta como una MFT.</span><span class="sxs-lookup"><span data-stu-id="1e276-137">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a screen decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="1e276-138">Puede usar el mismo CLSID (CLSID \_ CMSSCDecMediaObject) para crear el descodificador de pantalla de la versión 7 y el descodificador de pantalla de la versión 9.</span><span class="sxs-lookup"><span data-stu-id="1e276-138">You can use the same CLSID (CLSID\_CMSSCDecMediaObject) to create the Version 7 Screen decoder and the Version 9 Screen decoder.</span></span> <span data-ttu-id="1e276-139">El FOURCC para el contenido codificado de la versión 7 de la pantalla Windows Media Video es "MSS1".</span><span class="sxs-lookup"><span data-stu-id="1e276-139">The FOURCC for Windows Media Video Screen Version 7 encoded content is "MSS1".</span></span> <span data-ttu-id="1e276-140">El descodificador de pantalla de la versión 7 admite el \_ tipo de entrada MSS1 de MEDIASUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="1e276-140">The Version 7 Screen decoder supports the MEDIASUBTYPE\_MSS1 input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e276-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e276-141">Requirements</span></span>



| <span data-ttu-id="1e276-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e276-142">Requirement</span></span> | <span data-ttu-id="1e276-143">Value</span><span class="sxs-lookup"><span data-stu-id="1e276-143">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e276-144">Remoto</span><span class="sxs-lookup"><span data-stu-id="1e276-144">Client</span></span><br/> | <span data-ttu-id="1e276-145">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e276-145">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="1e276-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e276-146">Header</span></span><br/> | <dl> <span data-ttu-id="1e276-147"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e276-147"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1e276-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e276-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="1e276-149"><dt>Wmvsdecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e276-149"><dt>Wmvsdecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e276-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e276-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e276-151">Objetos Codec</span><span class="sxs-lookup"><span data-stu-id="1e276-151">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1e276-152">Implementación de códecs</span><span class="sxs-lookup"><span data-stu-id="1e276-152">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="1e276-153">Usar el códec de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1e276-153">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="1e276-154">Codificador de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="1e276-154">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
