---
title: Mensaje de TB_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.
ms.assetid: d4eec78d-c25b-4b86-9449-64f091cd8501
keywords:
- TB_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf53a6c252690de8f9e001d34c1001d24aac57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905678"
---
# <a name="tb_setunicodeformat-message"></a><span data-ttu-id="0c03b-105">\_Mensaje SETUNICODEFORMAT TB</span><span class="sxs-lookup"><span data-stu-id="0c03b-105">TB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="0c03b-106">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="0c03b-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="0c03b-107">Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="0c03b-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c03b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c03b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c03b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c03b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c03b-110">Determina el juego de caracteres utilizado por el control.</span><span class="sxs-lookup"><span data-stu-id="0c03b-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="0c03b-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="0c03b-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="0c03b-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="0c03b-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="0c03b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c03b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0c03b-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0c03b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c03b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c03b-115">Return value</span></span>

<span data-ttu-id="0c03b-116">Devuelve la marca de formato Unicode anterior para el control.</span><span class="sxs-lookup"><span data-stu-id="0c03b-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c03b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c03b-117">Remarks</span></span>

<span data-ttu-id="0c03b-118">Vea la sección Comentarios para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="0c03b-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c03b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c03b-119">Requirements</span></span>



| <span data-ttu-id="0c03b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c03b-120">Requirement</span></span> | <span data-ttu-id="0c03b-121">Value</span><span class="sxs-lookup"><span data-stu-id="0c03b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c03b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c03b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0c03b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0c03b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c03b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c03b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0c03b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c03b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c03b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c03b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c03b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c03b-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c03b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c03b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c03b-129">**TB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="0c03b-129">**TB\_GETUNICODEFORMAT**</span></span>](tb-getunicodeformat.md)
</dt> </dl>

 

 





