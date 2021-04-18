---
description: Especifica qué secuencias se conectaron correctamente a un receptor de medios.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Propiedad MFP_PKEY_StreamRenderingResults (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360384"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="35177-103">MFP \_ PKEY \_ propiedad StreamRenderingResults</span><span class="sxs-lookup"><span data-stu-id="35177-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35177-104">En desuso.</span><span class="sxs-lookup"><span data-stu-id="35177-104">Deprecated.</span></span> <span data-ttu-id="35177-105">Esta API se puede quitar de las versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="35177-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="35177-106">Las aplicaciones deben usar la [sesión multimedia](media-session.md) para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="35177-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="35177-107">Especifica qué secuencias se conectaron correctamente a un receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="35177-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="35177-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="35177-108">Data type</span></span>

<span data-ttu-id="35177-109">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="35177-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="35177-110">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="35177-110">PROPVARIANT member</span></span>

<span data-ttu-id="35177-111">Matriz de valores **DWORD** (**caul**)</span><span class="sxs-lookup"><span data-stu-id="35177-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="35177-112">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="35177-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="35177-113">**caul**</span><span class="sxs-lookup"><span data-stu-id="35177-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="35177-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35177-114">Remarks</span></span>

<span data-ttu-id="35177-115">Esta propiedad se puede enviar con el evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** .</span><span class="sxs-lookup"><span data-stu-id="35177-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="35177-116">El valor de la propiedad es una matriz de **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="35177-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="35177-117">Las entradas de la matriz corresponden a las secuencias del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="35177-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="35177-118">Cada entrada de la matriz indica si la secuencia correspondiente se conectó a un receptor de medios, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="35177-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="35177-119">Si la secuencia está conectada a un receptor de medios, el valor es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="35177-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="35177-120">Si la secuencia no está seleccionada, el valor es **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="35177-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="35177-121">Si se produjo un error al intentar conectar el flujo, el valor es un código de error.</span><span class="sxs-lookup"><span data-stu-id="35177-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="35177-122">Si al menos una secuencia se conectó correctamente, es posible la reproducción.</span><span class="sxs-lookup"><span data-stu-id="35177-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="35177-123">Por ejemplo, el usuario podría tener el códec necesario para reproducir la secuencia de audio, pero no reproducir la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="35177-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="35177-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35177-124">Requirements</span></span>



| <span data-ttu-id="35177-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="35177-125">Requirement</span></span> | <span data-ttu-id="35177-126">Value</span><span class="sxs-lookup"><span data-stu-id="35177-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35177-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35177-127">Minimum supported client</span></span><br/> | <span data-ttu-id="35177-128">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="35177-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35177-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35177-129">Minimum supported server</span></span><br/> | <span data-ttu-id="35177-130">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35177-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35177-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35177-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="35177-132"><dt>Mfplay. h</dt></span><span class="sxs-lookup"><span data-stu-id="35177-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35177-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="35177-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35177-134">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35177-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="35177-135">**\_MEDIAITEM el \_ \_ evento set de MFP**</span><span class="sxs-lookup"><span data-stu-id="35177-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




