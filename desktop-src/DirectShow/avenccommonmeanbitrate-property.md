---
description: Especifica la velocidad media de bits codificada, en bits por segundo. Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Propiedad AVEncCommonMeanBitRate (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4eaec7fc6578e6e69a45616ee6de059bb7a378b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538007"
---
# <a name="avenccommonmeanbitrate-property"></a><span data-ttu-id="94f77-104">Propiedad AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="94f77-104">AVEncCommonMeanBitRate property</span></span>

<span data-ttu-id="94f77-105">Especifica la velocidad media de bits codificada, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="94f77-105">Specifies the average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="94f77-106">Esta propiedad solo se aplica a los modos de codificación de velocidad de bits constante (CBR) y de velocidad de bits variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="94f77-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="94f77-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="94f77-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="94f77-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="94f77-108">Data type</span></span>

<span data-ttu-id="94f77-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="94f77-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="94f77-110">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="94f77-110">Property GUID</span></span>

<span data-ttu-id="94f77-111">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="94f77-111">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="94f77-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="94f77-112">Property value</span></span>

<span data-ttu-id="94f77-113">Los codificadores pueden implementar esta propiedad como un conjunto enumerado o como un intervalo lineal.</span><span class="sxs-lookup"><span data-stu-id="94f77-113">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="94f77-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94f77-114">Remarks</span></span>

<span data-ttu-id="94f77-115">Esta propiedad también se usa con [codificadores de cámara H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="94f77-115">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="94f77-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94f77-116">Requirements</span></span>



| <span data-ttu-id="94f77-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="94f77-117">Requirement</span></span> | <span data-ttu-id="94f77-118">Value</span><span class="sxs-lookup"><span data-stu-id="94f77-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94f77-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94f77-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94f77-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]</span><span class="sxs-lookup"><span data-stu-id="94f77-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="94f77-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94f77-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94f77-122">Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]</span><span class="sxs-lookup"><span data-stu-id="94f77-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="94f77-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94f77-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="94f77-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="94f77-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94f77-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="94f77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94f77-126">Propiedades de la API de códec</span><span class="sxs-lookup"><span data-stu-id="94f77-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="94f77-127">**Interfaz ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="94f77-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

