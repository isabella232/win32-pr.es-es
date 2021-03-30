---
title: Mensaje de MCM_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la \_ macro MonthCal GetUnicodeFormat.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- MCM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803830"
---
# <a name="mcm_getunicodeformat-message"></a><span data-ttu-id="30221-105">Mensaje de MCM \_ GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="30221-105">MCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="30221-106">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="30221-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="30221-107">Puede enviar este mensaje explícitamente o utilizar la macro [**MonthCal \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="30221-107">You can send this message explicitly or use the [**MonthCal\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="30221-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30221-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30221-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30221-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="30221-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="30221-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="30221-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30221-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="30221-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="30221-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30221-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30221-113">Return value</span></span>

<span data-ttu-id="30221-114">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="30221-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="30221-115">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="30221-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="30221-116">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="30221-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="30221-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30221-117">Remarks</span></span>

<span data-ttu-id="30221-118">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="30221-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="30221-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30221-119">Requirements</span></span>



| <span data-ttu-id="30221-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="30221-120">Requirement</span></span> | <span data-ttu-id="30221-121">Value</span><span class="sxs-lookup"><span data-stu-id="30221-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30221-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30221-122">Minimum supported client</span></span><br/> | <span data-ttu-id="30221-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="30221-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30221-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30221-124">Minimum supported server</span></span><br/> | <span data-ttu-id="30221-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="30221-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30221-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30221-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="30221-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="30221-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30221-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="30221-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30221-129">**MCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="30221-129">**MCM\_SETUNICODEFORMAT**</span></span>](mcm-setunicodeformat.md)
</dt> </dl>

 

 





