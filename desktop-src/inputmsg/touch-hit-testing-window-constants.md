---
title: Constantes de la ventana de prueba de posicionamiento táctil
description: Indica cómo las ventanas que se registran mediante la función RegisterTouchHitTestingWindow procesan los mensajes para la prueba de posicionamiento táctil.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422500"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="9637f-103">Constantes de la ventana de prueba de posicionamiento táctil</span><span class="sxs-lookup"><span data-stu-id="9637f-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="9637f-104">Indica cómo las ventanas que se registran mediante la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) procesan los mensajes para la prueba de posicionamiento táctil.</span><span class="sxs-lookup"><span data-stu-id="9637f-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="9637f-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="9637f-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="9637f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9637f-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="9637f-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="9637f-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9637f-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) mensajes no se envían a la ventana de destino, sino que se envían a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="9637f-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="9637f-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="9637f-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="9637f-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) mensajes se envían a la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="9637f-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="9637f-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="9637f-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="9637f-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) mensajes no se envían a la ventana de destino ni a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="9637f-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="9637f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9637f-113">Requirements</span></span>



| <span data-ttu-id="9637f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9637f-114">Requirement</span></span> | <span data-ttu-id="9637f-115">Value</span><span class="sxs-lookup"><span data-stu-id="9637f-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9637f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9637f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9637f-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9637f-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9637f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9637f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9637f-119">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9637f-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9637f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9637f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9637f-121"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9637f-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9637f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9637f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9637f-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="9637f-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="9637f-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="9637f-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

