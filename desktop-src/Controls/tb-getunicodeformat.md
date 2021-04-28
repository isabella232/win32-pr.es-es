---
title: TB_GETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TB_GETUNICODEFORMAT mensaje: recupera la marca de formato de caracteres Unicode para el control.'
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT de mensajes controles de Windows
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
ms.openlocfilehash: 4beb5a5ff0b71dd76c85db2788d9dc91aa9f4957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106793"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="bcf75-104">Mensaje \_ GETUNICODEFORMAT de TB</span><span class="sxs-lookup"><span data-stu-id="bcf75-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="bcf75-105">Recupera la marca de formato de caracteres Unicode para el control .</span><span class="sxs-lookup"><span data-stu-id="bcf75-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcf75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcf75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf75-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcf75-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bcf75-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bcf75-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bcf75-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcf75-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bcf75-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bcf75-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf75-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcf75-111">Return value</span></span>

<span data-ttu-id="bcf75-112">Devuelve la marca de formato Unicode del control.</span><span class="sxs-lookup"><span data-stu-id="bcf75-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="bcf75-113">Si este valor es distinto de cero, el control usa caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="bcf75-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="bcf75-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="bcf75-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf75-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcf75-115">Remarks</span></span>

<span data-ttu-id="bcf75-116">Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="bcf75-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf75-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcf75-117">Requirements</span></span>



| <span data-ttu-id="bcf75-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf75-118">Requirement</span></span> | <span data-ttu-id="bcf75-119">Valor</span><span class="sxs-lookup"><span data-stu-id="bcf75-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf75-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf75-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf75-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bcf75-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcf75-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf75-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf75-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bcf75-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcf75-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcf75-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf75-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf75-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf75-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcf75-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf75-127">**TB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="bcf75-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





