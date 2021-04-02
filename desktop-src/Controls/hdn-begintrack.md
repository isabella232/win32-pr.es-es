---
title: Código de notificación de HDN_BEGINTRACK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha empezado a arrastrar un divisor en el control (es decir, el usuario ha presionado el botón primario del mouse mientras el cursor se encuentra en un divisor del control de encabezado).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151287"
---
# <a name="hdn_begintrack-notification-code"></a><span data-ttu-id="ff752-104">Código de notificación de BEGINTRACK de HDN \_</span><span class="sxs-lookup"><span data-stu-id="ff752-104">HDN\_BEGINTRACK notification code</span></span>

<span data-ttu-id="ff752-105">Notifica a la ventana primaria de un control de encabezado que el usuario ha empezado a arrastrar un divisor en el control (es decir, el usuario ha presionado el botón primario del mouse mientras el cursor se encuentra en un divisor del control de encabezado).</span><span class="sxs-lookup"><span data-stu-id="ff752-105">Notifies a header control's parent window that the user has begun dragging a divider in the control (that is, the user has pressed the left mouse button while the mouse cursor is on a divider in the header control).</span></span> <span data-ttu-id="ff752-106">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ff752-106">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ff752-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff752-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff752-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff752-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff752-109">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se va a arrastrar.</span><span class="sxs-lookup"><span data-stu-id="ff752-109">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is to be dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff752-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff752-110">Return value</span></span>

<span data-ttu-id="ff752-111">Devuelve **false** para permitir el seguimiento del divisor o **true** para evitar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ff752-111">Returns **FALSE** to allow tracking of the divider, or **TRUE** to prevent tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff752-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff752-112">Requirements</span></span>



| <span data-ttu-id="ff752-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff752-113">Requirement</span></span> | <span data-ttu-id="ff752-114">Value</span><span class="sxs-lookup"><span data-stu-id="ff752-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff752-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff752-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ff752-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ff752-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff752-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff752-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ff752-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff752-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff752-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff752-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff752-120"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff752-120"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ff752-121">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="ff752-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ff752-122">**HDN \_ BEGINTRACKW** (Unicode) y **HDN \_ BEGINTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ff752-122">**HDN\_BEGINTRACKW** (Unicode) and **HDN\_BEGINTRACKA** (ANSI)</span></span><br/>             |



 

 





