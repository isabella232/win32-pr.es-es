---
title: Mensaje de RB_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control.
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- RB_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6ef31c409ddc0570b03a3bcd8bb0dd81e9c722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489245"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="a53dd-104">Mensaje de GETUNICODEFORMAT de RB \_</span><span class="sxs-lookup"><span data-stu-id="a53dd-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="a53dd-105">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="a53dd-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a53dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a53dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a53dd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a53dd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a53dd-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a53dd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a53dd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a53dd-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a53dd-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a53dd-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a53dd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a53dd-111">Return value</span></span>

<span data-ttu-id="a53dd-112">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="a53dd-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="a53dd-113">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a53dd-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="a53dd-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="a53dd-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a53dd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a53dd-115">Remarks</span></span>

<span data-ttu-id="a53dd-116">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a53dd-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a53dd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53dd-117">Requirements</span></span>



| <span data-ttu-id="a53dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53dd-118">Requirement</span></span> | <span data-ttu-id="a53dd-119">Value</span><span class="sxs-lookup"><span data-stu-id="a53dd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a53dd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a53dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a53dd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a53dd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a53dd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a53dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a53dd-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a53dd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a53dd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a53dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53dd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a53dd-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a53dd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a53dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53dd-127">**\_SETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="a53dd-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





