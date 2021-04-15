---
title: Mensaje de TTM_RELAYEVENT (commctrl. h)
description: Pasa un mensaje del mouse a un control ToolTip para su procesamiento.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362249"
---
# <a name="ttm_relayevent-message"></a><span data-ttu-id="fb1fd-104">TTM \_ RELAYEVENT</span><span class="sxs-lookup"><span data-stu-id="fb1fd-104">TTM\_RELAYEVENT message</span></span>

<span data-ttu-id="fb1fd-105">Pasa un mensaje del mouse a un control ToolTip para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="fb1fd-105">Passes a mouse message to a tooltip control for processing.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb1fd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb1fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb1fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fb1fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1fd-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fb1fd-108">Must be zero.</span></span> <span data-ttu-id="fb1fd-109">**Windows 7 y versiones posteriores:** Si la posición de la información sobre herramientas se desplaza desde la posición del cursor (para que no esté obstruida por un dedo o un dispositivo señalador), este parámetro puede contener información adicional tomada del mensaje de [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="fb1fd-109">**Windows 7 and later:** If the position of the tooltip is offset from the cursor position (in order not be obstructed by a finger or pointing device), this parameter can contain extra information taken from the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="fb1fd-110">Recupere esta información adicional con [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span><span class="sxs-lookup"><span data-stu-id="fb1fd-110">Retrieve this extra information with [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).</span></span>

</dd> <dt>

<span data-ttu-id="fb1fd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fb1fd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fb1fd-112">Puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje que se va a retransmitir.</span><span class="sxs-lookup"><span data-stu-id="fb1fd-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to relay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb1fd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb1fd-113">Return value</span></span>

<span data-ttu-id="fb1fd-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fb1fd-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb1fd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb1fd-115">Remarks</span></span>

<span data-ttu-id="fb1fd-116">Un control ToolTip solo procesa los mensajes siguientes que le pasa el mensaje **\_ RELAYEVENT de TTM** :</span><span class="sxs-lookup"><span data-stu-id="fb1fd-116">A tooltip control processes only the following messages passed to it by the **TTM\_RELAYEVENT** message:</span></span>

-   <span data-ttu-id="fb1fd-117">LBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-117">WM\_LBUTTONDOWN</span></span>
-   <span data-ttu-id="fb1fd-118">LBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-118">WM\_LBUTTONUP</span></span>
-   <span data-ttu-id="fb1fd-119">MBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-119">WM\_MBUTTONDOWN</span></span>
-   <span data-ttu-id="fb1fd-120">MBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-120">WM\_MBUTTONUP</span></span>
-   <span data-ttu-id="fb1fd-121">MOUSEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-121">WM\_MOUSEMOVE</span></span>
-   <span data-ttu-id="fb1fd-122">NCMOUSEMOVE de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-122">WM\_NCMOUSEMOVE</span></span>
-   <span data-ttu-id="fb1fd-123">RBUTTONDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-123">WM\_RBUTTONDOWN</span></span>
-   <span data-ttu-id="fb1fd-124">RBUTTONUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="fb1fd-124">WM\_RBUTTONUP</span></span>

<span data-ttu-id="fb1fd-125">El resto de los mensajes se omiten.</span><span class="sxs-lookup"><span data-stu-id="fb1fd-125">All other messages are ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1fd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1fd-126">Requirements</span></span>



| <span data-ttu-id="fb1fd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1fd-127">Requirement</span></span> | <span data-ttu-id="fb1fd-128">Value</span><span class="sxs-lookup"><span data-stu-id="fb1fd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1fd-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1fd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb1fd-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb1fd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb1fd-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb1fd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb1fd-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb1fd-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb1fd-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb1fd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb1fd-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb1fd-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

