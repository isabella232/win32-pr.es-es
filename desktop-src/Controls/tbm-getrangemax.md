---
title: Mensaje de TBM_GETRANGEMAX (commctrl. h)
description: Recupera la posición máxima del control deslizante en una barra de desplazamiento.
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- TBM_GETRANGEMAX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079400"
---
# <a name="tbm_getrangemax-message"></a><span data-ttu-id="46df8-104">TBM \_ GETRANGEMAX</span><span class="sxs-lookup"><span data-stu-id="46df8-104">TBM\_GETRANGEMAX message</span></span>

<span data-ttu-id="46df8-105">Recupera la posición máxima del control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="46df8-105">Retrieves the maximum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="46df8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46df8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46df8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46df8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="46df8-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="46df8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="46df8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46df8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="46df8-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="46df8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46df8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46df8-111">Return value</span></span>

<span data-ttu-id="46df8-112">Devuelve un valor de 32 bits que especifica la posición máxima en el intervalo de la barra de desplazamiento mínima en el máximo.</span><span class="sxs-lookup"><span data-stu-id="46df8-112">Returns a 32-bit value that specifies the maximum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="46df8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46df8-113">Requirements</span></span>



| <span data-ttu-id="46df8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46df8-114">Requirement</span></span> | <span data-ttu-id="46df8-115">Value</span><span class="sxs-lookup"><span data-stu-id="46df8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46df8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46df8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46df8-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="46df8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46df8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46df8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46df8-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="46df8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46df8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46df8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46df8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46df8-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46df8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="46df8-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="46df8-123">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="46df8-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="46df8-124">**TBM \_ GETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="46df8-124">**TBM\_GETRANGEMIN**</span></span>](tbm-getrangemin.md)
</dt> <dt>

[<span data-ttu-id="46df8-125">**TBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="46df8-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="46df8-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="46df8-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





