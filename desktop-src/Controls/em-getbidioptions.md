---
title: Mensaje EM_GETBIDIOPTIONS (RichEdit. h)
description: Indica el estado actual de las opciones bidireccionales en el control Rich Edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150408"
---
# <a name="em_getbidioptions-message"></a><span data-ttu-id="f8768-104">\_Mensaje GETBIDIOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="f8768-104">EM\_GETBIDIOPTIONS message</span></span>

<span data-ttu-id="f8768-105">Indica el estado actual de las opciones bidireccionales en el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f8768-105">Indicates the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8768-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8768-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8768-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8768-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8768-108">Este parámetro no se usa; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f8768-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f8768-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8768-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8768-110">Una estructura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que recibe el estado actual de las opciones bidireccionales en el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f8768-110">A [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) structure that receives the current state of the bidirectional options in the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8768-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8768-111">Return value</span></span>

<span data-ttu-id="f8768-112">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f8768-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8768-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8768-113">Remarks</span></span>

<span data-ttu-id="f8768-114">Este mensaje establece los valores de los miembros **wMask** y **wEffects** en el valor del estado actual de las opciones bidireccionales en el control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="f8768-114">This message sets the values of the **wMask** and **wEffects** members to the value of the current state of the bidirectional options in the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8768-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8768-115">Requirements</span></span>



| <span data-ttu-id="f8768-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8768-116">Requirement</span></span> | <span data-ttu-id="f8768-117">Value</span><span class="sxs-lookup"><span data-stu-id="f8768-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8768-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8768-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f8768-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8768-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8768-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8768-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f8768-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8768-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8768-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f8768-122">Redistributable</span></span><br/>          | <span data-ttu-id="f8768-123">Edición enriquecida 3,0</span><span class="sxs-lookup"><span data-stu-id="f8768-123">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f8768-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8768-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8768-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8768-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8768-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8768-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8768-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f8768-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8768-128">**BIDIOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="f8768-128">**BIDIOPTIONS**</span></span>](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[<span data-ttu-id="f8768-129">**\_SETBIDIOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="f8768-129">**EM\_SETBIDIOPTIONS**</span></span>](em-setbidioptions.md)
</dt> </dl>

 

 





