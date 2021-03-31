---
title: Mensaje EM_SETCTFOPENSTATUS (RichEdit. h)
description: Abre o cierra el teclado de servicios de texto (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079663"
---
# <a name="em_setctfopenstatus-message"></a><span data-ttu-id="06976-104">\_Mensaje SETCTFOPENSTATUS em</span><span class="sxs-lookup"><span data-stu-id="06976-104">EM\_SETCTFOPENSTATUS message</span></span>

<span data-ttu-id="06976-105">Abre o cierra el teclado de servicios de texto (TSF).</span><span class="sxs-lookup"><span data-stu-id="06976-105">Opens or closes the Text Services Framework (TSF) keyboard.</span></span>

## <a name="parameters"></a><span data-ttu-id="06976-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06976-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06976-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06976-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06976-108">Para activar el teclado TSF, use **true**.</span><span class="sxs-lookup"><span data-stu-id="06976-108">To turn on the TSF keyboard, use **TRUE**.</span></span> <span data-ttu-id="06976-109">Para desactivar el teclado TSF, use **false**.</span><span class="sxs-lookup"><span data-stu-id="06976-109">To turn off the TSF keyboard, use **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="06976-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06976-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06976-111">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="06976-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06976-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06976-112">Return value</span></span>

<span data-ttu-id="06976-113">Si se realiza correctamente, este mensaje devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="06976-113">If successful, this message returns **TRUE**.</span></span> <span data-ttu-id="06976-114">Si no se realiza correctamente, este mensaje devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="06976-114">If unsuccessful, this message returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="06976-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06976-115">Requirements</span></span>



| <span data-ttu-id="06976-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="06976-116">Requirement</span></span> | <span data-ttu-id="06976-117">Value</span><span class="sxs-lookup"><span data-stu-id="06976-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06976-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06976-118">Minimum supported client</span></span><br/> | <span data-ttu-id="06976-119">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="06976-119">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06976-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06976-120">Minimum supported server</span></span><br/> | <span data-ttu-id="06976-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="06976-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06976-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06976-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="06976-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="06976-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06976-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="06976-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06976-125">**\_GETCTFOPENSTATUS em**</span><span class="sxs-lookup"><span data-stu-id="06976-125">**EM\_GETCTFOPENSTATUS**</span></span>](em-getctfopenstatus.md)
</dt> </dl>

 

 





