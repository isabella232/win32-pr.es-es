---
title: Mensaje de CQPM_GETPARAMETERS (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para recuperar datos sobre la consulta realizada por la página.
ms.assetid: 6b94b318-8356-4554-99fe-f82364325e6e
ms.tgt_platform: multiple
keywords:
- CQPM_GETPARAMETERS Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_GETPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aac8961e2299e4a8a69ead9426698e8c932346e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905064"
---
# <a name="cqpm_getparameters-message"></a><span data-ttu-id="d79be-104">CQPM \_ mensaje de GETPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d79be-104">CQPM\_GETPARAMETERS message</span></span>

<span data-ttu-id="d79be-105">El mensaje de **\_ GETPARAMETERS de CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para recuperar datos sobre la consulta realizada por la página.</span><span class="sxs-lookup"><span data-stu-id="d79be-105">The **CQPM\_GETPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to retrieve data about the query performed by the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="d79be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d79be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d79be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d79be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d79be-108">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d79be-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d79be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d79be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d79be-110">Puntero a un valor de [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) que recibe datos sobre la consulta realizada por la página.</span><span class="sxs-lookup"><span data-stu-id="d79be-110">Pointer to a [**LPDSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) value that receives data about the query performed by the page.</span></span> <span data-ttu-id="d79be-111">Si este parámetro es **null**, la extensión **DSQUERYPARAMS** debe estar asignada mediante la función [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) .</span><span class="sxs-lookup"><span data-stu-id="d79be-111">If this parameter is **NULL**, the **DSQUERYPARAMS** structure must be allocated by the extension using the [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d79be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d79be-112">Return value</span></span>

<span data-ttu-id="d79be-113">Devuelve **S \_ correcto** si es correcto o un código de error **HRESULT** estándar en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d79be-113">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d79be-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d79be-114">Requirements</span></span>



| <span data-ttu-id="d79be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d79be-115">Requirement</span></span> | <span data-ttu-id="d79be-116">Value</span><span class="sxs-lookup"><span data-stu-id="d79be-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d79be-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d79be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d79be-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d79be-118">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="d79be-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d79be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d79be-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d79be-120">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="d79be-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d79be-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d79be-122"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="d79be-122"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d79be-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d79be-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d79be-124">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="d79be-124">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="d79be-125">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="d79be-125">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> <dt>

[<span data-ttu-id="d79be-126">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="d79be-126">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
</dt> </dl>

 

