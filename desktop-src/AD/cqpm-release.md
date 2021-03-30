---
title: Mensaje de CQPM_RELEASE (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una página de extensión de formulario de consulta cuando la página está a punto de descargarse.
ms.assetid: b935ae8d-a07f-4f0d-b379-5512e96a25a5
ms.tgt_platform: multiple
keywords:
- CQPM_RELEASE Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_RELEASE
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4957f02b57f499d80f7802b4fe9bd2639485b8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079314"
---
# <a name="cqpm_release-message"></a><span data-ttu-id="4888b-104">Mensaje de versión de CQPM \_</span><span class="sxs-lookup"><span data-stu-id="4888b-104">CQPM\_RELEASE message</span></span>

<span data-ttu-id="4888b-105">El mensaje de **\_ versión CQPM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una página de extensión de formulario de consulta cuando la página está a punto de descargarse.</span><span class="sxs-lookup"><span data-stu-id="4888b-105">The **CQPM\_RELEASE** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query form extension page when the page is about to be unloaded.</span></span>

## <a name="parameters"></a><span data-ttu-id="4888b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4888b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4888b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4888b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4888b-108">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4888b-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4888b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4888b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4888b-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4888b-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4888b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4888b-111">Return value</span></span>

<span data-ttu-id="4888b-112">Se omite el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4888b-112">The return value for this message is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4888b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4888b-113">Requirements</span></span>



| <span data-ttu-id="4888b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4888b-114">Requirement</span></span> | <span data-ttu-id="4888b-115">Value</span><span class="sxs-lookup"><span data-stu-id="4888b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4888b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4888b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4888b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4888b-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="4888b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4888b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4888b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4888b-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="4888b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4888b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4888b-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="4888b-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4888b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4888b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4888b-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="4888b-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





