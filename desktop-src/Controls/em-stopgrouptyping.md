---
title: Mensaje EM_STOPGROUPTYPING (RichEdit. h)
description: Detiene un control Rich Edit para recopilar acciones de escritura adicionales en la acción de deshacer actual. El control almacena la siguiente acción de escritura, si existe, en una nueva acción en la cola de deshacer.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802077"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="1956b-105">\_Mensaje STOPGROUPTYPING em</span><span class="sxs-lookup"><span data-stu-id="1956b-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="1956b-106">Detiene un control Rich Edit para recopilar acciones de escritura adicionales en la acción de deshacer actual.</span><span class="sxs-lookup"><span data-stu-id="1956b-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="1956b-107">El control almacena la siguiente acción de escritura, si existe, en una nueva acción en la cola de deshacer.</span><span class="sxs-lookup"><span data-stu-id="1956b-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="1956b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1956b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1956b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1956b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1956b-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1956b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1956b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1956b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1956b-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1956b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1956b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1956b-113">Return value</span></span>

<span data-ttu-id="1956b-114">El valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="1956b-114">The return value is zero.</span></span> <span data-ttu-id="1956b-115">No se puede producir un error en este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1956b-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="1956b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1956b-116">Remarks</span></span>

<span data-ttu-id="1956b-117">Un control Rich Edit agrupa acciones de escritura consecutivas, incluidos los caracteres eliminados mediante la tecla **retroceso** , en una sola acción de deshacer hasta que se produce uno de los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="1956b-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="1956b-118">El control recibe un **mensaje \_ STOPGROUPTYPING em** .</span><span class="sxs-lookup"><span data-stu-id="1956b-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="1956b-119">El control pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="1956b-119">The control loses focus.</span></span>
-   <span data-ttu-id="1956b-120">El usuario mueve la selección actual, ya sea mediante las teclas de dirección o haciendo clic con el mouse.</span><span class="sxs-lookup"><span data-stu-id="1956b-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="1956b-121">El usuario presiona la tecla **Supr** .</span><span class="sxs-lookup"><span data-stu-id="1956b-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="1956b-122">El usuario realiza cualquier otra acción, como una operación de pegar que **no** implica la escritura.</span><span class="sxs-lookup"><span data-stu-id="1956b-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="1956b-123">Puede enviar el mensaje **\_ STOPGROUPTYPING em** para dividir acciones de escritura consecutivas en grupos de deshacer más pequeños.</span><span class="sxs-lookup"><span data-stu-id="1956b-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="1956b-124">Por ejemplo, podría enviar **em \_ STOPGROUPTYPING** después de cada carácter o en cada separación de palabras.</span><span class="sxs-lookup"><span data-stu-id="1956b-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="1956b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1956b-125">Requirements</span></span>



| <span data-ttu-id="1956b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1956b-126">Requirement</span></span> | <span data-ttu-id="1956b-127">Value</span><span class="sxs-lookup"><span data-stu-id="1956b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1956b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1956b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1956b-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1956b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1956b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1956b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1956b-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1956b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1956b-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1956b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1956b-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1956b-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1956b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1956b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1956b-135">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="1956b-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





