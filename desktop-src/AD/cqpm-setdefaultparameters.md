---
title: Mensaje de CQPM_SETDEFAULTPARAMETERS (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para establecer parámetros predeterminados alternativos para la página.
ms.assetid: 4d7f1c03-5c67-4f4c-b381-034a142251fe
ms.tgt_platform: multiple
keywords:
- CQPM_SETDEFAULTPARAMETERS Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_SETDEFAULTPARAMETERS
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4df77b9068c23a0eeac30181d131cb8469dc53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490384"
---
# <a name="cqpm_setdefaultparameters-message"></a><span data-ttu-id="d2727-104">CQPM \_ SETDEFAULTPARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2727-104">CQPM\_SETDEFAULTPARAMETERS message</span></span>

<span data-ttu-id="d2727-105">El mensaje **CQPM \_ SETDEFAULTPARAMETERS** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para establecer parámetros predeterminados alternativos para la página.</span><span class="sxs-lookup"><span data-stu-id="d2727-105">The **CQPM\_SETDEFAULTPARAMETERS** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to set alternate default parameters for the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2727-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2727-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2727-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2727-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2727-108">Contiene un valor distinto de cero si la página es la página predeterminada o cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d2727-108">Contains nonzero if the page is the default page or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="d2727-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2727-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2727-110">Puntero a una estructura [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) que contiene datos sobre el cuadro de diálogo consulta de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="d2727-110">Pointer to an [**OPENQUERYWINDOW**](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow) structure that contains data about the directory service query dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2727-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2727-111">Return value</span></span>

<span data-ttu-id="d2727-112">Se omite el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d2727-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2727-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2727-113">Requirements</span></span>



| <span data-ttu-id="d2727-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2727-114">Requirement</span></span> | <span data-ttu-id="d2727-115">Value</span><span class="sxs-lookup"><span data-stu-id="d2727-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2727-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2727-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d2727-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2727-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="d2727-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2727-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d2727-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2727-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="d2727-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2727-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2727-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2727-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2727-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2727-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2727-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="d2727-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[<span data-ttu-id="d2727-124">**OPENQUERYWINDOW**</span><span class="sxs-lookup"><span data-stu-id="d2727-124">**OPENQUERYWINDOW**</span></span>](/windows/desktop/api/Cmnquery/ns-cmnquery-openquerywindow)
</dt> </dl>

 

 





