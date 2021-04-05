---
title: Mensaje de CQPM_ENABLE (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta para habilitar o deshabilitar la página.
ms.assetid: dc75fab7-6de7-4138-86df-84d44e774120
ms.tgt_platform: multiple
keywords:
- CQPM_ENABLE Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_ENABLE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0252c5e1ec7fd9633241416fbf01bb4ead52c45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079011"
---
# <a name="cqpm_enable-message"></a><span data-ttu-id="a8fbe-104">CQPM \_ Habilitar mensaje</span><span class="sxs-lookup"><span data-stu-id="a8fbe-104">CQPM\_ENABLE message</span></span>

<span data-ttu-id="a8fbe-105">El mensaje de **\_ habilitación de CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta para habilitar o deshabilitar la página.</span><span class="sxs-lookup"><span data-stu-id="a8fbe-105">The **CQPM\_ENABLE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page to enable or disable the page.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8fbe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8fbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8fbe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8fbe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8fbe-108">Contiene cero para deshabilitar la página o un valor distinto de cero para habilitar la página.</span><span class="sxs-lookup"><span data-stu-id="a8fbe-108">Contains zero to disable the page or nonzero to enable the page.</span></span>

</dd> <dt>

<span data-ttu-id="a8fbe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8fbe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8fbe-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a8fbe-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8fbe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8fbe-111">Return value</span></span>

<span data-ttu-id="a8fbe-112">Se omite el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a8fbe-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fbe-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fbe-113">Requirements</span></span>



| <span data-ttu-id="a8fbe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8fbe-114">Requirement</span></span> | <span data-ttu-id="a8fbe-115">Value</span><span class="sxs-lookup"><span data-stu-id="a8fbe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fbe-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8fbe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fbe-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8fbe-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a8fbe-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8fbe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fbe-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8fbe-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="a8fbe-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8fbe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8fbe-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8fbe-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fbe-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8fbe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fbe-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="a8fbe-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





