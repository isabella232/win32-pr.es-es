---
title: RB_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'RB_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.'
ms.assetid: 769b74e0-c1f0-4068-80c4-075f1db2058a
keywords:
- RB_SETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- RB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9c168ee298d28d59010491031f7d94ebcaa650
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090973"
---
# <a name="rb_setunicodeformat-message"></a><span data-ttu-id="84269-105">Mensaje \_ SETUNICODEFORMAT de RB</span><span class="sxs-lookup"><span data-stu-id="84269-105">RB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="84269-106">Establece la marca de formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="84269-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="84269-107">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="84269-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="84269-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84269-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84269-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84269-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84269-110">Determina el juego de caracteres utilizado por el control .</span><span class="sxs-lookup"><span data-stu-id="84269-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="84269-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="84269-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="84269-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="84269-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="84269-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84269-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="84269-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="84269-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84269-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84269-115">Return value</span></span>

<span data-ttu-id="84269-116">Devuelve la marca de formato Unicode anterior para el control .</span><span class="sxs-lookup"><span data-stu-id="84269-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="84269-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84269-117">Remarks</span></span>

<span data-ttu-id="84269-118">Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="84269-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="84269-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84269-119">Requirements</span></span>



| <span data-ttu-id="84269-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="84269-120">Requirement</span></span> | <span data-ttu-id="84269-121">Valor</span><span class="sxs-lookup"><span data-stu-id="84269-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84269-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84269-122">Minimum supported client</span></span><br/> | <span data-ttu-id="84269-123">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="84269-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84269-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="84269-124">Minimum supported server</span></span><br/> | <span data-ttu-id="84269-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="84269-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84269-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84269-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="84269-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="84269-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84269-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84269-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84269-129">**RB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="84269-129">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
</dt> </dl>

 

 





