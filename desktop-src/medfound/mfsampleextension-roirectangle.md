---
description: Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720490"
---
# <a name="mfsampleextension_roirectangle-attribute"></a><span data-ttu-id="3897f-103">\_Atributo ROIRectangle de MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="3897f-103">MFSampleExtension\_ROIRectangle attribute</span></span>

<span data-ttu-id="3897f-104">Especifica los límites de la región de interés que indica la región del marco que requiere una calidad diferente.</span><span class="sxs-lookup"><span data-stu-id="3897f-104">Specifies the bounds of the region of interest which indicates the region of the frame that requires different quality.</span></span>

## <a name="data-type"></a><span data-ttu-id="3897f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3897f-105">Data type</span></span>

<span data-ttu-id="3897f-106">**[**ROI \_ ÁREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** almacenada como **BLOB**</span><span class="sxs-lookup"><span data-stu-id="3897f-106">**[**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** stored as **BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="3897f-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3897f-107">Remarks</span></span>

<span data-ttu-id="3897f-108">Después de configurar correctamente [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) en un valor distinto de cero en un MFT del codificador, la aplicación puede establecer este atributo en los ejemplos de entrada y esperar que se respete.</span><span class="sxs-lookup"><span data-stu-id="3897f-108">After successfully setting [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) to a non-zero value on an encoder MFT, the application can set this attribute on input samples and expect it to be honored.</span></span>

<span data-ttu-id="3897f-109">Si [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) no se establece en un valor distinto de cero, el \_ atributo MFSampleExtension ROIRectangle se omite en los ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="3897f-109">If [CODECAPI\_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) is not set to a non-zero value, the MFSampleExtension\_ROIRectangle attribute is ignored on input samples.</span></span>

<span data-ttu-id="3897f-110">MFSampleExtension \_ ROIRectangle se establece en una muestra de entrada y solo se aplica al ejemplo de entrada actual.</span><span class="sxs-lookup"><span data-stu-id="3897f-110">MFSampleExtension\_ROIRectangle is set on an input sample and is only applied to the current input sample.</span></span>

<span data-ttu-id="3897f-111">El campo **QPDelta** de la estructura de [**\_ área de ROI**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) especifica el delta del parámetro de cuantificación para la región especificada desde el resto del marco.</span><span class="sxs-lookup"><span data-stu-id="3897f-111">The **QPDelta** field on the [**ROI\_AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) structure specifies the quantization parameter delta for the specified region from the rest of the frame.</span></span> <span data-ttu-id="3897f-112">Si **QPDelta** es positivo, indica que la aplicación desea que el rectángulo tenga una calidad inferior que el resto del marco.</span><span class="sxs-lookup"><span data-stu-id="3897f-112">If **QPDelta** is positive, this indicates the application wants the rectangle to have lower quality than the rest of the frame.</span></span>

<span data-ttu-id="3897f-113">**Codificadores H. 264/AVC:** **QPDelta** debe estar entre \[ -25, + 25 \] .</span><span class="sxs-lookup"><span data-stu-id="3897f-113">**H.264/AVC encoders:** **QPDelta** shall be between \[-25, +25\].</span></span> <span data-ttu-id="3897f-114">El codificador garantizará que la QP final esté en un intervalo válido para el estándar de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3897f-114">The encoder shall ensure that the final QP is in a valid range for the video standard.</span></span>

<span data-ttu-id="3897f-115">No es necesario que la región especificada sea de MB alineada.</span><span class="sxs-lookup"><span data-stu-id="3897f-115">The specified region is not required to be MB aligned.</span></span> <span data-ttu-id="3897f-116">Los codificadores tienen flexibilidad para decidir el límite real.</span><span class="sxs-lookup"><span data-stu-id="3897f-116">Encoders have flexibility to decide the actual boundary.</span></span> <span data-ttu-id="3897f-117">Se recomienda cubrir toda la región especificada.</span><span class="sxs-lookup"><span data-stu-id="3897f-117">It is recommended to cover the entire specified region.</span></span>

## <a name="requirements"></a><span data-ttu-id="3897f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3897f-118">Requirements</span></span>



| <span data-ttu-id="3897f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3897f-119">Requirement</span></span> | <span data-ttu-id="3897f-120">Value</span><span class="sxs-lookup"><span data-stu-id="3897f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3897f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3897f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3897f-122">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="3897f-122">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="3897f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3897f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3897f-124">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3897f-124">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3897f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3897f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3897f-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3897f-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3897f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3897f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3897f-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3897f-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




