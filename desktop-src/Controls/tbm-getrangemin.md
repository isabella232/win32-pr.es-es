---
title: Mensaje de TBM_GETRANGEMIN (commctrl. h)
description: Recupera la posición mínima del control deslizante en una barra de desplazamiento.
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- TBM_GETRANGEMIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddef597f7b129f8334f75136f56404a8ef117fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996424"
---
# <a name="tbm_getrangemin-message"></a><span data-ttu-id="2d343-104">TBM \_ GETRANGEMIN</span><span class="sxs-lookup"><span data-stu-id="2d343-104">TBM\_GETRANGEMIN message</span></span>

<span data-ttu-id="2d343-105">Recupera la posición mínima del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2d343-105">Retrieves the minimum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d343-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d343-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d343-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d343-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2d343-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2d343-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2d343-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d343-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2d343-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2d343-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d343-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d343-111">Return value</span></span>

<span data-ttu-id="2d343-112">Devuelve un valor de 32 bits que especifica la posición mínima en el intervalo de la barra de desplazamiento mínima en el máximo.</span><span class="sxs-lookup"><span data-stu-id="2d343-112">Returns a 32-bit value that specifies the minimum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d343-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d343-113">Requirements</span></span>



| <span data-ttu-id="2d343-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d343-114">Requirement</span></span> | <span data-ttu-id="2d343-115">Value</span><span class="sxs-lookup"><span data-stu-id="2d343-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d343-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d343-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d343-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2d343-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d343-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2d343-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d343-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2d343-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d343-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d343-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d343-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d343-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d343-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d343-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="2d343-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2d343-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2d343-124">**TBM \_ GETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="2d343-124">**TBM\_GETRANGEMAX**</span></span>](tbm-getrangemax.md)
</dt> <dt>

[<span data-ttu-id="2d343-125">**TBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="2d343-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="2d343-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="2d343-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





