---
title: Mensaje de UDM_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT controles de mensajes de Windows
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
ms.openlocfilehash: 4b2f9eef604af6cf5dfcefbf1e3e03dec561ac21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997136"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="fa3a5-104">\_Mensaje GETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="fa3a5-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="fa3a5-105">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa3a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa3a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa3a5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa3a5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fa3a5-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fa3a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa3a5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fa3a5-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa3a5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa3a5-111">Return value</span></span>

<span data-ttu-id="fa3a5-112">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="fa3a5-113">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="fa3a5-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3a5-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa3a5-115">Remarks</span></span>

<span data-ttu-id="fa3a5-116">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa3a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa3a5-117">Requirements</span></span>



| <span data-ttu-id="fa3a5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa3a5-118">Requirement</span></span> | <span data-ttu-id="fa3a5-119">Value</span><span class="sxs-lookup"><span data-stu-id="fa3a5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3a5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa3a5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3a5-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fa3a5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa3a5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa3a5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3a5-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa3a5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa3a5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa3a5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa3a5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa3a5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa3a5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa3a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3a5-127">**UDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="fa3a5-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





