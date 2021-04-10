---
title: Mensaje de TTM_SETMAXTIPWIDTH (commctrl. h)
description: Establece el ancho máximo de una ventana de información sobre herramientas.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274521"
---
# <a name="ttm_setmaxtipwidth-message"></a><span data-ttu-id="26ff5-104">TTM \_ SETMAXTIPWIDTH</span><span class="sxs-lookup"><span data-stu-id="26ff5-104">TTM\_SETMAXTIPWIDTH message</span></span>

<span data-ttu-id="26ff5-105">Establece el ancho máximo de una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="26ff5-105">Sets the maximum width for a tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="26ff5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ff5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26ff5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="26ff5-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="26ff5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="26ff5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26ff5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="26ff5-110">Ancho máximo de la ventana de información sobre herramientas o-1 para permitir cualquier ancho.</span><span class="sxs-lookup"><span data-stu-id="26ff5-110">Maximum tooltip window width, or -1 to allow any width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ff5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26ff5-111">Return value</span></span>

<span data-ttu-id="26ff5-112">Devuelve el ancho máximo de la información sobre herramientas anterior.</span><span class="sxs-lookup"><span data-stu-id="26ff5-112">Returns the previous maximum tooltip width.</span></span>

## <a name="remarks"></a><span data-ttu-id="26ff5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26ff5-113">Remarks</span></span>

<span data-ttu-id="26ff5-114">El valor de ancho máximo no indica el ancho real de una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="26ff5-114">The maximum width value does not indicate a tooltip window's actual width.</span></span> <span data-ttu-id="26ff5-115">En su lugar, si una cadena de información sobre herramientas supera el ancho máximo, el control divide el texto en varias líneas, usando espacios para determinar los saltos de línea.</span><span class="sxs-lookup"><span data-stu-id="26ff5-115">Rather, if a tooltip string exceeds the maximum width, the control breaks the text into multiple lines, using spaces to determine line breaks.</span></span> <span data-ttu-id="26ff5-116">Si el texto no se puede segmentar en varias líneas, se muestra en una sola línea, lo que puede superar el ancho máximo de la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="26ff5-116">If the text cannot be segmented into multiple lines, it is displayed on a single line, which may exceed the maximum tooltip width.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ff5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26ff5-117">Requirements</span></span>



| <span data-ttu-id="26ff5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="26ff5-118">Requirement</span></span> | <span data-ttu-id="26ff5-119">Value</span><span class="sxs-lookup"><span data-stu-id="26ff5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26ff5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26ff5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26ff5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26ff5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26ff5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26ff5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26ff5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="26ff5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26ff5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26ff5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26ff5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ff5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ff5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="26ff5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ff5-127">**TTM \_ GETMAXTIPWIDTH**</span><span class="sxs-lookup"><span data-stu-id="26ff5-127">**TTM\_GETMAXTIPWIDTH**</span></span>](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





