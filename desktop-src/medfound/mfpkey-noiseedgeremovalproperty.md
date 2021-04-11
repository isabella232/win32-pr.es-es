---
description: Especifica si el códec debe intentar detectar bordes de fotogramas ruidosos y quitarlos.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Propiedad MFPKEY_NOISEEDGEREMOVAL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276314"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="ba832-103">\_Propiedad NOISEEDGEREMOVAL de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ba832-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="ba832-104">Especifica si el códec debe intentar detectar bordes de fotogramas ruidosos y quitarlos.</span><span class="sxs-lookup"><span data-stu-id="ba832-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ba832-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ba832-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ba832-106">g \_ wszWMVCNoiseEdgeRemoval</span><span class="sxs-lookup"><span data-stu-id="ba832-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="ba832-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ba832-107">Data Type</span></span>

<span data-ttu-id="ba832-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="ba832-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="ba832-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="ba832-109">Default Value</span></span>

<span data-ttu-id="ba832-110">false</span><span class="sxs-lookup"><span data-stu-id="ba832-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="ba832-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba832-111">Remarks</span></span>

<span data-ttu-id="ba832-112">Un borde de marco ruidoso suele ser el intervalo de espacio en blanco (VBI) vertical de un fotograma de televisión de difusión.</span><span class="sxs-lookup"><span data-stu-id="ba832-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="ba832-113">VBI son las 21 primeras líneas de análisis del fotograma de televisión.</span><span class="sxs-lookup"><span data-stu-id="ba832-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="ba832-114">Estas líneas de análisis no contienen datos de vídeo, sino que contienen datos sobre la difusión.</span><span class="sxs-lookup"><span data-stu-id="ba832-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="ba832-115">Cuando una tarjeta de captura graba una señal de televisión, el VBI normalmente se quita del fotograma.</span><span class="sxs-lookup"><span data-stu-id="ba832-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="ba832-116">La detección y corrección de bordes ruidosos realizadas por el códec solo puede corregir un borde que tenga tres o menos líneas de ruido.</span><span class="sxs-lookup"><span data-stu-id="ba832-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="ba832-117">Si el vídeo capturado contiene más de tres líneas ruidosos, hay un problema con el hardware que se usa para capturar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="ba832-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="ba832-118">Si el códec está configurado para quitar bordes ruidosos, duplica líneas adyacentes al borde ruidoso para rellenar el fotograma.</span><span class="sxs-lookup"><span data-stu-id="ba832-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba832-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba832-119">Requirements</span></span>



| <span data-ttu-id="ba832-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba832-120">Requirement</span></span> | <span data-ttu-id="ba832-121">Value</span><span class="sxs-lookup"><span data-stu-id="ba832-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba832-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba832-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ba832-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ba832-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ba832-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba832-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ba832-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba832-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba832-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba832-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba832-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba832-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba832-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba832-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba832-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba832-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




