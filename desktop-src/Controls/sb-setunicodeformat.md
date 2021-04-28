---
title: SB_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'SB_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.'
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278a5645928a51732b87c12447bb2524bfadfbcd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085893"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="10fdd-105">Mensaje \_ SB SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="10fdd-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="10fdd-106">Establece la marca de formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="10fdd-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="10fdd-107">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="10fdd-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="10fdd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10fdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10fdd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10fdd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10fdd-110">Determina el juego de caracteres utilizado por el control .</span><span class="sxs-lookup"><span data-stu-id="10fdd-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="10fdd-111">Si este valor es **TRUE**, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="10fdd-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="10fdd-112">Si este valor es **FALSE,** el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="10fdd-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="10fdd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10fdd-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="10fdd-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="10fdd-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10fdd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10fdd-115">Return value</span></span>

<span data-ttu-id="10fdd-116">Devuelve la marca de formato Unicode anterior para el control .</span><span class="sxs-lookup"><span data-stu-id="10fdd-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="10fdd-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10fdd-117">Remarks</span></span>

<span data-ttu-id="10fdd-118">Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="10fdd-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fdd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10fdd-119">Requirements</span></span>



| <span data-ttu-id="10fdd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10fdd-120">Requirement</span></span> | <span data-ttu-id="10fdd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="10fdd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10fdd-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10fdd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10fdd-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10fdd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10fdd-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10fdd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10fdd-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="10fdd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10fdd-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10fdd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fdd-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="10fdd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fdd-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="10fdd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fdd-129">**SB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="10fdd-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





