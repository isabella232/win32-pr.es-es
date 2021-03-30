---
title: Mensaje de CBEM_SETUNICODEFORMAT (commctrl. h)
description: Establece la marca del formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- CBEM_SETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89540d4e942b8b705685c13addeeb17adf0b4f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150980"
---
# <a name="cbem_setunicodeformat-message"></a><span data-ttu-id="d9eb3-105">CBEM \_ SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="d9eb3-105">CBEM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="d9eb3-106">Establece la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-106">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="d9eb3-107">Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9eb3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9eb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9eb3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9eb3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9eb3-110">Determina el juego de caracteres utilizado por el control.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="d9eb3-111">Si este valor es distinto de cero, el control usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="d9eb3-112">Si este valor es cero, el control usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="d9eb3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9eb3-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d9eb3-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9eb3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9eb3-115">Return value</span></span>

<span data-ttu-id="d9eb3-116">Devuelve la marca de formato Unicode anterior para el control.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9eb3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9eb3-117">Remarks</span></span>

<span data-ttu-id="d9eb3-118">Vea la sección Comentarios para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9eb3-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9eb3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9eb3-119">Requirements</span></span>



| <span data-ttu-id="d9eb3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9eb3-120">Requirement</span></span> | <span data-ttu-id="d9eb3-121">Value</span><span class="sxs-lookup"><span data-stu-id="d9eb3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9eb3-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9eb3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d9eb3-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9eb3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9eb3-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9eb3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d9eb3-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9eb3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9eb3-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9eb3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9eb3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9eb3-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9eb3-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9eb3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9eb3-129">**CBEM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d9eb3-129">**CBEM\_GETUNICODEFORMAT**</span></span>](cbem-getunicodeformat.md)
</dt> </dl>

 

 





