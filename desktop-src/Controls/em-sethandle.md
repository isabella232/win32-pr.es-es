---
title: Mensaje de EM_SETHANDLE (Winuser. h)
description: Establece el identificador de la memoria que va a usar un control de edición multilínea.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150917"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="437cd-104">\_Mensaje SETHANDLE em</span><span class="sxs-lookup"><span data-stu-id="437cd-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="437cd-105">Establece el identificador de la memoria que va a usar un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="437cd-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="437cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="437cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="437cd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="437cd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="437cd-108">Identificador del búfer de memoria que el control de edición utiliza para almacenar el texto que se muestra actualmente en lugar de asignar su propia memoria.</span><span class="sxs-lookup"><span data-stu-id="437cd-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="437cd-109">Si es necesario, el control reasigna esta memoria.</span><span class="sxs-lookup"><span data-stu-id="437cd-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="437cd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="437cd-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="437cd-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="437cd-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="437cd-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="437cd-112">Return value</span></span>

<span data-ttu-id="437cd-113">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="437cd-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="437cd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="437cd-114">Remarks</span></span>

<span data-ttu-id="437cd-115">Antes de que una aplicación establezca un nuevo identificador de memoria, debe enviar un mensaje de [**\_ GETHANDLE em**](em-gethandle.md) para recuperar el identificador del búfer de memoria actual y liberar esa memoria.</span><span class="sxs-lookup"><span data-stu-id="437cd-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="437cd-116">Un control de edición reasigna automáticamente el búfer determinado cada vez que necesita espacio adicional para el texto o quita el texto suficiente para que ya no se necesite espacio adicional.</span><span class="sxs-lookup"><span data-stu-id="437cd-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="437cd-117">Al enviar un mensaje **\_ SETHANDLE em** se borra el búfer de deshacer (EM) y la marca de modificación interna ([**em \_ GETMODIFY**](em-getmodify.md) devuelve cero).[**\_**](em-canundo.md)</span><span class="sxs-lookup"><span data-stu-id="437cd-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="437cd-118">Se vuelve a dibujar la ventana de control de edición.</span><span class="sxs-lookup"><span data-stu-id="437cd-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="437cd-119">**Edición enriquecida:** No se admite el mensaje **\_ SETHANDLE em** .</span><span class="sxs-lookup"><span data-stu-id="437cd-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="437cd-120">Los controles Rich Edit no almacenan texto como una matriz de caracteres simple.</span><span class="sxs-lookup"><span data-stu-id="437cd-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="437cd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="437cd-121">Requirements</span></span>



| <span data-ttu-id="437cd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="437cd-122">Requirement</span></span> | <span data-ttu-id="437cd-123">Value</span><span class="sxs-lookup"><span data-stu-id="437cd-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="437cd-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="437cd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="437cd-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="437cd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="437cd-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="437cd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="437cd-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="437cd-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="437cd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="437cd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="437cd-129"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="437cd-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="437cd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="437cd-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="437cd-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="437cd-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="437cd-132">**la \_ CANUNDO em**</span><span class="sxs-lookup"><span data-stu-id="437cd-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="437cd-133">**GETHANDLE (EM) \_**</span><span class="sxs-lookup"><span data-stu-id="437cd-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="437cd-134">**\_GETMODIFY em**</span><span class="sxs-lookup"><span data-stu-id="437cd-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 





