---
title: Mensaje EM_SETIMEMODEBIAS (RichEdit. h)
description: Establezca el sesgo del modo editor de métodos de entrada (IME) para un control Rich Edit.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491212"
---
# <a name="em_setimemodebias-message"></a><span data-ttu-id="171f3-104">\_Mensaje SETIMEMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="171f3-104">EM\_SETIMEMODEBIAS message</span></span>

<span data-ttu-id="171f3-105">Establezca el sesgo del modo editor de métodos de entrada (IME) para un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="171f3-105">Set the Input Method Editor (IME) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="171f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="171f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="171f3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="171f3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="171f3-108">Valor de diferencia del modo IME.</span><span class="sxs-lookup"><span data-stu-id="171f3-108">IME mode bias value.</span></span> <span data-ttu-id="171f3-109">Puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="171f3-109">It can be one of the following.</span></span>



| <span data-ttu-id="171f3-110">Value</span><span class="sxs-lookup"><span data-stu-id="171f3-110">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="171f3-111">Significado</span><span class="sxs-lookup"><span data-stu-id="171f3-111">Meaning</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <span data-ttu-id="171f3-112"><dt>**\_PLAURALCLAUSE SMODE \_ IMF**</dt></span><span class="sxs-lookup"><span data-stu-id="171f3-112"><dt>**IMF\_SMODE\_PLAURALCLAUSE**</dt></span></span> </dl> | <span data-ttu-id="171f3-113">Establece la diferencia entre el modo IME y el nombre.</span><span class="sxs-lookup"><span data-stu-id="171f3-113">Sets the IME mode bias to Name.</span></span><br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <span data-ttu-id="171f3-114"><dt>**IMF \_ SMODE \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="171f3-114"><dt>**IMF\_SMODE\_NONE**</dt></span></span> </dl>                            | <span data-ttu-id="171f3-115">Sin sesgo.</span><span class="sxs-lookup"><span data-stu-id="171f3-115">No bias.</span></span><br/>                        |



 

</dd> <dt>

<span data-ttu-id="171f3-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="171f3-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="171f3-117">Debe ser el mismo valor que *wParam*.</span><span class="sxs-lookup"><span data-stu-id="171f3-117">This must be the same value as *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="171f3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="171f3-118">Return value</span></span>

<span data-ttu-id="171f3-119">Este mensaje devuelve el nuevo valor de diferencia del modo IME.</span><span class="sxs-lookup"><span data-stu-id="171f3-119">This message returns the new IME mode bias setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="171f3-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="171f3-120">Remarks</span></span>

<span data-ttu-id="171f3-121">Cuando el IME genera una lista de opciones alternativas para un juego de caracteres, este mensaje establece los criterios por los que algunas de las opciones aparecerán en la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="171f3-121">When the IME generates a list of alternative choices for a set of characters, this message sets the criteria by which some of the choices will appear at the top of the list.</span></span>

<span data-ttu-id="171f3-122">Para establecer la diferencia del modo de Text Services Framework (TSF), use [**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md).</span><span class="sxs-lookup"><span data-stu-id="171f3-122">To set the Text Services Framework (TSF) mode bias, use [**EM\_SETCTFMODEBIAS**](em-setctfmodebias.md).</span></span>

<span data-ttu-id="171f3-123">La aplicación debe llamar a [**em \_ ISIME**](em-isime.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="171f3-123">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="171f3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="171f3-124">Requirements</span></span>



| <span data-ttu-id="171f3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="171f3-125">Requirement</span></span> | <span data-ttu-id="171f3-126">Value</span><span class="sxs-lookup"><span data-stu-id="171f3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="171f3-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="171f3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="171f3-128">Solo aplicaciones de escritorio de Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="171f3-128">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="171f3-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="171f3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="171f3-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="171f3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="171f3-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="171f3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="171f3-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="171f3-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="171f3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="171f3-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="171f3-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="171f3-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="171f3-135">**\_ISIME em**</span><span class="sxs-lookup"><span data-stu-id="171f3-135">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

[<span data-ttu-id="171f3-136">**\_SETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="171f3-136">**EM\_SETCTFMODEBIAS**</span></span>](em-setctfmodebias.md)
</dt> </dl>

 

 





