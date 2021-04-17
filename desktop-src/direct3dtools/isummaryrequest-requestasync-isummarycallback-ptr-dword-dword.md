---
description: Una solicitud asincrónica para obtener información de resumen sobre un registro de gráficos.
MS-HAID: vspixengine.ISummaryRequest\_RequestAsync\_iSummaryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISummaryRequest:: RequestAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A33798E3-7332-4582-A7B1-B0F9FB694872
api_name:
- ISummaryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c716545de275250efcae56a6be39c8b620ed014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714744"
---
# <a name="span-idvspixengineisummaryrequest_requestasync_isummarycallback_ptr_dword_dwordspanisummaryrequestrequestasync-method"></a><span data-ttu-id="4f512-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest:: RequestAsync (método)</span><span class="sxs-lookup"><span data-stu-id="4f512-103"><span id="vspixengine.isummaryrequest_requestasync_isummarycallback_ptr_dword_dword"></span>ISummaryRequest::RequestAsync method</span></span>

<span data-ttu-id="4f512-104">Una solicitud asincrónica para obtener información de resumen sobre un registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="4f512-104">An asynchronous request to get summary information about a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f512-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f512-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   iSummaryCallback * requestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4f512-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f512-106">Parameters</span></span>

<span data-ttu-id="4f512-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4f512-107">*requestCallback* </span></span>  
<span data-ttu-id="4f512-108">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="4f512-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4f512-109">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="4f512-109">*requestCookie* </span></span>  
<span data-ttu-id="4f512-110">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="4f512-110">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4f512-111">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4f512-111">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4f512-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4f512-112">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f512-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f512-113">Return value</span></span>

<span data-ttu-id="4f512-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4f512-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f512-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f512-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f512-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f512-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4f512-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f512-117">Header</span></span></p></td><td><span data-ttu-id="4f512-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="4f512-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4f512-119"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="4f512-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4f512-120">**ISummaryRequest**</span><span class="sxs-lookup"><span data-stu-id="4f512-120">**ISummaryRequest**</span></span>](/windows/desktop/direct3dtools/isummaryrequest)

 

 
