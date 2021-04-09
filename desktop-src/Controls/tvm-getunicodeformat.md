---
title: Mensaje de TVM_GETUNICODEFORMAT (commctrl. h)
description: Recupera la marca del formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetUnicodeFormat de TreeView.
ms.assetid: d95f61b6-9ec1-4471-b24b-efe141428747
keywords:
- TVM_GETUNICODEFORMAT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88478d30e8da98ebf2e2325d6152087a14bc066a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079111"
---
# <a name="tvm_getunicodeformat-message"></a><span data-ttu-id="4995d-105">\_Mensaje de GETUNICODEFORMAT TVM</span><span class="sxs-lookup"><span data-stu-id="4995d-105">TVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="4995d-106">Recupera la marca del formato de caracteres Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="4995d-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="4995d-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetUnicodeFormat de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="4995d-107">You can send this message explicitly or use the [**TreeView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4995d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4995d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4995d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4995d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4995d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4995d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4995d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4995d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4995d-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4995d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4995d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4995d-113">Return value</span></span>

<span data-ttu-id="4995d-114">Devuelve la marca de formato Unicode para el control.</span><span class="sxs-lookup"><span data-stu-id="4995d-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="4995d-115">Si este valor es distinto de cero, el control utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="4995d-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="4995d-116">Si este valor es cero, el control usa caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="4995d-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4995d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4995d-117">Remarks</span></span>

<span data-ttu-id="4995d-118">Vea la sección Comentarios para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para obtener una descripción de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4995d-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4995d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4995d-119">Requirements</span></span>



| <span data-ttu-id="4995d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4995d-120">Requirement</span></span> | <span data-ttu-id="4995d-121">Value</span><span class="sxs-lookup"><span data-stu-id="4995d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4995d-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4995d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4995d-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4995d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4995d-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4995d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4995d-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4995d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4995d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4995d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4995d-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4995d-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4995d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4995d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4995d-129">**TVM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="4995d-129">**TVM\_SETUNICODEFORMAT**</span></span>](tvm-setunicodeformat.md)
</dt> </dl>

 

 





