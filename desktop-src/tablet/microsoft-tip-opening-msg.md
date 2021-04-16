---
description: Notifica a la ventana cuando el panel de entrada de texto se está abriendo.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Mensaje de MICROSOFT_TIP_OPENING_MSG (Peninputpanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718991"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="b33ba-103">\_Mensaje de \_ mensajes de apertura de propinas de Microsoft \_</span><span class="sxs-lookup"><span data-stu-id="b33ba-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="b33ba-104">Notifica a la ventana cuando el panel de entrada de texto se está abriendo.</span><span class="sxs-lookup"><span data-stu-id="b33ba-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="b33ba-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b33ba-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33ba-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b33ba-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b33ba-107">Actualmente no se usa, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b33ba-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b33ba-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b33ba-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b33ba-109">Actualmente no se usa, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b33ba-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33ba-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b33ba-110">Return value</span></span>

<span data-ttu-id="b33ba-111">Las aplicaciones deben llamar a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) después de controlar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b33ba-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="b33ba-112">Vea **DefWindowProc** para obtener información sobre los valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="b33ba-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b33ba-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b33ba-113">Remarks</span></span>

<span data-ttu-id="b33ba-114">Esta notificación le permite saber cuándo se abre el panel de entrada.</span><span class="sxs-lookup"><span data-stu-id="b33ba-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="b33ba-115">Si desea realizar una acción cuando esto sucede, controle el mensaje, realice la operación en el controlador y, a continuación, pase el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="b33ba-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="b33ba-116">Este mensaje también se envía cuando el panel de entrada de texto ya está visible y el usuario cambia del teclado a la máscara de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="b33ba-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b33ba-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33ba-117">Requirements</span></span>



| <span data-ttu-id="b33ba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33ba-118">Requirement</span></span> | <span data-ttu-id="b33ba-119">Value</span><span class="sxs-lookup"><span data-stu-id="b33ba-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b33ba-120">Remoto</span><span class="sxs-lookup"><span data-stu-id="b33ba-120">Client</span></span><br/> | <span data-ttu-id="b33ba-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b33ba-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="b33ba-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b33ba-122">Header</span></span><br/> | <dl> <span data-ttu-id="b33ba-123"><dt>Peninputpanel. h</dt></span><span class="sxs-lookup"><span data-stu-id="b33ba-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 

