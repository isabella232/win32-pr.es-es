---
title: Mensaje de TB_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control.
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44b1f65647953702deae5bee6cdd9acc8186e3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802509"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="62abd-104">\_Mensaje GETUNICODEFORMAT TB</span><span class="sxs-lookup"><span data-stu-id="62abd-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="62abd-105">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="62abd-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="62abd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62abd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62abd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62abd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62abd-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="62abd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62abd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62abd-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="62abd-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="62abd-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62abd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62abd-111">Return value</span></span>

<span data-ttu-id="62abd-112">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="62abd-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="62abd-113">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="62abd-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="62abd-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="62abd-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="62abd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62abd-115">Remarks</span></span>

<span data-ttu-id="62abd-116">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="62abd-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="62abd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62abd-117">Requirements</span></span>



| <span data-ttu-id="62abd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="62abd-118">Requirement</span></span> | <span data-ttu-id="62abd-119">Value</span><span class="sxs-lookup"><span data-stu-id="62abd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62abd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62abd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62abd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="62abd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62abd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62abd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62abd-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="62abd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62abd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62abd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="62abd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62abd-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62abd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="62abd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62abd-127">**TB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="62abd-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





