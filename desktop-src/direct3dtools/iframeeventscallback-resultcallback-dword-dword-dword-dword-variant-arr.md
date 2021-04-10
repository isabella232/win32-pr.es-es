---
description: Función de devolución de llamada que se usa para notificar al host de información sobre eventos en la lista de eventos.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274725"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span data-ttu-id="0ce22-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="0ce22-103"><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>IFrameEventsCallback::ResultCallback method</span></span>

<span data-ttu-id="0ce22-104">Función de devolución de llamada que se usa para notificar al host de información sobre eventos en la lista de eventos.</span><span class="sxs-lookup"><span data-stu-id="0ce22-104">A callback function used to notify the host of information about events in the event list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ce22-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a><span data-ttu-id="0ce22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ce22-106">Parameters</span></span>

<span data-ttu-id="0ce22-107">*Númeromarco* </span><span class="sxs-lookup"><span data-stu-id="0ce22-107">*frameNumber* </span></span>  
<span data-ttu-id="0ce22-108">Número de marco asociado a los eventos.</span><span class="sxs-lookup"><span data-stu-id="0ce22-108">The frame number associated with the events.</span></span>

<span data-ttu-id="0ce22-109">*numElements* </span><span class="sxs-lookup"><span data-stu-id="0ce22-109">*numElements* </span></span>  
<span data-ttu-id="0ce22-110">El número total de campos en todas las columnas de todos los eventos.</span><span class="sxs-lookup"><span data-stu-id="0ce22-110">The total number of fields in all columns of all events.</span></span>

<span data-ttu-id="0ce22-111">*numRows* </span><span class="sxs-lookup"><span data-stu-id="0ce22-111">*numRows* </span></span>  
<span data-ttu-id="0ce22-112">Número de eventos del resultado.</span><span class="sxs-lookup"><span data-stu-id="0ce22-112">The number of events in the result.</span></span>

<span data-ttu-id="0ce22-113">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="0ce22-113">*numColumns* </span></span>  
<span data-ttu-id="0ce22-114">El número de columnas (campos) de cada fila.</span><span class="sxs-lookup"><span data-stu-id="0ce22-114">The number of columns (fields) in each row.</span></span>

<span data-ttu-id="0ce22-115">*count1 \_ pRowData* </span><span class="sxs-lookup"><span data-stu-id="0ce22-115">*count1\_pRowData* </span></span>  
<span data-ttu-id="0ce22-116">Información sobre los eventos; un elemento para cada campo de cada evento.</span><span class="sxs-lookup"><span data-stu-id="0ce22-116">Information about the events; one item for each field of each event.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ce22-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ce22-117">Return value</span></span>

<span data-ttu-id="0ce22-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0ce22-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ce22-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ce22-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce22-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ce22-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0ce22-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ce22-121">Header</span></span></p></td><td><span data-ttu-id="0ce22-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0ce22-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0ce22-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="0ce22-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0ce22-124">**IFrameEventsCallback**</span><span class="sxs-lookup"><span data-stu-id="0ce22-124">**IFrameEventsCallback**</span></span>](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
