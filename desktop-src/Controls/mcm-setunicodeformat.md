---
title: MCM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'MCM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control.'
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- MCM_SETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa922b0dde8702f447690f9626938364174cbff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112374"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="9a823-104">Mensaje \_ SETUNICODEFORMAT de MCM</span><span class="sxs-lookup"><span data-stu-id="9a823-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="9a823-105">Establece la marca de formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="9a823-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="9a823-106">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="9a823-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="9a823-107">Puede enviar este mensaje explícitamente o usar la macro [**MonthCal \_ SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat)</span><span class="sxs-lookup"><span data-stu-id="9a823-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a823-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a823-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a823-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9a823-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9a823-110">Determina el juego de caracteres utilizado por el control .</span><span class="sxs-lookup"><span data-stu-id="9a823-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="9a823-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a823-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="9a823-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a823-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="9a823-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9a823-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9a823-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9a823-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a823-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a823-115">Return value</span></span>

<span data-ttu-id="9a823-116">Devuelve la marca de formato Unicode anterior para el control .</span><span class="sxs-lookup"><span data-stu-id="9a823-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a823-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9a823-117">Remarks</span></span>

<span data-ttu-id="9a823-118">Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9a823-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a823-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a823-119">Requirements</span></span>



| <span data-ttu-id="9a823-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a823-120">Requirement</span></span> | <span data-ttu-id="9a823-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9a823-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a823-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a823-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9a823-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9a823-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a823-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a823-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9a823-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a823-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a823-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a823-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a823-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="9a823-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a823-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9a823-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a823-129">**MCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="9a823-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





