---
title: Mensaje de HDM_GETBITMAPMARGIN (commctrl. h)
description: Obtiene el ancho del margen de mapa de bits de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header GetBitmapMargin.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c3f0fced77edd3f149009e1b3c2bb1eb75182c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996432"
---
# <a name="hdm_getbitmapmargin-message"></a><span data-ttu-id="b33e3-105">HDM \_ GETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="b33e3-105">HDM\_GETBITMAPMARGIN message</span></span>

<span data-ttu-id="b33e3-106">Obtiene el ancho del margen de mapa de bits de un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="b33e3-106">Gets the width of the bitmap margin for a header control.</span></span> <span data-ttu-id="b33e3-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="b33e3-107">You can send this message explicitly or use the [**Header\_GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b33e3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b33e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b33e3-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b33e3-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b33e3-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b33e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b33e3-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b33e3-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b33e3-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33e3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b33e3-113">Return value</span></span>

<span data-ttu-id="b33e3-114">Devuelve el ancho del margen del mapa de bits en píxeles.</span><span class="sxs-lookup"><span data-stu-id="b33e3-114">Returns the width of the bitmap margin in pixels.</span></span> <span data-ttu-id="b33e3-115">Si no se especificó previamente el margen del mapa de bits, se devuelve el valor predeterminado de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE).</span><span class="sxs-lookup"><span data-stu-id="b33e3-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM\_CXEDGE) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33e3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33e3-116">Requirements</span></span>



| <span data-ttu-id="b33e3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33e3-117">Requirement</span></span> | <span data-ttu-id="b33e3-118">Value</span><span class="sxs-lookup"><span data-stu-id="b33e3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b33e3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b33e3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b33e3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b33e3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b33e3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b33e3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b33e3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b33e3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b33e3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b33e3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b33e3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b33e3-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b33e3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b33e3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b33e3-126">**HDM \_ SETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="b33e3-126">**HDM\_SETBITMAPMARGIN**</span></span>](hdm-setbitmapmargin.md)
</dt> </dl>

 

