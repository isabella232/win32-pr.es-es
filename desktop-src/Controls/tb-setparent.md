---
title: Mensaje de TB_SETPARENT (commctrl. h)
description: Establece la ventana en la que el control de barra de herramientas envía mensajes de notificación.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905555"
---
# <a name="tb_setparent-message"></a><span data-ttu-id="dcd87-104">\_Message TB SETPARENT</span><span class="sxs-lookup"><span data-stu-id="dcd87-104">TB\_SETPARENT message</span></span>

<span data-ttu-id="dcd87-105">Establece la ventana en la que el control de barra de herramientas envía mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="dcd87-105">Sets the window to which the toolbar control sends notification messages.</span></span>

## <a name="parameters"></a><span data-ttu-id="dcd87-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcd87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd87-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcd87-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd87-108">Identificador de la ventana para recibir mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="dcd87-108">Handle to the window to receive notification messages.</span></span>

</dd> <dt>

<span data-ttu-id="dcd87-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcd87-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dcd87-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dcd87-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcd87-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcd87-111">Return value</span></span>

<span data-ttu-id="dcd87-112">El valor devuelto es un identificador de la ventana de notificación anterior, o **null** si no hay ninguna ventana de notificación anterior.</span><span class="sxs-lookup"><span data-stu-id="dcd87-112">The return value is a handle to the previous notification window, or **NULL** if there is no previous notification window.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcd87-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcd87-113">Remarks</span></span>

<span data-ttu-id="dcd87-114">El mensaje del objeto **\_ SETPARENT de TB** no cambia la ventana primaria que se especificó cuando se creó el control.</span><span class="sxs-lookup"><span data-stu-id="dcd87-114">The **TB\_SETPARENT** message does not change the parent window that was specified when the control was created.</span></span> <span data-ttu-id="dcd87-115">La llamada a la función [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para un control de barra de herramientas devolverá la ventana primaria real, no la ventana especificada en **TB \_ SETPARENT**.</span><span class="sxs-lookup"><span data-stu-id="dcd87-115">Calling the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function for a toolbar control will return the actual parent window, not the window specified in **TB\_SETPARENT**.</span></span> <span data-ttu-id="dcd87-116">Para cambiar la ventana primaria del control, llame a la función [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) .</span><span class="sxs-lookup"><span data-stu-id="dcd87-116">To change the control's parent window, call the [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcd87-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcd87-117">Requirements</span></span>



| <span data-ttu-id="dcd87-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcd87-118">Requirement</span></span> | <span data-ttu-id="dcd87-119">Value</span><span class="sxs-lookup"><span data-stu-id="dcd87-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcd87-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcd87-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd87-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dcd87-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcd87-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcd87-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd87-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcd87-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dcd87-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcd87-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcd87-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcd87-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

