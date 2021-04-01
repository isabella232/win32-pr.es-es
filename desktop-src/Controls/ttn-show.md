---
title: Código de notificación de TTN_SHOW (commctrl. h)
description: Notifica a la ventana propietaria que un control de información sobre herramientas está a punto de mostrarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996460"
---
# <a name="ttn_show-notification-code"></a><span data-ttu-id="ec78b-105">TTN \_ Mostrar código de notificación</span><span class="sxs-lookup"><span data-stu-id="ec78b-105">TTN\_SHOW notification code</span></span>

<span data-ttu-id="ec78b-106">Notifica a la ventana propietaria que un control de información sobre herramientas está a punto de mostrarse.</span><span class="sxs-lookup"><span data-stu-id="ec78b-106">Notifies the owner window that a tooltip control is about to be displayed.</span></span> <span data-ttu-id="ec78b-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ec78b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ec78b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec78b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec78b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec78b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec78b-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="ec78b-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec78b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec78b-111">Return value</span></span>

<span data-ttu-id="ec78b-112">[Versión 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="ec78b-112">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="ec78b-113">Para mostrar la información sobre herramientas en su ubicación predeterminada, devuelva cero.</span><span class="sxs-lookup"><span data-stu-id="ec78b-113">To display the tooltip in its default location, return zero.</span></span> <span data-ttu-id="ec78b-114">Para personalizar la posición de la información sobre herramientas, cambie la posición de la ventana de información sobre herramientas con la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) y devuelva **true**.</span><span class="sxs-lookup"><span data-stu-id="ec78b-114">To customize the tooltip position, reposition the tooltip window with the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function and return **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="ec78b-115">En el caso de las versiones anteriores a 4,70, no hay ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ec78b-115">For versions earlier than 4.70, there is no return value.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="ec78b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec78b-116">Remarks</span></span>

<span data-ttu-id="ec78b-117">Un rectángulo de la ventana de información sobre herramientas es algo más grande que su rectángulo de presentación de texto y su origen está desplazado hacia arriba y hacia la izquierda.</span><span class="sxs-lookup"><span data-stu-id="ec78b-117">A tooltip window rectangle is somewhat larger than its text display rectangle, and its origin is offset up and to the left.</span></span> <span data-ttu-id="ec78b-118">Si necesita colocar con precisión el rectángulo de presentación de texto de una información sobre herramientas, el mensaje [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) convierte un rectángulo de presentación de texto en el rectángulo de la ventana de información sobre herramientas correspondiente y viceversa.</span><span class="sxs-lookup"><span data-stu-id="ec78b-118">If you need to accurately position the text display rectangle of a tooltip, the [**TTM\_ADJUSTRECT**](ttm-adjustrect.md) message converts a text display rectangle into the corresponding tooltip window rectangle and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec78b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec78b-119">Requirements</span></span>



| <span data-ttu-id="ec78b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec78b-120">Requirement</span></span> | <span data-ttu-id="ec78b-121">Value</span><span class="sxs-lookup"><span data-stu-id="ec78b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec78b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec78b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec78b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ec78b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec78b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec78b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec78b-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec78b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec78b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec78b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec78b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec78b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

