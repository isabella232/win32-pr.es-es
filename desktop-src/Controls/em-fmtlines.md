---
title: Mensaje de EM_FMTLINES (Winuser. h)
description: Establece una marca que determina si un control de edición multilínea incluye caracteres de salto de línea automáticos. Un salto de línea flexible se compone de dos retornos de carro y un avance de línea, y se inserta al final de una línea que se rompe debido a aparecen.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491009"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="4780c-105">\_Mensaje FMTLINES em</span><span class="sxs-lookup"><span data-stu-id="4780c-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="4780c-106">Establece una marca que determina si un control de edición multilínea incluye caracteres de salto de línea automáticos.</span><span class="sxs-lookup"><span data-stu-id="4780c-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="4780c-107">Un salto de línea flexible se compone de dos retornos de carro y un avance de línea, y se inserta al final de una línea que se rompe debido a aparecen.</span><span class="sxs-lookup"><span data-stu-id="4780c-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="4780c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4780c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4780c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4780c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4780c-110">Especifica si se van a insertar caracteres de salto de línea.</span><span class="sxs-lookup"><span data-stu-id="4780c-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="4780c-111">Un valor **true** inserta los caracteres; Si el valor **es false** , se quitan.</span><span class="sxs-lookup"><span data-stu-id="4780c-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="4780c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4780c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4780c-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4780c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4780c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4780c-114">Return value</span></span>

<span data-ttu-id="4780c-115">El valor devuelto es idéntico al parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="4780c-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="4780c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4780c-116">Remarks</span></span>

<span data-ttu-id="4780c-117">Este mensaje solo afecta al búfer devuelto por el mensaje de [**\_ GETHANDLE em**](em-gethandle.md) y el texto devuelto por el mensaje de [**\_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) .</span><span class="sxs-lookup"><span data-stu-id="4780c-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="4780c-118">No tiene ningún efecto en la presentación del texto en el control de edición.</span><span class="sxs-lookup"><span data-stu-id="4780c-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="4780c-119">El **mensaje \_ FMTLINES em** no afecta a una línea que termina con un salto de línea fuerte.</span><span class="sxs-lookup"><span data-stu-id="4780c-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="4780c-120">Un salto de línea fuerte se compone de un retorno de carro y un avance de línea.</span><span class="sxs-lookup"><span data-stu-id="4780c-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="4780c-121">El tamaño del texto cambia cuando se procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4780c-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="4780c-122">**Edición enriquecida:** No se admite el mensaje **\_ FMTLINES em** .</span><span class="sxs-lookup"><span data-stu-id="4780c-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4780c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4780c-123">Requirements</span></span>



| <span data-ttu-id="4780c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4780c-124">Requirement</span></span> | <span data-ttu-id="4780c-125">Value</span><span class="sxs-lookup"><span data-stu-id="4780c-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4780c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4780c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4780c-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4780c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4780c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4780c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4780c-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4780c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4780c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4780c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4780c-131"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4780c-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4780c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4780c-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="4780c-133">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4780c-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4780c-134">**GETHANDLE (EM) \_**</span><span class="sxs-lookup"><span data-stu-id="4780c-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="4780c-135">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="4780c-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4780c-136">**GETTEXT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="4780c-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

