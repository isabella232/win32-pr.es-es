---
title: Mensaje de EM_GETFIRSTVISIBLELINE (Winuser. h)
description: Obtiene el índice de base cero de la línea visible superior de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534689"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="d9986-105">\_Mensaje GETFIRSTVISIBLELINE em</span><span class="sxs-lookup"><span data-stu-id="d9986-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="d9986-106">Obtiene el índice de base cero de la línea visible superior de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="d9986-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="d9986-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d9986-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9986-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9986-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9986-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9986-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9986-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d9986-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d9986-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9986-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9986-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d9986-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9986-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9986-113">Return value</span></span>

<span data-ttu-id="d9986-114">El valor devuelto es el índice de base cero de la línea visible superior en un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="d9986-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="d9986-115">**Controles de edición:** En el caso de los controles de edición de una sola línea, el valor devuelto es el índice de base cero del primer carácter visible.</span><span class="sxs-lookup"><span data-stu-id="d9986-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="d9986-116">**Controles Rich Edit:** En el caso de los controles de edición enriquecida de una sola línea, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="d9986-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9986-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9986-117">Remarks</span></span>

<span data-ttu-id="d9986-118">El número de líneas y la longitud de las líneas en un control de edición dependen del ancho del control y del valor de WordWrap actual.</span><span class="sxs-lookup"><span data-stu-id="d9986-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="d9986-119">**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d9986-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="d9986-120">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d9986-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9986-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9986-121">Requirements</span></span>



| <span data-ttu-id="d9986-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9986-122">Requirement</span></span> | <span data-ttu-id="d9986-123">Value</span><span class="sxs-lookup"><span data-stu-id="d9986-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9986-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9986-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d9986-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9986-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9986-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9986-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d9986-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9986-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9986-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9986-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9986-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9986-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





