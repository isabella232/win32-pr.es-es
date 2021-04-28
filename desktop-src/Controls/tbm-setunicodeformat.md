---
title: TBM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TBM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.'
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- TBM_SETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- TBM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f076efe2a575eff131c9bc2a1fe3df9ecab0fe68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104043"
---
# <a name="tbm_setunicodeformat-message"></a><span data-ttu-id="436f2-105">Mensaje \_ TBM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="436f2-105">TBM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="436f2-106">Establece la marca de formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="436f2-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="436f2-107">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="436f2-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="436f2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="436f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="436f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="436f2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="436f2-110">Determina el juego de caracteres utilizado por el control .</span><span class="sxs-lookup"><span data-stu-id="436f2-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="436f2-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="436f2-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="436f2-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="436f2-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="436f2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="436f2-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="436f2-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="436f2-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="436f2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="436f2-115">Return value</span></span>

<span data-ttu-id="436f2-116">Devuelve la marca de formato Unicode anterior para el control .</span><span class="sxs-lookup"><span data-stu-id="436f2-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="436f2-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="436f2-117">Remarks</span></span>

<span data-ttu-id="436f2-118">Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="436f2-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="436f2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="436f2-119">Requirements</span></span>



| <span data-ttu-id="436f2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="436f2-120">Requirement</span></span> | <span data-ttu-id="436f2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="436f2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="436f2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="436f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="436f2-123">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="436f2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="436f2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="436f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="436f2-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="436f2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="436f2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="436f2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="436f2-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="436f2-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="436f2-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="436f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="436f2-129">**TBM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="436f2-129">**TBM\_GETUNICODEFORMAT**</span></span>](tbm-getunicodeformat.md)
</dt> </dl>

 

 





