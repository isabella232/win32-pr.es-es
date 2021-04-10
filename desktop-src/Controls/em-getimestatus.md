---
title: Mensaje de EM_GETIMESTATUS (Winuser. h)
description: Obtiene un conjunto de marcas de estado que indican cómo interactúa el control de edición con el editor de métodos de entrada (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150766"
---
# <a name="em_getimestatus-message"></a><span data-ttu-id="d00b0-104">\_Mensaje GETIMESTATUS em</span><span class="sxs-lookup"><span data-stu-id="d00b0-104">EM\_GETIMESTATUS message</span></span>

<span data-ttu-id="d00b0-105">Obtiene un conjunto de marcas de estado que indican cómo interactúa el control de edición con el editor de métodos de entrada (IME).</span><span class="sxs-lookup"><span data-stu-id="d00b0-105">Gets a set of status flags that indicate how the edit control interacts with the Input Method Editor (IME).</span></span>

## <a name="parameters"></a><span data-ttu-id="d00b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d00b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d00b0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d00b0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d00b0-108">Tipo de estado que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d00b0-108">The type of status to retrieve.</span></span> <span data-ttu-id="d00b0-109">Este parámetro puede ser el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="d00b0-109">This parameter can be the following value.</span></span>



| <span data-ttu-id="d00b0-110">Value</span><span class="sxs-lookup"><span data-stu-id="d00b0-110">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="d00b0-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d00b0-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <span data-ttu-id="d00b0-112"><dt>**EMSIS \_ COMPOSITIONSTRING**</dt></span><span class="sxs-lookup"><span data-stu-id="d00b0-112"><dt>**EMSIS\_COMPOSITIONSTRING**</dt></span></span> </dl> | <span data-ttu-id="d00b0-113">Establece el comportamiento para controlar la cadena de composición.</span><span class="sxs-lookup"><span data-stu-id="d00b0-113">Sets behavior for handling the composition string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d00b0-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d00b0-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d00b0-115">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d00b0-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d00b0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d00b0-116">Return value</span></span>

<span data-ttu-id="d00b0-117">Datos específicos del tipo de estado que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d00b0-117">Data specific to the type of status to retrieve.</span></span> <span data-ttu-id="d00b0-118">Con el valor de **EMSIS \_ COMPOSITIONSTRING** para *status*, este valor devuelto es uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d00b0-118">With the **EMSIS\_COMPOSITIONSTRING** value for *status*, this return value is one or more of the following values.</span></span>



| <span data-ttu-id="d00b0-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d00b0-119">Return code</span></span>                                                                                                    | <span data-ttu-id="d00b0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d00b0-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d00b0-121"><dt>**EIMES \_ GETCOMPSTRATONCE**</dt></span><span class="sxs-lookup"><span data-stu-id="d00b0-121"><dt>**EIMES\_GETCOMPSTRATONCE**</dt></span></span> </dl>         | <span data-ttu-id="d00b0-122">Si se establece esta marca, el control de edición enlaza el mensaje de [**\_ \_ composición del IME de WM**](/windows/desktop/Intl/wm-ime-composition) con *fFlags* establecido en los conjuntos de resultados de GC \_ y devuelve la cadena de resultado inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d00b0-122">If this flag is set, the edit control hooks the [**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) message with *fFlags* set to GCS\_RESULTSTR and returns the result string immediately.</span></span> <span data-ttu-id="d00b0-123">Si no se establece esta marca, el control de edición pasa el mensaje de **\_ \_ composición del IME de WM** al procedimiento de ventana predeterminado y procesa la cadena de resultado del mensaje de [**\_ carácter de WM**](/windows/desktop/inputdev/wm-char) ; éste es el comportamiento predeterminado del control de edición.</span><span class="sxs-lookup"><span data-stu-id="d00b0-123">If this flag is not set, the edit control passes the **WM\_IME\_COMPOSITION** message to the default window procedure and processes the result string from the [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message; this is the default behavior of the edit control.</span></span><br/> |
| <dl> <span data-ttu-id="d00b0-124"><dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="d00b0-124"><dt>**EIMES\_CANCELCOMPSTRINFOCUS**</dt></span></span> </dl>     | <span data-ttu-id="d00b0-125">Si se establece esta marca, el control de edición cancela la cadena de composición cuando recibe el mensaje de [**\_ SETFOCUS de WM**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="d00b0-125">If this flag is set, the edit control cancels the composition string when it receives the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span> <span data-ttu-id="d00b0-126">Si no se establece esta marca, el control de edición no cancela la cadena de composición; Éste es el comportamiento predeterminado del control de edición.</span><span class="sxs-lookup"><span data-stu-id="d00b0-126">If this flag is not set, the edit control does not cancel the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="d00b0-127"><dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt></span><span class="sxs-lookup"><span data-stu-id="d00b0-127"><dt>**EIMES\_COMPLETECOMPSTRKILLFOCUS**</dt></span></span> </dl> | <span data-ttu-id="d00b0-128">Si se establece esta marca, el control de edición completa la cadena de composición al recibir el mensaje de [**\_ KILLFOCUS de WM**](/windows/desktop/inputdev/wm-killfocus) .</span><span class="sxs-lookup"><span data-stu-id="d00b0-128">If this flag is set, the edit control completes the composition string upon receiving the [**WM\_KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) message.</span></span> <span data-ttu-id="d00b0-129">Si no se establece esta marca, el control de edición no completa la cadena de composición; Éste es el comportamiento predeterminado del control de edición.</span><span class="sxs-lookup"><span data-stu-id="d00b0-129">If this flag is not set, the edit control does not complete the composition string; this is the default behavior of the edit control.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="d00b0-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d00b0-130">Remarks</span></span>

<span data-ttu-id="d00b0-131">**Edición enriquecida:** No se admite el mensaje **\_ GETIMESTATUS em** .</span><span class="sxs-lookup"><span data-stu-id="d00b0-131">**Rich Edit:** The **EM\_GETIMESTATUS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00b0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d00b0-132">Requirements</span></span>



| <span data-ttu-id="d00b0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d00b0-133">Requirement</span></span> | <span data-ttu-id="d00b0-134">Value</span><span class="sxs-lookup"><span data-stu-id="d00b0-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d00b0-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d00b0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d00b0-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d00b0-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d00b0-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d00b0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d00b0-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d00b0-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d00b0-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d00b0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d00b0-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d00b0-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00b0-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d00b0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00b0-142">**\_SETIMESTATUS em**</span><span class="sxs-lookup"><span data-stu-id="d00b0-142">**EM\_SETIMESTATUS**</span></span>](em-setimestatus.md)
</dt> </dl>

 

