---
description: Función de devolución de llamada que se usa para notificar al host la información de resumen del registro de gráficos.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISummaryCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714745"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span data-ttu-id="e0e4e-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="e0e4e-103"><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback::ResultCallback method</span></span>

<span data-ttu-id="e0e4e-104">Función de devolución de llamada que se usa para notificar al host la información de resumen del registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e0e4e-104">A callback function used to notify the host of graphics log summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e4e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0e4e-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a><span data-ttu-id="e0e4e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0e4e-106">Parameters</span></span>

<span data-ttu-id="e0e4e-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="e0e4e-107">*count* </span></span>  
<span data-ttu-id="e0e4e-108">El número de elementos de información de Resumen devueltos.</span><span class="sxs-lookup"><span data-stu-id="e0e4e-108">The number of summary information items returned.</span></span>

<span data-ttu-id="e0e4e-109">*count0 \_ summaryItem* </span><span class="sxs-lookup"><span data-stu-id="e0e4e-109">*count0\_summaryItem* </span></span>  
<span data-ttu-id="e0e4e-110">Los elementos de información de resumen (pares clave-valor).</span><span class="sxs-lookup"><span data-stu-id="e0e4e-110">The summary information items (key-value pairs).</span></span>

## <a name="return-value"></a><span data-ttu-id="e0e4e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0e4e-111">Return value</span></span>

<span data-ttu-id="e0e4e-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e0e4e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0e4e-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0e4e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e4e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e4e-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e0e4e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0e4e-115">Header</span></span></p></td><td><span data-ttu-id="e0e4e-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e0e4e-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e0e4e-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="e0e4e-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e0e4e-118">**ISummaryCallback**</span><span class="sxs-lookup"><span data-stu-id="e0e4e-118">**ISummaryCallback**</span></span>](/windows/desktop/direct3dtools/isummarycallback)

 

 
