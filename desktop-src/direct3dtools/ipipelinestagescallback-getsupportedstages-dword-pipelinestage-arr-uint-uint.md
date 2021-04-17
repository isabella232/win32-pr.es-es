---
description: Devolución de llamada que notifica al host las fases de canalización que usa la llamada a Draw de la solicitud asociada.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback:: GetSupportedStages (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c55c7f8bfa6b5b69ea2a46dd6023021a6b4ab6c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537005"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span data-ttu-id="f18a5-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback:: GetSupportedStages (método)</span><span class="sxs-lookup"><span data-stu-id="f18a5-103"><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages method</span></span>

<span data-ttu-id="f18a5-104">Devolución de llamada que notifica al host las fases de canalización que usa la llamada a Draw de la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="f18a5-104">A callback that notifies the host of which pipeline stages are used by the draw call of the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f18a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f18a5-105">Syntax</span></span>


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a><span data-ttu-id="f18a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f18a5-106">Parameters</span></span>

<span data-ttu-id="f18a5-107">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="f18a5-107">*numColumns* </span></span>  
<span data-ttu-id="f18a5-108">Número de fases devueltas.</span><span class="sxs-lookup"><span data-stu-id="f18a5-108">The number of stages returned.</span></span>

<span data-ttu-id="f18a5-109">*count0 \_ pStages* </span><span class="sxs-lookup"><span data-stu-id="f18a5-109">*count0\_pStages* </span></span>  
<span data-ttu-id="f18a5-110">Fases de canalización.</span><span class="sxs-lookup"><span data-stu-id="f18a5-110">The pipeline stages.</span></span>

<span data-ttu-id="f18a5-111">*swapChainWidth* </span><span class="sxs-lookup"><span data-stu-id="f18a5-111">*swapChainWidth* </span></span>  
<span data-ttu-id="f18a5-112">El ancho de la cadena de intercambio asociada con la llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="f18a5-112">The width of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="f18a5-113">Se usa cuando se solicitan imágenes de vista previa de canalización.</span><span class="sxs-lookup"><span data-stu-id="f18a5-113">This is used when requesting pipeline preview images.</span></span>

<span data-ttu-id="f18a5-114">*swapChainHeight* </span><span class="sxs-lookup"><span data-stu-id="f18a5-114">*swapChainHeight* </span></span>  
<span data-ttu-id="f18a5-115">El alto de la cadena de intercambio asociada con la llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="f18a5-115">The height of the swap chain assocaited with the draw call.</span></span> <span data-ttu-id="f18a5-116">Se usa cuando se solicitan imágenes de vista previa de canalización.</span><span class="sxs-lookup"><span data-stu-id="f18a5-116">This is used when requesting pipeline preview images.</span></span>

## <a name="return-value"></a><span data-ttu-id="f18a5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f18a5-117">Return value</span></span>

<span data-ttu-id="f18a5-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f18a5-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f18a5-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f18a5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f18a5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f18a5-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f18a5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f18a5-121">Header</span></span></p></td><td><span data-ttu-id="f18a5-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f18a5-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f18a5-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="f18a5-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f18a5-124">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="f18a5-124">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
