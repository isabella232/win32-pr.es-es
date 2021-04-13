---
title: Enumeración CB_REQUEST_STATUS (Cbclient. h)
description: Especifica el estado de una solicitud asincrónica.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS enumeración Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359705"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="9e851-104">\_Enumeración del estado de la solicitud CB \_</span><span class="sxs-lookup"><span data-stu-id="9e851-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="9e851-105">Especifica el estado de una solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="9e851-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="9e851-106">Esta enumeración se utiliza con el método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="9e851-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e851-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e851-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="9e851-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="9e851-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9e851-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_Estado CB \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="9e851-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-110">El objeto de solicitud no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="9e851-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_solicitud de \_ Inicio del estado CB \_**</span><span class="sxs-lookup"><span data-stu-id="9e851-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9e851-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**solicitud de estado de CB \_ \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="9e851-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-114">La solicitud se ha completado.</span><span class="sxs-lookup"><span data-stu-id="9e851-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**error en la \_ solicitud de estado CB \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9e851-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-116">Error en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e851-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_solicitud de estado CB \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="9e851-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-118">Se anuló la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9e851-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_destino de \_ búsqueda de estado de CB \_**</span><span class="sxs-lookup"><span data-stu-id="9e851-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9e851-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_destino de \_ carga de estado de CB \_**</span><span class="sxs-lookup"><span data-stu-id="9e851-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9e851-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**Estado de CB \_ \_ poniendo \_ sesión \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="9e851-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9e851-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e851-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_estado \_ de CB redirigiendo \_ al \_ destino**</span><span class="sxs-lookup"><span data-stu-id="9e851-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="9e851-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9e851-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e851-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e851-127">Requirements</span></span>



| <span data-ttu-id="9e851-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e851-128">Requirement</span></span> | <span data-ttu-id="9e851-129">Value</span><span class="sxs-lookup"><span data-stu-id="9e851-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e851-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e851-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9e851-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9e851-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="9e851-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e851-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9e851-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e851-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="9e851-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e851-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e851-135"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e851-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e851-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e851-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e851-137">**IConnectionBrokerRequest:: CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="9e851-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





