---
title: Código de notificación de MCN_VIEWCHANGE (commctrl. h)
description: Se envía por un control de calendario mensual cuando cambia la vista actual. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489442"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="7d733-105">Código de notificación de VIEWCHANGE de MCN \_</span><span class="sxs-lookup"><span data-stu-id="7d733-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="7d733-106">Se envía por un control de calendario mensual cuando cambia la vista actual.</span><span class="sxs-lookup"><span data-stu-id="7d733-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="7d733-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7d733-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7d733-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d733-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d733-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d733-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d733-110">Puntero a una estructura [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) que contiene información sobre la vista actual.</span><span class="sxs-lookup"><span data-stu-id="7d733-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d733-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d733-111">Return value</span></span>

<span data-ttu-id="7d733-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7d733-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d733-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d733-113">Requirements</span></span>



| <span data-ttu-id="7d733-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d733-114">Requirement</span></span> | <span data-ttu-id="7d733-115">Value</span><span class="sxs-lookup"><span data-stu-id="7d733-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d733-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d733-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7d733-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7d733-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d733-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d733-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7d733-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d733-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d733-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d733-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d733-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d733-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





