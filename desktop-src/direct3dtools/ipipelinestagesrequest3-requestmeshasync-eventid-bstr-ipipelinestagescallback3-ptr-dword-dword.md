---
description: Una solicitud asincrónica para obtener los datos de la malla del evento especificado.
MS-HAID: vspixengine.IPipeLineStagesRequest3\_RequestMeshAsync\_EventID\_BSTR\_IPipeLineStagesCallback3\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesRequest3:: RequestMeshAsync (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CAA36C96-3622-4D26-AB26-AD7960700B2A
api_name:
- IPipeLineStagesRequest3.RequestMeshAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 50fc73c803f708284ecef73f89ba74a452816bc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714685"
---
# <a name="span-idvspixengineipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dwordspanipipelinestagesrequest3requestmeshasync-method"></a><span data-ttu-id="d4bb4-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3:: RequestMeshAsync (método)</span><span class="sxs-lookup"><span data-stu-id="d4bb4-103"><span id="vspixengine.ipipelinestagesrequest3_requestmeshasync_eventid_bstr_ipipelinestagescallback3_ptr_dword_dword"></span>IPipeLineStagesRequest3::RequestMeshAsync method</span></span>

<span data-ttu-id="d4bb4-104">Una solicitud asincrónica para obtener los datos de la malla del evento especificado.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-104">An asynchronous request to get mesh data from the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4bb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4bb4-105">Syntax</span></span>


```C++
HRESULT RequestMeshAsync(
   EventID                    eventID,
   BSTR                       meshFilename,
   IPipeLineStagesCallback3 * requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d4bb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4bb4-106">Parameters</span></span>

<span data-ttu-id="d4bb4-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="d4bb4-107">*eventID* </span></span>  
<span data-ttu-id="d4bb4-108">El evento especificado.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-108">The specified event.</span></span>

<span data-ttu-id="d4bb4-109">*meshFilename* </span><span class="sxs-lookup"><span data-stu-id="d4bb4-109">*meshFilename* </span></span>  
<span data-ttu-id="d4bb4-110">Cadena COM que contiene la ruta de acceso del archivo donde se escriben los datos de la malla.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-110">A COM string containing the pathname of the file where the mesh data is written.</span></span>

<span data-ttu-id="d4bb4-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="d4bb4-111">*requestCallback* </span></span>  
<span data-ttu-id="d4bb4-112">Dirección de devolución de llamada que se utiliza para notificar al host los resultados.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d4bb4-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d4bb4-113">*requestCookie* </span></span>  
<span data-ttu-id="d4bb4-114">Cookie que identifica de forma única la solicitud y que se puede usar para indicar que se va a cancelar.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d4bb4-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d4bb4-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d4bb4-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4bb4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4bb4-117">Return value</span></span>

<span data-ttu-id="d4bb4-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d4bb4-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4bb4-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4bb4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4bb4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4bb4-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d4bb4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4bb4-121">Header</span></span></p></td><td><span data-ttu-id="d4bb4-122">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="d4bb4-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d4bb4-123"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="d4bb4-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d4bb4-124">**IPipeLineStagesRequest3**</span><span class="sxs-lookup"><span data-stu-id="d4bb4-124">**IPipeLineStagesRequest3**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest3)

 

 
