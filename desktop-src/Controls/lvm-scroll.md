---
title: Mensaje de LVM_SCROLL (commctrl. h)
description: Desplaza el contenido de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro scroll de ListView.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491452"
---
# <a name="lvm_scroll-message"></a><span data-ttu-id="aa8e2-105">Mensaje de desplazamiento del LVM \_</span><span class="sxs-lookup"><span data-stu-id="aa8e2-105">LVM\_SCROLL message</span></span>

<span data-ttu-id="aa8e2-106">Desplaza el contenido de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-106">Scrolls the content of a list-view control.</span></span> <span data-ttu-id="aa8e2-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ Scroll de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) .</span><span class="sxs-lookup"><span data-stu-id="aa8e2-107">You can send this message explicitly or by using the [**ListView\_Scroll**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa8e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa8e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa8e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa8e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8e2-110">Valor de tipo **int** que especifica la cantidad de desplazamiento horizontal, en píxeles, con respecto a la posición actual del contenido de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-110">Value of type **int** that specifies the amount of horizontal scrolling, in pixels, relative to the current position of the list view content.</span></span> <span data-ttu-id="aa8e2-111">Si el control de vista de lista está en la vista de lista, este valor se redondea al número más cercano de píxeles que forman una columna completa.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-111">If the list-view control is in list view, this value is rounded up to the nearest number of pixels that form a whole column.</span></span>

</dd> <dt>

<span data-ttu-id="aa8e2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa8e2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa8e2-113">Valor de tipo **int** que especifica la cantidad de desplazamiento vertical, en píxeles, con respecto a la posición actual del contenido de la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-113">Value of type **int** that specifies the amount of vertical scrolling, in pixels, relative to the current position of the list view content.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa8e2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa8e2-114">Return value</span></span>

<span data-ttu-id="aa8e2-115">Devuelve **true si es** correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-115">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa8e2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa8e2-116">Remarks</span></span>

<span data-ttu-id="aa8e2-117">Cuando el control de vista de lista está en la vista de informe, el control solo se puede desplazar verticalmente en incrementos de líneas completas.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-117">When the list-view control is in report view, the control can only be scrolled vertically in whole line increments.</span></span> <span data-ttu-id="aa8e2-118">Por lo tanto, el parámetro *lParam* se redondea al número más cercano de píxeles que forman un incremento de línea completo.</span><span class="sxs-lookup"><span data-stu-id="aa8e2-118">Therefore, the *lParam* parameter will be rounded to the nearest number of pixels that form a whole line increment.</span></span> <span data-ttu-id="aa8e2-119">Por ejemplo, si el alto de una línea es 16 píxeles y 8 se pasa para *lParam*, la lista se desplazará por 16 píxeles (1 línea).</span><span class="sxs-lookup"><span data-stu-id="aa8e2-119">For example, if the height of a line is 16 pixels and 8 is passed for *lParam*, the list will be scrolled by 16 pixels (1 line).</span></span> <span data-ttu-id="aa8e2-120">Si se pasa 7 para *lParam*, la lista se desplazará 0 píxeles (0 líneas).</span><span class="sxs-lookup"><span data-stu-id="aa8e2-120">If 7 is passed for *lParam*, the list will be scrolled 0 pixels (0 lines).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa8e2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa8e2-121">Requirements</span></span>



| <span data-ttu-id="aa8e2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa8e2-122">Requirement</span></span> | <span data-ttu-id="aa8e2-123">Value</span><span class="sxs-lookup"><span data-stu-id="aa8e2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8e2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa8e2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8e2-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa8e2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa8e2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa8e2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8e2-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa8e2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa8e2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa8e2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa8e2-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa8e2-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





