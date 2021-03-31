---
title: Mensaje de TTM_GETMAXTIPWIDTH (commctrl. h)
description: Recupera el ancho máximo de una ventana de información sobre herramientas.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996411"
---
# <a name="ttm_getmaxtipwidth-message"></a><span data-ttu-id="4faf8-104">TTM \_ GETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="4faf8-104">TTM\_GETMAXTIPWIDTH message</span></span>

<span data-ttu-id="4faf8-105">Recupera el ancho máximo de una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="4faf8-105">Retrieves the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="4faf8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4faf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4faf8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4faf8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4faf8-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4faf8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4faf8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4faf8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4faf8-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4faf8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4faf8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4faf8-111">Return value</span></span>

<span data-ttu-id="4faf8-112">Devuelve un valor **int** que representa el ancho máximo de la información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4faf8-112">Returns an **INT** value that represents the maximum tooltip width, in pixels.</span></span> <span data-ttu-id="4faf8-113">Si no se estableció previamente el ancho máximo, el mensaje devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="4faf8-113">If no maximum width was set previously, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="4faf8-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4faf8-114">Remarks</span></span>

<span data-ttu-id="4faf8-115">El valor de ancho máximo de la información sobre herramientas no indica el ancho real de una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="4faf8-115">The maximum tooltip width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="4faf8-116">En su lugar, si una cadena de información sobre herramientas supera el ancho máximo, el control divide el texto en varias líneas, usando espacios para determinar los saltos de línea.</span><span class="sxs-lookup"><span data-stu-id="4faf8-116">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="4faf8-117">Si el texto no se puede segmentar en varias líneas, se mostrará en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="4faf8-117">If the text cannot be segmented into multiple lines, it will be displayed on a single line.</span></span> <span data-ttu-id="4faf8-118">La longitud de esta línea puede superar el ancho máximo de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="4faf8-118">The length of this line may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="4faf8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4faf8-119">Requirements</span></span>



| <span data-ttu-id="4faf8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4faf8-120">Requirement</span></span> | <span data-ttu-id="4faf8-121">Value</span><span class="sxs-lookup"><span data-stu-id="4faf8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4faf8-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4faf8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4faf8-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4faf8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4faf8-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4faf8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4faf8-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4faf8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4faf8-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4faf8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4faf8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4faf8-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4faf8-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4faf8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4faf8-129">**TTM \_ SETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="4faf8-129">**TTM\_SETMAXTIPWIDTH**</span></span>](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





