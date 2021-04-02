---
title: Mensaje de TCM_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la \_ macro TabCtrl GetUnicodeFormat.
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- TCM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905545"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="b3724-105">\_Mensaje GETUNICODEFORMAT de TCM</span><span class="sxs-lookup"><span data-stu-id="b3724-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="b3724-106">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="b3724-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="b3724-107">Puede enviar este mensaje explícitamente o utilizar la macro [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="b3724-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b3724-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3724-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3724-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b3724-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b3724-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b3724-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b3724-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b3724-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b3724-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b3724-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3724-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3724-113">Return value</span></span>

<span data-ttu-id="b3724-114">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="b3724-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="b3724-115">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="b3724-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="b3724-116">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="b3724-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3724-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3724-117">Remarks</span></span>

<span data-ttu-id="b3724-118">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b3724-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3724-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3724-119">Requirements</span></span>



| <span data-ttu-id="b3724-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3724-120">Requirement</span></span> | <span data-ttu-id="b3724-121">Value</span><span class="sxs-lookup"><span data-stu-id="b3724-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3724-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3724-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3724-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b3724-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3724-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b3724-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3724-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3724-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b3724-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3724-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3724-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3724-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3724-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3724-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3724-129">**\_SETUNICODEFORMAT TCM**</span><span class="sxs-lookup"><span data-stu-id="b3724-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





