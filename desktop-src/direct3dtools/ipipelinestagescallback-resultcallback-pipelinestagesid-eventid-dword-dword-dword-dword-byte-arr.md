---
description: Devolución de llamada que notifica al host la información de la imagen de las fases de canalización devuelta por la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_ResultCallback\_PipeLineStagesID\_EventID\_DWORD\_DWORD\_DWORD\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 922DBEE0-CE47-4292-A5E6-4503E6F77A23
api_name:
- IPipeLineStagesCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c9c09c0fe1e68dc0d0613589ff8b3d5037face9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104360008"
---
# <a name="span-idvspixengineipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arrspanipipelinestagescallbackresultcallback-method"></a><span data-ttu-id="eb0ed-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="eb0ed-103"><span id="vspixengine.ipipelinestagescallback_resultcallback_pipelinestagesid_eventid_dword_dword_dword_dword_byte_arr"></span>IPipeLineStagesCallback::ResultCallback method</span></span>

<span data-ttu-id="eb0ed-104">Devolución de llamada que notifica al host la información de la imagen de las fases de canalización devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-104">A callback that notifies the host of pipeline stages image information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0ed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb0ed-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   PipeLineStagesID stageId,
   EventID          eid,
   DWORD            width,
   DWORD            height,
   DWORD            format,
   DWORD            size,
   BYTE []          count5_buffer
);
```

## <a name="parameters"></a><span data-ttu-id="eb0ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb0ed-106">Parameters</span></span>

<span data-ttu-id="eb0ed-107">*stageId* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-107">*stageId* </span></span>  
<span data-ttu-id="eb0ed-108">Fase de canalización representada en los resultados.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-108">The pipeline stage represented in the results.</span></span>

<span data-ttu-id="eb0ed-109">*Eid* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-109">*eid* </span></span>  
<span data-ttu-id="eb0ed-110">Evento representado en los resultados.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-110">The event represented in the results.</span></span>

<span data-ttu-id="eb0ed-111">*Ancho* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-111">*width* </span></span>  
<span data-ttu-id="eb0ed-112">Ancho de la imagen de visualización de la canalización.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-112">The width of the pipeline visualization image.</span></span>

<span data-ttu-id="eb0ed-113">*alto* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-113">*height* </span></span>  
<span data-ttu-id="eb0ed-114">Alto de la imagen de visualización de la canalización.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-114">The height of the pipeline visualization image.</span></span>

<span data-ttu-id="eb0ed-115">*Aplique* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-115">*format* </span></span>  
<span data-ttu-id="eb0ed-116">Formato de la imagen de visualización de la canalización.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-116">The format of the pipeline visualization image.</span></span>

<span data-ttu-id="eb0ed-117">*ajusta* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-117">*size* </span></span>  
<span data-ttu-id="eb0ed-118">Tamaño de la imagen en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-118">The size of the image in bytes.</span></span>

<span data-ttu-id="eb0ed-119">*\_búfer count5* </span><span class="sxs-lookup"><span data-stu-id="eb0ed-119">*count5\_buffer* </span></span>  
<span data-ttu-id="eb0ed-120">La imagen de visualización de la canalización.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-120">The pipeline visualization image.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb0ed-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb0ed-121">Return value</span></span>

<span data-ttu-id="eb0ed-122">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="eb0ed-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb0ed-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb0ed-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0ed-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb0ed-124">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="eb0ed-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb0ed-125">Header</span></span></p></td><td><span data-ttu-id="eb0ed-126">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="eb0ed-126">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="eb0ed-127"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="eb0ed-127"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="eb0ed-128">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="eb0ed-128">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
