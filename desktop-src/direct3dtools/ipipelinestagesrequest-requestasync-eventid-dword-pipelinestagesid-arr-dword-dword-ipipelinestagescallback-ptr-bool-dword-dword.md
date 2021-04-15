---
description: Una solicitud asincrónica para obtener las imágenes de vista previa para la ventana etapas de canalización de gráficos.
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestAsync\_EventID\_DWORD\_PipeLineStagesID\_arr\_DWORD\_DWORD\_IPipeLineStagesCallback\_ptr\_BOOL\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B725E541-EAC8-49DE-9EE7-C20698FE4A1F
api_name:
- IPipeLineStagesRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89c67689668aa1c4227b33d861495c2504e5d626
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537540"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dwordspanipipelinestagesrequestrequestasync-method"></a><span data-ttu-id="c8b3b-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="c8b3b-103"><span id="vspixengine.ipipelinestagesrequest_requestasync_eventid_dword_pipelinestagesid_arr_dword_dword_ipipelinestagescallback_ptr_bool_dword_dword"></span>IPipeLineStagesRequest::RequestAsync method</span></span>

<span data-ttu-id="c8b3b-104">Una solicitud asincrónica para obtener las imágenes de vista previa para la ventana etapas de canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-104">An asynchronous request to get preview images for the graphics pipeline stages window.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b3b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8b3b-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   DWORD                     numStages,
   PipeLineStagesID []       count1_stageIds,
   DWORD                     width,
   DWORD                     height,
   IPipeLineStagesCallback * requestCallback,
   BOOL                      getMeshData,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="c8b3b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8b3b-106">Parameters</span></span>

<span data-ttu-id="c8b3b-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-107">*eventID* </span></span>  
<span data-ttu-id="c8b3b-108">IDENTIFICADOR del evento de gráficos para el que se solicitan las imágenes.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-108">The ID of the graphics event that images are being requested for.</span></span>

<span data-ttu-id="c8b3b-109">*numStages* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-109">*numStages* </span></span>  
<span data-ttu-id="c8b3b-110">El número de fases de canalización para las que se solicitan las imágenes.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-110">The number of pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="c8b3b-111">*count1 \_ stageIds* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-111">*count1\_stageIds* </span></span>  
<span data-ttu-id="c8b3b-112">Identificadores de las fases de canalización para las que se solicitan las imágenes.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-112">IDs of the pipeline stages that images are being requested for.</span></span>

<span data-ttu-id="c8b3b-113">*Ancho* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-113">*width* </span></span>  
<span data-ttu-id="c8b3b-114">Ancho de las imágenes solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-114">The width of the requested images.</span></span>

<span data-ttu-id="c8b3b-115">*alto* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-115">*height* </span></span>  
<span data-ttu-id="c8b3b-116">Alto de las imágenes solicitadas.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-116">The height of the requested images.</span></span>

<span data-ttu-id="c8b3b-117">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-117">*requestCallback* </span></span>  
<span data-ttu-id="c8b3b-118">La dirección de la devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-118">The address of the callback used to notify the host of results.</span></span>

<span data-ttu-id="c8b3b-119">*getMeshData* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-119">*getMeshData* </span></span>  
<span data-ttu-id="c8b3b-120">True para devolver datos de malla; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-120">true to return mesh data; otherwise false.</span></span>

<span data-ttu-id="c8b3b-121">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-121">*requestCookie* </span></span>  
<span data-ttu-id="c8b3b-122">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-122">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="c8b3b-123">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="c8b3b-123">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="c8b3b-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-124">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8b3b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8b3b-125">Return value</span></span>

<span data-ttu-id="c8b3b-126">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c8b3b-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8b3b-127">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8b3b-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b3b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b3b-128">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c8b3b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8b3b-129">Header</span></span></p></td><td><span data-ttu-id="c8b3b-130">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c8b3b-130">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="c8b3b-131"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="c8b3b-131"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="c8b3b-132">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="c8b3b-132">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
