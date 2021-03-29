---
title: Mensaje de EM_GETRECT (Winuser. h)
description: Obtiene el rectángulo de formato de un control de edición.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905311"
---
# <a name="em_getrect-message"></a><span data-ttu-id="2061f-104">\_Mensaje GETRECT em</span><span class="sxs-lookup"><span data-stu-id="2061f-104">EM\_GETRECT message</span></span>

<span data-ttu-id="2061f-105">Obtiene el [rectángulo de formato](about-edit-controls.md) de un control de edición.</span><span class="sxs-lookup"><span data-stu-id="2061f-105">Gets the [formatting rectangle](about-edit-controls.md) of an edit control.</span></span> <span data-ttu-id="2061f-106">El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="2061f-106">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="2061f-107">El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="2061f-107">The limiting rectangle is independent of the size of the edit-control window.</span></span> <span data-ttu-id="2061f-108">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2061f-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2061f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2061f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2061f-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2061f-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2061f-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="2061f-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2061f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2061f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2061f-113">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo de formato.</span><span class="sxs-lookup"><span data-stu-id="2061f-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the formatting rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2061f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2061f-114">Return value</span></span>

<span data-ttu-id="2061f-115">El valor devuelto no es significativo.</span><span class="sxs-lookup"><span data-stu-id="2061f-115">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2061f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2061f-116">Remarks</span></span>

<span data-ttu-id="2061f-117">Puede modificar el rectángulo de formato de un control de edición multilínea mediante los mensajes [**em \_ SETRECT**](em-setrect.md) y [**em \_ SETRECTNP**](em-setrectnp.md) .</span><span class="sxs-lookup"><span data-stu-id="2061f-117">You can modify the formatting rectangle of a multiline edit control by using the [**EM\_SETRECT**](em-setrect.md) and [**EM\_SETRECTNP**](em-setrectnp.md) messages.</span></span>

<span data-ttu-id="2061f-118">En determinadas condiciones, es posible que **em \_ GETRECT** no devuelva los valores exactos que [**em \_ SETRECT**](em-setrect.md) o [**em \_ SETRECTNP**](em-setrectnp.md) set será aproximadamente correcto, pero puede estar desactivado en unos pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="2061f-118">Under certain conditions, **EM\_GETRECT** might not return the exact values that [**EM\_SETRECT**](em-setrect.md) or [**EM\_SETRECTNP**](em-setrectnp.md) set it will be approximately correct, but it can be off by a few pixels.</span></span>

<span data-ttu-id="2061f-119">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2061f-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="2061f-120">El rectángulo de formato no incluye la barra de selección, que es un área no marcada a la izquierda de cada párrafo.</span><span class="sxs-lookup"><span data-stu-id="2061f-120">The formatting rectangle does not include the selection bar, which is an unmarked area to the left of each paragraph.</span></span> <span data-ttu-id="2061f-121">Al hacer clic en ella, la barra de selección selecciona la línea.</span><span class="sxs-lookup"><span data-stu-id="2061f-121">When clicked, the selection bar selects the line.</span></span> <span data-ttu-id="2061f-122">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="2061f-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2061f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2061f-123">Requirements</span></span>



| <span data-ttu-id="2061f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2061f-124">Requirement</span></span> | <span data-ttu-id="2061f-125">Value</span><span class="sxs-lookup"><span data-stu-id="2061f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2061f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2061f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2061f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2061f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2061f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2061f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2061f-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2061f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2061f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2061f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2061f-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2061f-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2061f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2061f-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="2061f-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="2061f-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2061f-134">**\_SETRECT em**</span><span class="sxs-lookup"><span data-stu-id="2061f-134">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

[<span data-ttu-id="2061f-135">**\_SETRECTNP em**</span><span class="sxs-lookup"><span data-stu-id="2061f-135">**EM\_SETRECTNP**</span></span>](em-setrectnp.md)
</dt> <dt>

<span data-ttu-id="2061f-136">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="2061f-136">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2061f-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2061f-137">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

