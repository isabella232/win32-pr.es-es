---
title: Código de notificación de NM_DBLCLK (barra de estado) (commctrl. h)
description: Notifica a la ventana primaria de un control de barra de estado que el usuario ha haga doble clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- Código de notificación de NM_DBLCLK (barra de estado) controles de Windows
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28866effbc4143dc9d0d5a3800f88711c99f88db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995931"
---
# <a name="nm_dblclk-status-bar-notification-code"></a><span data-ttu-id="8cbd8-105">Código de notificación de NM \_ DBLCLK (barra de estado)</span><span class="sxs-lookup"><span data-stu-id="8cbd8-105">NM\_DBLCLK (status bar) notification code</span></span>

<span data-ttu-id="8cbd8-106">Notifica a la ventana primaria de un control de barra de estado que el usuario ha haga doble clic en el botón primario del mouse dentro del control.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-106">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="8cbd8-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8cbd8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8cbd8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cbd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cbd8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cbd8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8cbd8-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="8cbd8-111">El miembro **dwItemSpec** contiene el índice de la sección en la que se hizo clic.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cbd8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cbd8-112">Return value</span></span>

<span data-ttu-id="8cbd8-113">Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="8cbd8-114">Devuelve **false** para permitir el procesamiento predeterminado del clic.</span><span class="sxs-lookup"><span data-stu-id="8cbd8-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cbd8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cbd8-115">Requirements</span></span>



| <span data-ttu-id="8cbd8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cbd8-116">Requirement</span></span> | <span data-ttu-id="8cbd8-117">Value</span><span class="sxs-lookup"><span data-stu-id="8cbd8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cbd8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cbd8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8cbd8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8cbd8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cbd8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cbd8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8cbd8-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8cbd8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cbd8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cbd8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cbd8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cbd8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





