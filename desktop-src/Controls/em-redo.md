---
title: Mensaje EM_REDO (RichEdit. h)
description: Envía un \_ mensaje de rehacer em a un control Rich Edit para rehacer la siguiente acción en la cola de puesta al día del control.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- EM_REDO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491494"
---
# <a name="em_redo-message"></a><span data-ttu-id="f9fc6-104">\_Mensaje de rehacer em</span><span class="sxs-lookup"><span data-stu-id="f9fc6-104">EM\_REDO message</span></span>

<span data-ttu-id="f9fc6-105">Envía un mensaje de **\_ rehacer em** a un control Rich Edit para rehacer la siguiente acción en la cola de puesta al día del control.</span><span class="sxs-lookup"><span data-stu-id="f9fc6-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9fc6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9fc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9fc6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9fc6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fc6-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f9fc6-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f9fc6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9fc6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9fc6-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f9fc6-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9fc6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9fc6-111">Return value</span></span>

<span data-ttu-id="f9fc6-112">Si la operación de **rehacer** se realiza correctamente, el valor devuelto es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f9fc6-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f9fc6-113">Si se produce un error en la operación de **rehacer** , el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f9fc6-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9fc6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9fc6-114">Remarks</span></span>

<span data-ttu-id="f9fc6-115">Para determinar si hay alguna acción en la cola de rehacer del control, envíe el mensaje [**\_ CANREDO em**](em-canredo.md) .</span><span class="sxs-lookup"><span data-stu-id="f9fc6-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9fc6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9fc6-116">Requirements</span></span>



| <span data-ttu-id="f9fc6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9fc6-117">Requirement</span></span> | <span data-ttu-id="f9fc6-118">Value</span><span class="sxs-lookup"><span data-stu-id="f9fc6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9fc6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fc6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f9fc6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f9fc6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9fc6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9fc6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f9fc6-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f9fc6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9fc6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9fc6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9fc6-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9fc6-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9fc6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9fc6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9fc6-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f9fc6-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f9fc6-127">**de \_ em**</span><span class="sxs-lookup"><span data-stu-id="f9fc6-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="f9fc6-128">**\_GETREDONAME em**</span><span class="sxs-lookup"><span data-stu-id="f9fc6-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="f9fc6-129">**\_GETUNDONAME em**</span><span class="sxs-lookup"><span data-stu-id="f9fc6-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="f9fc6-130">**deshacer EM \_**</span><span class="sxs-lookup"><span data-stu-id="f9fc6-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





