---
title: Código de notificación de HDN_ENDTRACK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha terminado de arrastrar un divisor. Este código de notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- HDN_ENDTRACK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078946"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="fc5d3-105">Código de notificación de ENDTRACK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="fc5d3-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="fc5d3-106">Notifica a la ventana primaria de un control de encabezado que el usuario ha terminado de arrastrar un divisor.</span><span class="sxs-lookup"><span data-stu-id="fc5d3-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="fc5d3-107">Este código de notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5d3-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fc5d3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc5d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc5d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc5d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc5d3-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se arrastró.</span><span class="sxs-lookup"><span data-stu-id="fc5d3-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc5d3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc5d3-111">Return value</span></span>

<span data-ttu-id="fc5d3-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc5d3-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5d3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc5d3-113">Requirements</span></span>



| <span data-ttu-id="fc5d3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc5d3-114">Requirement</span></span> | <span data-ttu-id="fc5d3-115">Value</span><span class="sxs-lookup"><span data-stu-id="fc5d3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5d3-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc5d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5d3-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fc5d3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc5d3-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc5d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5d3-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc5d3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc5d3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc5d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc5d3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc5d3-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fc5d3-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="fc5d3-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fc5d3-123">**HDN \_ ENDTRACKW** (Unicode) y **HDN \_ ENDTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fc5d3-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 





