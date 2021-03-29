---
title: Código de notificación de HDN_TRACK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario está arrastrando un divisor en el control de encabezado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905403"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="41f90-105">Código de notificación de seguimiento de HDN \_</span><span class="sxs-lookup"><span data-stu-id="41f90-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="41f90-106">Notifica a la ventana primaria de un control de encabezado que el usuario está arrastrando un divisor en el control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="41f90-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="41f90-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="41f90-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="41f90-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41f90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41f90-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41f90-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41f90-110">Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se está arrastrando.</span><span class="sxs-lookup"><span data-stu-id="41f90-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41f90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41f90-111">Return value</span></span>

<span data-ttu-id="41f90-112">Devuelve **false** para seguir realizando el seguimiento del divisor o en **true** para finalizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="41f90-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f90-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41f90-113">Requirements</span></span>



| <span data-ttu-id="41f90-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f90-114">Requirement</span></span> | <span data-ttu-id="41f90-115">Value</span><span class="sxs-lookup"><span data-stu-id="41f90-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41f90-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41f90-116">Minimum supported client</span></span><br/> | <span data-ttu-id="41f90-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="41f90-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="41f90-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41f90-118">Minimum supported server</span></span><br/> | <span data-ttu-id="41f90-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="41f90-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41f90-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41f90-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f90-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f90-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="41f90-122">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="41f90-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="41f90-123">**HDN \_ TRACKW** (Unicode) y **HDN \_ TRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="41f90-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 





