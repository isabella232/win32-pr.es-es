---
title: Mensaje de SB_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control.
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT controles de mensajes de Windows
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
ms.openlocfilehash: 9dbb639a04f0a40d9d5e11b938aaadbcc8b4c730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534828"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="a816d-104">\_Mensaje GETUNICODEFORMAT de SB</span><span class="sxs-lookup"><span data-stu-id="a816d-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="a816d-105">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="a816d-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a816d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a816d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a816d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a816d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a816d-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a816d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a816d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a816d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a816d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a816d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a816d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a816d-111">Return value</span></span>

<span data-ttu-id="a816d-112">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="a816d-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="a816d-113">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a816d-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="a816d-114">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="a816d-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a816d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a816d-115">Remarks</span></span>

<span data-ttu-id="a816d-116">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="a816d-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a816d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a816d-117">Requirements</span></span>



| <span data-ttu-id="a816d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a816d-118">Requirement</span></span> | <span data-ttu-id="a816d-119">Value</span><span class="sxs-lookup"><span data-stu-id="a816d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a816d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a816d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a816d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a816d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a816d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a816d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a816d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a816d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a816d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a816d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a816d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a816d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a816d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a816d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a816d-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="a816d-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





