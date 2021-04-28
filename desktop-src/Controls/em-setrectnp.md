---
title: EM_SETRECTNP mensaje (Winuser.h)
description: 'EM_SETRECTNP mensaje: establece el rectángulo de formato de un control de edición multilínea.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP de mensajes controles de Windows
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
ms.openlocfilehash: e9a8c85d4f7abd58ed3adb33ede66254c190a7bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085993"
---
# <a name="em_setrectnp-message"></a><span data-ttu-id="44237-104">Mensaje \_ DE EM SETRECTNP</span><span class="sxs-lookup"><span data-stu-id="44237-104">EM\_SETRECTNP message</span></span>

<span data-ttu-id="44237-105">Establece el [rectángulo de formato de](about-edit-controls.md) un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="44237-105">Sets the [formatting rectangle](about-edit-controls.md) of a multiline edit control.</span></span> <span data-ttu-id="44237-106">El **mensaje \_ EM SETRECTNP** es idéntico al mensaje [**EM \_ SETRECT,**](em-setrect.md) salvo que **EM \_ SETRECTNP** no *vuelve* a dibujar la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="44237-106">The **EM\_SETRECTNP** message is identical to the [**EM\_SETRECT**](em-setrect.md) message, except that **EM\_SETRECTNP** does *not* redraw the edit control window.</span></span>

<span data-ttu-id="44237-107">El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="44237-107">The formatting rectangle is the limiting rectangle into which the control draws the text.</span></span> <span data-ttu-id="44237-108">El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="44237-108">The limiting rectangle is independent of the size of the edit control window.</span></span>

<span data-ttu-id="44237-109">Este mensaje solo se procesa mediante controles de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="44237-109">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="44237-110">Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.</span><span class="sxs-lookup"><span data-stu-id="44237-110">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="44237-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44237-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44237-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44237-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44237-113">**Rich Edit 3.0 y versiones posteriores:** Indica si el nuevo rectángulo contiene coordenadas absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="44237-113">**Rich Edit 3.0 and later:** Indicates whether the new rectangle contains absolute or relative coordinates.</span></span> <span data-ttu-id="44237-114">Un valor de cero indica coordenadas absolutas.</span><span class="sxs-lookup"><span data-stu-id="44237-114">A value of zero indicates absolute coordinates.</span></span> <span data-ttu-id="44237-115">Un valor de 1 indica desplazamientos relativos al rectángulo de formato actual.</span><span class="sxs-lookup"><span data-stu-id="44237-115">A value of 1 indicates offsets relative to the current formatting rectangle.</span></span> <span data-ttu-id="44237-116">(Los desplazamientos pueden ser positivos o negativos).</span><span class="sxs-lookup"><span data-stu-id="44237-116">(The offsets can be positive or negative.)</span></span>

<span data-ttu-id="44237-117">**Editar controles:** Este parámetro no se usa y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="44237-117">**Edit controls:** This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="44237-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44237-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44237-119">Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="44237-119">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the new dimensions of the rectangle.</span></span> <span data-ttu-id="44237-120">Si este parámetro es **NULL,** el rectángulo de formato se establece en sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="44237-120">If this parameter is **NULL**, the formatting rectangle is set to its default values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44237-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44237-121">Return value</span></span>

<span data-ttu-id="44237-122">Este mensaje no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="44237-122">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44237-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44237-123">Remarks</span></span>

<span data-ttu-id="44237-124">**Edición enriquecte:** Compatible con Microsoft Rich Edit 3.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="44237-124">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="44237-125">Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="44237-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44237-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44237-126">Requirements</span></span>



| <span data-ttu-id="44237-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="44237-127">Requirement</span></span> | <span data-ttu-id="44237-128">Valor</span><span class="sxs-lookup"><span data-stu-id="44237-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44237-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44237-129">Minimum supported client</span></span><br/> | <span data-ttu-id="44237-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="44237-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44237-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44237-131">Minimum supported server</span></span><br/> | <span data-ttu-id="44237-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="44237-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44237-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44237-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="44237-134"><dt>Winuser.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="44237-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44237-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="44237-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="44237-136">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="44237-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44237-137">**EM \_ SETRECT**</span><span class="sxs-lookup"><span data-stu-id="44237-137">**EM\_SETRECT**</span></span>](em-setrect.md)
</dt> <dt>

<span data-ttu-id="44237-138">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="44237-138">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="44237-139">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44237-139">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

