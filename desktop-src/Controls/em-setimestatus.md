---
title: Mensaje de EM_SETIMESTATUS (Winuser. h)
description: Establece las marcas de estado que determinan cómo interactúa un control de edición con el editor de métodos de entrada (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802659"
---
# <a name="em_setimestatus-message"></a><span data-ttu-id="8095e-104">\_Mensaje SETIMESTATUS em</span><span class="sxs-lookup"><span data-stu-id="8095e-104">EM\_SETIMESTATUS message</span></span>

<span data-ttu-id="8095e-105">Establece las marcas de estado que determinan cómo interactúa un control de edición con el editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="8095e-105">Sets the status flags that determine how an edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="8095e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8095e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8095e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8095e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8095e-108">Tipo de estado que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="8095e-108">The type of status to set.</span></span> <span data-ttu-id="8095e-109">Este parámetro puede ser el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="8095e-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="8095e-110">Value</span><span class="sxs-lookup"><span data-stu-id="8095e-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="8095e-111">Significado</span><span class="sxs-lookup"><span data-stu-id="8095e-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="8095e-112"><dt>**EMSIS \_ COMPOSITIONSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="8095e-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="8095e-113">Establece el comportamiento de la cadena de composición de control.</span><span class="sxs-lookup"><span data-stu-id="8095e-113">Sets behavior for the handling composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8095e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8095e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8095e-115">Datos específicos del tipo de estado.</span><span class="sxs-lookup"><span data-stu-id="8095e-115">Data specific to the status type.</span></span> <span data-ttu-id="8095e-116">Si *wParam* es **EMSIS \_ COMPOSITIONSTRING**, este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8095e-116">If *wParam* is **EMSIS\_COMPOSITIONSTRING**, this parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8095e-117">Value</span><span class="sxs-lookup"><span data-stu-id="8095e-117">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="8095e-118">Significado</span><span class="sxs-lookup"><span data-stu-id="8095e-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <span data-ttu-id="8095e-119"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="8095e-119"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>                         | <span data-ttu-id="8095e-120">Si se establece esta marca, el control de edición enlaza el mensaje de [**\_ \_ composición del IME de WM**](/windows/desktop/Intl/wm-ime-composition) con *lParam* establecido en el valor de RESULTSTR de GC \_ y devuelve la cadena de resultado inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8095e-120">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *lParam* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="8095e-121">Si no se establece esta marca, el control de edición pasa el mensaje de **\_ \_ composición del IME de WM** al procedimiento de ventana predeterminado y controla la cadena de resultado del mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) ; éste es el comportamiento predeterminado del control de edición.</span><span class="sxs-lookup"><span data-stu-id="8095e-121">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and handles the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <span data-ttu-id="8095e-122"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="8095e-122"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>             | <span data-ttu-id="8095e-123">Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="8095e-123">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="8095e-124">Si no se establece esta marca, el control de edición no cancela la cadena de composición; Éste es el comportamiento predeterminado del control de edición.</span><span class="sxs-lookup"><span data-stu-id="8095e-124">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <span data-ttu-id="8095e-125"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="8095e-125"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="8095e-126">Si se establece esta marca, el control de edición completa la cadena de composición al recibir el mensaje de [**\_ KILLFOCUS de WM**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="8095e-126">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="8095e-127">Si no se establece esta marca, el control de edición no completa la cadena de composición; Éste es el comportamiento predeterminado del control de edición.</span><span class="sxs-lookup"><span data-stu-id="8095e-127">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8095e-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8095e-128">Return value</span></span>

<span data-ttu-id="8095e-129">Devuelve el valor anterior del parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="8095e-129">Returns the previous value of the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="8095e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8095e-130">Remarks</span></span>

<span data-ttu-id="8095e-131">**Edición enriquecida:** No se admite el mensaje **\_ SETIMESTATUS em** .</span><span class="sxs-lookup"><span data-stu-id="8095e-131">**Rich Edit:** The **EM\_SETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8095e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8095e-132">Requirements</span></span>



| <span data-ttu-id="8095e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8095e-133">Requirement</span></span> | <span data-ttu-id="8095e-134">Value</span><span class="sxs-lookup"><span data-stu-id="8095e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8095e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8095e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8095e-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8095e-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8095e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8095e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8095e-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8095e-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8095e-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8095e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8095e-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8095e-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8095e-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8095e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8095e-142">**\_GETIMESTATUS em**</span><span class="sxs-lookup"><span data-stu-id="8095e-142">**EM\_GETIMESTATUS**</span></span>](em-getimestatus.md)
</dt> </dl>

 

