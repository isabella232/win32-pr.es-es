---
title: Comportamientos de la prueba de posicionamiento táctil
description: Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los mensajes para las pruebas de posicionamiento táctil mediante Windows que se registran a través de la función RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
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
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720228"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="c3136-103">Comportamientos de la prueba de posicionamiento táctil</span><span class="sxs-lookup"><span data-stu-id="c3136-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="c3136-104">Las aplicaciones o marcos de interfaz de usuario usan las constantes siguientes para identificar cómo se procesan los mensajes para las pruebas de posicionamiento táctil mediante Windows que se registran a través de la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="c3136-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="c3136-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="c3136-105">Constant/value</span></span> | <span data-ttu-id="c3136-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3136-106">Description</span></span> |
|---|---|
| <span data-ttu-id="c3136-107">**TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="c3136-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="c3136-108">Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes no se envían a la ventana de destino, sino que se envían a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="c3136-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="c3136-109">**TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="c3136-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="c3136-110">Indica que se envían [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes a la ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="c3136-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="c3136-111">**TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="c3136-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="c3136-112">Indica que [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) mensajes no se envían a la ventana de destino o a las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="c3136-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="c3136-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3136-113">Requirements</span></span>

| <span data-ttu-id="c3136-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3136-114">Requirement</span></span> | <span data-ttu-id="c3136-115">Value</span><span class="sxs-lookup"><span data-stu-id="c3136-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3136-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3136-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c3136-117">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3136-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c3136-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3136-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c3136-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3136-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c3136-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3136-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3136-121"><dt>Winuser. h</span><span class="sxs-lookup"><span data-stu-id="c3136-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="c3136-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3136-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3136-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="c3136-123">Constants</span></span>](constants.md)
