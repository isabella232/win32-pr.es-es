---
title: Mensaje de EM_SETRECTNP (Winuser. h)
description: Establece el rectángulo de formato de un control de edición multilínea.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996925"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="4a077-104">\_Mensaje SETRECTNP em</span><span class="sxs-lookup"><span data-stu-id="4a077-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="4a077-105">Establece el [rectángulo de formato](about-edit-controls.md) de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="4a077-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="4a077-106">El **mensaje em \_ SETRECTNP** es idéntico al mensaje [**em \_ SETRECT**](em-setrect.md) , salvo que **em \_ SETRECTNP** no vuelve  a dibujar la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="4a077-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="4a077-107">El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="4a077-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="4a077-108">El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="4a077-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="4a077-109">Este mensaje solo lo procesan los controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="4a077-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="4a077-110">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="4a077-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a077-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a077-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a077-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a077-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a077-113">**Edición enriquecida 3,0 y versiones posteriores:** Indica si el nuevo rectángulo contiene coordenadas absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="4a077-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="4a077-114">Un valor de cero indica coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="4a077-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="4a077-115">Un valor de 1 indica desplazamientos respecto al rectángulo de formato actual.</span><span class="sxs-lookup"><span data-stu-id="4a077-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="4a077-116">(Los desplazamientos pueden ser positivos o negativos).</span><span class="sxs-lookup"><span data-stu-id="4a077-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="4a077-117">**Controles de edición:** Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4a077-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a077-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a077-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a077-119">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="4a077-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="4a077-120">Si este parámetro es **null**, el rectángulo de formato se establece en sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="4a077-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a077-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a077-121">Return value</span></span>

<span data-ttu-id="4a077-122">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4a077-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a077-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a077-123">Remarks</span></span>

<span data-ttu-id="4a077-124">**Edición enriquecida:** Compatible con Microsoft Rich Edit 3,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a077-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="4a077-125">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="4a077-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a077-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a077-126">Requirements</span></span>



| <span data-ttu-id="4a077-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a077-127">Requirement</span></span> | <span data-ttu-id="4a077-128">Value</span><span class="sxs-lookup"><span data-stu-id="4a077-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a077-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a077-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4a077-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a077-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4a077-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a077-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4a077-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a077-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a077-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a077-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a077-134"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a077-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a077-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a077-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a077-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4a077-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a077-137">**\_SETRECT em**</span><span class="sxs-lookup"><span data-stu-id="4a077-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="4a077-138">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="4a077-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4a077-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a077-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

