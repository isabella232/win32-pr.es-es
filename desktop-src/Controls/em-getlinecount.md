---
title: Mensaje de EM_GETLINECOUNT (Winuser. h)
description: Obtiene el número de líneas de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETLINECOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLINECOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15ffbeafb13850317faccb4be44571d81b0d7e36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489461"
---
# <a name="em_getlinecount-message-winuserh"></a><span data-ttu-id="5f318-105">Mensaje de EM_GETLINECOUNT (Winuser. h)</span><span class="sxs-lookup"><span data-stu-id="5f318-105">EM_GETLINECOUNT message (Winuser.h)</span></span>

<span data-ttu-id="5f318-106">Obtiene el número de líneas de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="5f318-106">Gets the number of lines in a multiline edit control.</span></span> <span data-ttu-id="5f318-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5f318-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f318-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f318-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f318-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f318-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f318-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f318-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5f318-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f318-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f318-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f318-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f318-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f318-113">Return value</span></span>

<span data-ttu-id="5f318-114">El valor devuelto es un entero que especifica el número total de líneas de texto en el control de edición multilínea o el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="5f318-114">The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control.</span></span> <span data-ttu-id="5f318-115">Si el control no tiene texto, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="5f318-115">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="5f318-116">El valor devuelto nunca será menor que 1.</span><span class="sxs-lookup"><span data-stu-id="5f318-116">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f318-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f318-117">Remarks</span></span>

<span data-ttu-id="5f318-118">El **mensaje \_ GETLINECOUNT em** recupera el número total de líneas de texto, no solo el número de líneas que están visibles actualmente.</span><span class="sxs-lookup"><span data-stu-id="5f318-118">The **EM\_GETLINECOUNT** message retrieves the total number of text lines, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="5f318-119">Si la característica WordWrap está habilitada, el número de líneas puede cambiar cuando cambian las dimensiones de la ventana de edición.</span><span class="sxs-lookup"><span data-stu-id="5f318-119">If the Wordwrap feature is enabled, the number of lines can change when the dimensions of the editing window change.</span></span>

<span data-ttu-id="5f318-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5f318-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="5f318-121">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="5f318-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f318-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f318-122">Requirements</span></span>



| <span data-ttu-id="5f318-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f318-123">Requirement</span></span> | <span data-ttu-id="5f318-124">Value</span><span class="sxs-lookup"><span data-stu-id="5f318-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f318-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f318-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5f318-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f318-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f318-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f318-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5f318-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f318-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f318-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f318-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f318-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f318-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f318-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f318-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f318-132">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5f318-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f318-133">**\_GETLINE em**</span><span class="sxs-lookup"><span data-stu-id="5f318-133">**EM\_GETLINE**</span></span>](em-getline.md)
</dt> <dt>

[<span data-ttu-id="5f318-134">**\_LINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="5f318-134">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="5f318-135">**Editar \_ GetLineCount**</span><span class="sxs-lookup"><span data-stu-id="5f318-135">**Edit\_GetLineCount**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getlinecount)
</dt> </dl>

 

 





