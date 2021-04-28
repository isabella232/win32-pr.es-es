---
title: TBM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TBM_GETUNICODEFORMAT mensaje: recupera la marca de formato de caracteres Unicode para el control.'
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT de mensajes controles de Windows
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104093"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="580bc-104">Mensaje \_ GETUNICODEFORMAT de TBM</span><span class="sxs-lookup"><span data-stu-id="580bc-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="580bc-105">Recupera la marca de formato de caracteres Unicode para el control .</span><span class="sxs-lookup"><span data-stu-id="580bc-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="580bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="580bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="580bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="580bc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="580bc-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="580bc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="580bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="580bc-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="580bc-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="580bc-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="580bc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="580bc-111">Return value</span></span>

<span data-ttu-id="580bc-112">Devuelve la marca de formato Unicode del control.</span><span class="sxs-lookup"><span data-stu-id="580bc-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="580bc-113">Si este valor es distinto de cero, el control usa caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="580bc-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="580bc-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="580bc-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="580bc-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="580bc-115">Remarks</span></span>

<span data-ttu-id="580bc-116">Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="580bc-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="580bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="580bc-117">Requirements</span></span>



| <span data-ttu-id="580bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="580bc-118">Requirement</span></span> | <span data-ttu-id="580bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="580bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="580bc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="580bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="580bc-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="580bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="580bc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="580bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="580bc-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="580bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="580bc-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="580bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="580bc-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="580bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580bc-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="580bc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580bc-127">**TBM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="580bc-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





