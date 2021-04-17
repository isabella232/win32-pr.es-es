---
description: Controla la señalización de MFSampleExtension \_ MeanAbsoluteDifference a través de IMFAttribute en cada ejemplo de salida.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Propiedad CODECAPI_AVEncVideoMeanAbsoluteDifference (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696171"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="ea1fe-103">\_Propiedad AVEncVideoMeanAbsoluteDifference de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="ea1fe-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="ea1fe-104">Controla la señalización de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a través de [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) en cada ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="ea1fe-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ea1fe-105">Data type</span></span>

<span data-ttu-id="ea1fe-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="ea1fe-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ea1fe-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="ea1fe-107">Property GUID</span></span>

<span data-ttu-id="ea1fe-108">**CODECAPI \_ AVEncVideoMeanAbsoluteDifference**</span><span class="sxs-lookup"><span data-stu-id="ea1fe-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1fe-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ea1fe-109">Remarks</span></span>

<span data-ttu-id="ea1fe-110">Si la aplicación establece un valor distinto de cero, el codificador debería agregar el atributo de ejemplo [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) a cada ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="ea1fe-111">El \_ atributo MeanAbsoluteDifference de MFSampleExtension indica la diferencia absoluta media entre los ejemplos de origen y los ejemplos de predicción en el plano y.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="ea1fe-112">Si el codificador devuelve 0 para **GetParameterRange**, el codificador no admite la salida de [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) en los ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="ea1fe-113">El valor predeterminado debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="ea1fe-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1fe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea1fe-114">Requirements</span></span>



| <span data-ttu-id="ea1fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea1fe-115">Requirement</span></span> | <span data-ttu-id="ea1fe-116">Value</span><span class="sxs-lookup"><span data-stu-id="ea1fe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1fe-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea1fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1fe-118">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ea1fe-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ea1fe-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea1fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1fe-120">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea1fe-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea1fe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea1fe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1fe-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1fe-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1fe-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ea1fe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1fe-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea1fe-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




