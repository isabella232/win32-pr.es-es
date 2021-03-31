---
title: Mensaje de CQPM_CLEARFORM (Cmnquery. h)
description: Se envía a la función de devolución de llamada CQPageProc de una consulta de la página de extensión cuando el contenido de la página debe restablecerse a los valores predeterminados.
ms.assetid: 0fd3ec82-0566-43de-a7a1-4b6b76bf2050
ms.tgt_platform: multiple
keywords:
- CQPM_CLEARFORM Active Directory de mensaje
topic_type:
- apiref
api_name:
- CQPM_CLEARFORM
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94af3a31a29da4ce5740c4e326bbf1a8961f9f82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996011"
---
# <a name="cqpm_clearform-message"></a><span data-ttu-id="bcb07-104">CQPM \_ CLEARFORM</span><span class="sxs-lookup"><span data-stu-id="bcb07-104">CQPM\_CLEARFORM message</span></span>

<span data-ttu-id="bcb07-105">El mensaje **CQPM \_ CLEARFORM** se envía a la función de devolución de llamada [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) de una consulta de la página de extensión cuando el contenido de la página debe restablecerse a los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="bcb07-105">The **CQPM\_CLEARFORM** message is sent to the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function of a query for extension page when the contents of the page should be reset to the default values.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcb07-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcb07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcb07-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcb07-108">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bcb07-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="bcb07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcb07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcb07-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bcb07-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb07-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcb07-111">Return value</span></span>

<span data-ttu-id="bcb07-112">Devuelve **S \_ correcto** si es correcto o un código de error **HRESULT** estándar en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bcb07-112">Returns **S\_OK** if successful or a standard **HRESULT** error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb07-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb07-113">Requirements</span></span>



| <span data-ttu-id="bcb07-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb07-114">Requirement</span></span> | <span data-ttu-id="bcb07-115">Value</span><span class="sxs-lookup"><span data-stu-id="bcb07-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb07-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcb07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb07-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcb07-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="bcb07-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcb07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb07-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcb07-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="bcb07-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcb07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb07-121"><dt>Cmnquery. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb07-121"><dt>Cmnquery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb07-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcb07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb07-123">**CQPageProc**</span><span class="sxs-lookup"><span data-stu-id="bcb07-123">**CQPageProc**</span></span>](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> </dl>

 

 





