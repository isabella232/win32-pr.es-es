---
title: Mensaje de HDM_SETBITMAPMARGIN (commctrl. h)
description: Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetBitmapMargin.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905478"
---
# <a name="hdm_setbitmapmargin-message"></a><span data-ttu-id="c00f9-105">HDM \_ SETBITMAPMARGIN</span><span class="sxs-lookup"><span data-stu-id="c00f9-105">HDM\_SETBITMAPMARGIN message</span></span>

<span data-ttu-id="c00f9-106">Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente.</span><span class="sxs-lookup"><span data-stu-id="c00f9-106">Sets the width of the margin, specified in pixels, of a bitmap in an existing header control.</span></span> <span data-ttu-id="c00f9-107">Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .</span><span class="sxs-lookup"><span data-stu-id="c00f9-107">You can send this message explicitly or use the [**Header\_SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c00f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c00f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c00f9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c00f9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c00f9-110">Ancho, especificado en píxeles, del margen que rodea un mapa de bits dentro de un control de encabezado existente.</span><span class="sxs-lookup"><span data-stu-id="c00f9-110">The width, specified in pixels, of the margin that surrounds a bitmap within an existing header control.</span></span>

</dd> <dt>

<span data-ttu-id="c00f9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c00f9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c00f9-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c00f9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c00f9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c00f9-113">Return value</span></span>

<span data-ttu-id="c00f9-114">Devuelve el ancho del margen del mapa de bits, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c00f9-114">Returns the width of the bitmap margin, in pixels.</span></span> <span data-ttu-id="c00f9-115">Si no se especificó previamente el margen del mapa de bits, se devuelve el valor predeterminado de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*).</span><span class="sxs-lookup"><span data-stu-id="c00f9-115">If the bitmap margin was not previously specified, the default value of 3\* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM\_CXEDGE*) is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c00f9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c00f9-116">Requirements</span></span>



| <span data-ttu-id="c00f9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c00f9-117">Requirement</span></span> | <span data-ttu-id="c00f9-118">Value</span><span class="sxs-lookup"><span data-stu-id="c00f9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c00f9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c00f9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c00f9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c00f9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c00f9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c00f9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c00f9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c00f9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c00f9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c00f9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c00f9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c00f9-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c00f9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c00f9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00f9-126">**HDM \_ GETBITMAPMARGIN**</span><span class="sxs-lookup"><span data-stu-id="c00f9-126">**HDM\_GETBITMAPMARGIN**</span></span>](hdm-getbitmapmargin.md)
</dt> </dl>

 

