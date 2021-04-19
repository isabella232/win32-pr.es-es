---
description: Contiene datos de formato adicionales para un tipo de medio.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: MF_MT_USER_DATA atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716673"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="fd0bd-103">\_Atributo de \_ datos de usuario MF MT \_</span><span class="sxs-lookup"><span data-stu-id="fd0bd-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="fd0bd-104">Contiene datos de formato adicionales para un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd0bd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fd0bd-105">Data type</span></span>

<span data-ttu-id="fd0bd-106">Byte array</span><span class="sxs-lookup"><span data-stu-id="fd0bd-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="fd0bd-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd0bd-107">Remarks</span></span>

<span data-ttu-id="fd0bd-108">El significado de los datos de este atributo depende del formato descrito por el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="fd0bd-109">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="fd0bd-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="fd0bd-110">Datos de formato adicionales</span><span class="sxs-lookup"><span data-stu-id="fd0bd-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0bd-111">Códec de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="fd0bd-112">Datos privados del códec.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="fd0bd-113">Estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) convertida.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="fd0bd-114">Datos adicionales que aparecen después de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , sin incluir la tabla de colores o las máscaras de color.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="fd0bd-115">Se ha convertido la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fd0bd-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="fd0bd-116">Datos adicionales que aparecen después de la estructura de formato de audio.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="fd0bd-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fd0bd-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0bd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd0bd-118">Requirements</span></span>



| <span data-ttu-id="fd0bd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd0bd-119">Requirement</span></span> | <span data-ttu-id="fd0bd-120">Value</span><span class="sxs-lookup"><span data-stu-id="fd0bd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0bd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd0bd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0bd-122">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="fd0bd-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="fd0bd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd0bd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0bd-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="fd0bd-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="fd0bd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd0bd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd0bd-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0bd-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0bd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd0bd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0bd-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd0bd-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd0bd-129">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="fd0bd-130">**IMFAttributes:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="fd0bd-131">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="fd0bd-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="fd0bd-132">Atributos de tipo de medio</span><span class="sxs-lookup"><span data-stu-id="fd0bd-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
