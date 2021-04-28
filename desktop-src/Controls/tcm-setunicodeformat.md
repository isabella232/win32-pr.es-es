---
title: TCM_SETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TCM_SETUNICODEFORMAT mensaje: establece la marca de formato de caracteres Unicode para el control.'
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- TCM_SETUNICODEFORMAT mensaje Controles de Windows
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b84f944be9bd20897d25e4b111f55ced558a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085853"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="ee501-104">Mensaje \_ SETUNICODEFORMAT de TCM</span><span class="sxs-lookup"><span data-stu-id="ee501-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="ee501-105">Establece la marca de formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="ee501-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="ee501-106">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="ee501-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="ee501-107">Puede enviar este mensaje explícitamente o usar la macro [**TabCtrl \_ SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat)</span><span class="sxs-lookup"><span data-stu-id="ee501-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee501-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee501-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee501-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee501-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee501-110">Determina el juego de caracteres utilizado por el control .</span><span class="sxs-lookup"><span data-stu-id="ee501-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="ee501-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="ee501-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="ee501-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="ee501-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="ee501-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee501-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ee501-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="ee501-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee501-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee501-115">Return value</span></span>

<span data-ttu-id="ee501-116">Devuelve la marca de formato Unicode anterior para el control .</span><span class="sxs-lookup"><span data-stu-id="ee501-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee501-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee501-117">Remarks</span></span>

<span data-ttu-id="ee501-118">Consulte los comentarios de [**CCM \_ SETUNICODEFORMAT para**](ccm-setunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="ee501-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee501-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee501-119">Requirements</span></span>



| <span data-ttu-id="ee501-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee501-120">Requirement</span></span> | <span data-ttu-id="ee501-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ee501-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee501-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee501-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee501-123">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee501-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee501-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee501-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee501-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee501-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee501-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee501-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee501-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="ee501-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee501-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee501-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee501-129">**TCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="ee501-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





