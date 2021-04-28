---
title: SB_GETUNICODEFORMAT mensaje (Commctrl.h)
description: 'SB_GETUNICODEFORMAT mensaje: recupera la marca de formato de caracteres Unicode para el control.'
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085903"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="99c02-104">Mensaje \_ SB GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="99c02-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="99c02-105">Recupera la marca de formato de caracteres Unicode para el control .</span><span class="sxs-lookup"><span data-stu-id="99c02-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="99c02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99c02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99c02-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="99c02-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="99c02-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="99c02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99c02-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="99c02-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="99c02-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c02-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99c02-111">Return value</span></span>

<span data-ttu-id="99c02-112">Devuelve la marca de formato Unicode del control.</span><span class="sxs-lookup"><span data-stu-id="99c02-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="99c02-113">Si este valor es distinto de cero, el control usa caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="99c02-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="99c02-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="99c02-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c02-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99c02-115">Remarks</span></span>

<span data-ttu-id="99c02-116">Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="99c02-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c02-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99c02-117">Requirements</span></span>



| <span data-ttu-id="99c02-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="99c02-118">Requirement</span></span> | <span data-ttu-id="99c02-119">Valor</span><span class="sxs-lookup"><span data-stu-id="99c02-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99c02-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99c02-120">Minimum supported client</span></span><br/> | <span data-ttu-id="99c02-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="99c02-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99c02-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99c02-122">Minimum supported server</span></span><br/> | <span data-ttu-id="99c02-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="99c02-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99c02-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99c02-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c02-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="99c02-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c02-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99c02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c02-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="99c02-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





