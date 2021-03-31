---
title: Mensaje de CCM_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- CCM_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491519"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="6cf1f-105">\_Mensaje SETUNICODEFORMAT de CCM</span><span class="sxs-lookup"><span data-stu-id="6cf1f-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="6cf1f-106">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="6cf1f-107">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cf1f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cf1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cf1f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cf1f-110">Valor que determina el juego de caracteres utilizado por el control.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="6cf1f-111">Si este valor es **true**, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="6cf1f-112">Si este valor es **false**, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="6cf1f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cf1f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6cf1f-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf1f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cf1f-115">Return value</span></span>

<span data-ttu-id="6cf1f-116">Devuelve la marca de formato Unicode anterior para el control.</span><span class="sxs-lookup"><span data-stu-id="6cf1f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf1f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cf1f-117">Requirements</span></span>



| <span data-ttu-id="6cf1f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf1f-118">Requirement</span></span> | <span data-ttu-id="6cf1f-119">Value</span><span class="sxs-lookup"><span data-stu-id="6cf1f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf1f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cf1f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf1f-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6cf1f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cf1f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6cf1f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf1f-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6cf1f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cf1f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cf1f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cf1f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cf1f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf1f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cf1f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf1f-127">**\_GETUNICODEFORMAT CCM**</span><span class="sxs-lookup"><span data-stu-id="6cf1f-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





