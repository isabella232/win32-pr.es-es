---
title: UDM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: 'UDM_GETUNICODEFORMAT mensaje: recupera la marca de formato de caracteres Unicode para el control.'
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT de mensajes controles de Windows
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273164df7f7021f39ec26a22eb637e8b9969fc24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113594"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="23433-104">Mensaje \_ GETUNICODEFORMAT de UDM</span><span class="sxs-lookup"><span data-stu-id="23433-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="23433-105">Recupera la marca de formato de caracteres Unicode para el control .</span><span class="sxs-lookup"><span data-stu-id="23433-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="23433-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23433-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23433-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23433-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="23433-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="23433-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="23433-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23433-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23433-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="23433-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23433-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23433-111">Return value</span></span>

<span data-ttu-id="23433-112">Devuelve la marca de formato Unicode del control.</span><span class="sxs-lookup"><span data-stu-id="23433-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="23433-113">Si este valor es distinto de cero, el control usa caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="23433-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="23433-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="23433-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="23433-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="23433-115">Remarks</span></span>

<span data-ttu-id="23433-116">Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="23433-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="23433-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23433-117">Requirements</span></span>



| <span data-ttu-id="23433-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="23433-118">Requirement</span></span> | <span data-ttu-id="23433-119">Valor</span><span class="sxs-lookup"><span data-stu-id="23433-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23433-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23433-120">Minimum supported client</span></span><br/> | <span data-ttu-id="23433-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="23433-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23433-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23433-122">Minimum supported server</span></span><br/> | <span data-ttu-id="23433-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="23433-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23433-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23433-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="23433-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="23433-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23433-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="23433-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23433-127">**UDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="23433-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





