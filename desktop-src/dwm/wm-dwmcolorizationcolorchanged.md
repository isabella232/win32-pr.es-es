---
title: Mensaje de WM_DWMCOLORIZATIONCOLORCHANGED (Winuser. h)
description: Informa a todas las ventanas de nivel superior que el color de coloración ha cambiado.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED Administrador de ventanas de escritorio de mensaje
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150373"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="55de2-104">Mensaje de DWMCOLORIZATIONCOLORCHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="55de2-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="55de2-105">Informa a todas las ventanas de nivel superior que el color de coloración ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="55de2-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="55de2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55de2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55de2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55de2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55de2-108">Especifica el nuevo color de color.</span><span class="sxs-lookup"><span data-stu-id="55de2-108">Specifies the new colorization color.</span></span> <span data-ttu-id="55de2-109">El formato de color es 0xAARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="55de2-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="55de2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55de2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55de2-111">Especifica si el nuevo color se mezcla con opacidad.</span><span class="sxs-lookup"><span data-stu-id="55de2-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55de2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55de2-112">Return value</span></span>

<span data-ttu-id="55de2-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="55de2-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="55de2-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55de2-114">Remarks</span></span>

<span data-ttu-id="55de2-115">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="55de2-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="55de2-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) se utiliza para determinar el valor de color actual.</span><span class="sxs-lookup"><span data-stu-id="55de2-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="55de2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55de2-117">Requirements</span></span>



| <span data-ttu-id="55de2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="55de2-118">Requirement</span></span> | <span data-ttu-id="55de2-119">Value</span><span class="sxs-lookup"><span data-stu-id="55de2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55de2-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55de2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55de2-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="55de2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="55de2-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55de2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55de2-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="55de2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55de2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55de2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55de2-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="55de2-125"><dt>Winuser.h</dt></span></span> </dl> |



 

