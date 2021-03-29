---
title: Código de notificación de NM_RCLICK (barra de estado) (commctrl. h)
description: Notifica a la ventana primaria de un control de barra de estado que el usuario ha hace clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- Código de notificación de NM_RCLICK (barra de estado) controles de Windows
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359872"
---
# <a name="nm_rclick-status-bar-notification-code"></a><span data-ttu-id="e4334-105">Código de notificación de NM \_ RCLICK (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="e4334-105">NM\_RCLICK (status bar) notification code</span></span>

<span data-ttu-id="e4334-106">Notifica a la ventana primaria de un control de barra de estado que el usuario ha hace clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="e4334-106">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="e4334-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e4334-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e4334-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4334-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4334-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4334-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4334-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="e4334-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4334-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4334-111">Return value</span></span>

<span data-ttu-id="e4334-112">Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4334-112">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="e4334-113">Devuelve **false** para permitir el procesamiento predeterminado del clic.</span><span class="sxs-lookup"><span data-stu-id="e4334-113">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4334-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4334-114">Requirements</span></span>



| <span data-ttu-id="e4334-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4334-115">Requirement</span></span> | <span data-ttu-id="e4334-116">Value</span><span class="sxs-lookup"><span data-stu-id="e4334-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4334-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4334-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4334-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e4334-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4334-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4334-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4334-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4334-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4334-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4334-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4334-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4334-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





