---
description: Establece el número de subprocesos de trabajo usados por un descodificador de vídeo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Propiedad CODECAPI_AVDecNumWorkerThreads (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714938"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a><span data-ttu-id="587c9-103">\_Propiedad AVDecNumWorkerThreads de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="587c9-103">CODECAPI\_AVDecNumWorkerThreads property</span></span>

<span data-ttu-id="587c9-104">Establece el número de subprocesos de trabajo usados por un descodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="587c9-104">Sets the number of worker threads that are used by a video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="587c9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="587c9-105">Data type</span></span>

<span data-ttu-id="587c9-106">**Long** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="587c9-106">**LONG** (**VT\_I4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="587c9-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="587c9-107">Property GUID</span></span>

<span data-ttu-id="587c9-108">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="587c9-108">CODECAPI\_AVDecNumWorkerThreads</span></span>

## <a name="remarks"></a><span data-ttu-id="587c9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="587c9-109">Remarks</span></span>

<span data-ttu-id="587c9-110">Si el valor es 1, el descodificador selecciona el número de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="587c9-110">If the value is  1, the decoder selects the number of threads.</span></span>

<span data-ttu-id="587c9-111">Para la interfaz [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , establezca esta propiedad como un valor **Long** (**VT \_ I4**).</span><span class="sxs-lookup"><span data-stu-id="587c9-111">For the [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) interface, set this property as a **LONG** value (**VT\_I4**).</span></span> <span data-ttu-id="587c9-112">Para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , establezca esta propiedad como **UINT32**, aunque el valor es signed.</span><span class="sxs-lookup"><span data-stu-id="587c9-112">For the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, set this property as a **UINT32**, although the value is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="587c9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="587c9-113">Requirements</span></span>



| <span data-ttu-id="587c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="587c9-114">Requirement</span></span> | <span data-ttu-id="587c9-115">Value</span><span class="sxs-lookup"><span data-stu-id="587c9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="587c9-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="587c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="587c9-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="587c9-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="587c9-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="587c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="587c9-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="587c9-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="587c9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="587c9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="587c9-121"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="587c9-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="587c9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="587c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587c9-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="587c9-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="587c9-124">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="587c9-124">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

