---
title: Mensaje de EM_GETLIMITTEXT (Winuser. h)
description: Obtiene el límite de texto actual para un control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53da76f43716fd7934011a96d449ffa37c254cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905038"
---
# <a name="em_getlimittext-message"></a><span data-ttu-id="1a213-105">\_Mensaje GETLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="1a213-105">EM\_GETLIMITTEXT message</span></span>

<span data-ttu-id="1a213-106">Obtiene el límite de texto actual para un control de edición.</span><span class="sxs-lookup"><span data-stu-id="1a213-106">Gets the current text limit for an edit control.</span></span> <span data-ttu-id="1a213-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1a213-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a213-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a213-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a213-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a213-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a213-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1a213-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a213-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a213-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a213-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1a213-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a213-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a213-113">Return value</span></span>

<span data-ttu-id="1a213-114">El valor devuelto es el límite del texto.</span><span class="sxs-lookup"><span data-stu-id="1a213-114">The return value is the text limit.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a213-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a213-115">Remarks</span></span>

<span data-ttu-id="1a213-116">**Controles de edición, edición enriquecida 2,0 y versiones posteriores:** El límite de texto es la cantidad máxima de texto, en **TCHAR** s, que puede contener el control.</span><span class="sxs-lookup"><span data-stu-id="1a213-116">**Edit controls, Rich Edit 2.0 and later:** The text limit is the maximum amount of text, in **TCHAR** s, that the control can contain.</span></span> <span data-ttu-id="1a213-117">Para texto ANSI, es el número de bytes; en el caso de texto Unicode, es el número de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1a213-117">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="1a213-118">Dos documentos con el mismo límite de caracteres producirán el mismo límite de texto, aunque uno sea ANSI y el otro sea Unicode.</span><span class="sxs-lookup"><span data-stu-id="1a213-118">Two documents with the same character limit will yield the same text limit, even if one is ANSI and the other is Unicode.</span></span>

<span data-ttu-id="1a213-119">**Rich Edit 1,0:** El límite de texto es la cantidad máxima de texto, en bytes, que puede contener el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1a213-119">**Rich Edit 1.0:** The text limit is the maximum amount of text, in bytes, that the rich edit control can contain.</span></span>

<span data-ttu-id="1a213-120">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1a213-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="1a213-121">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="1a213-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a213-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a213-122">Requirements</span></span>



| <span data-ttu-id="1a213-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a213-123">Requirement</span></span> | <span data-ttu-id="1a213-124">Value</span><span class="sxs-lookup"><span data-stu-id="1a213-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a213-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a213-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a213-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1a213-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a213-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a213-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a213-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a213-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a213-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a213-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a213-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a213-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a213-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a213-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a213-132">**\_SETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="1a213-132">**EM\_SETLIMITTEXT**</span></span>](em-setlimittext.md)
</dt> </dl>

 

 





