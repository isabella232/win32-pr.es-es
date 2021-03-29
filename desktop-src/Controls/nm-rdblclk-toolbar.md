---
title: Código de notificación de NM_RDBLCLK (barra de herramientas) (commctrl. h)
description: Notifica a la ventana primaria de un control que el usuario ha doble clic con el botón secundario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0281a687-3f1c-4fc1-bf1d-19c7ac920cd3
keywords:
- Código de notificación de NM_RDBLCLK (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec2129b6400c60bd59e441ff8af2083e781ba22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492148"
---
# <a name="nm_rdblclk-toolbar-notification-code"></a><span data-ttu-id="3cd26-105">NM \_ RDBLCLK (barra de herramientas) código de notificación</span><span class="sxs-lookup"><span data-stu-id="3cd26-105">NM\_RDBLCLK (toolbar) notification code</span></span>

<span data-ttu-id="3cd26-106">Notifica a la ventana primaria de un control que el usuario ha doble clic con el botón secundario del mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="3cd26-106">Notifies a control's parent window that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="3cd26-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3cd26-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3cd26-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3cd26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cd26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd26-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="3cd26-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="3cd26-111">Si se hizo clic con el mouse en un elemento de la barra de herramientas, el miembro **dwItemSpec** contiene el identificador del elemento y el miembro **dwItemData** contiene los datos del elemento.</span><span class="sxs-lookup"><span data-stu-id="3cd26-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="3cd26-112">Si se hizo clic con el mouse en un separador o en un espacio en blanco en la barra de herramientas, el miembro **dwItemSpec** contendrá-1.</span><span class="sxs-lookup"><span data-stu-id="3cd26-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd26-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3cd26-113">Return value</span></span>

<span data-ttu-id="3cd26-114">Devuelve **false** para permitir que el control de barra de herramientas realice el procesamiento predeterminado del evento, o bien **true** para evitar que el control procese el evento.</span><span class="sxs-lookup"><span data-stu-id="3cd26-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd26-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cd26-115">Requirements</span></span>



| <span data-ttu-id="3cd26-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cd26-116">Requirement</span></span> | <span data-ttu-id="3cd26-117">Value</span><span class="sxs-lookup"><span data-stu-id="3cd26-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd26-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cd26-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3cd26-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3cd26-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cd26-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cd26-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3cd26-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3cd26-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cd26-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3cd26-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cd26-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd26-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





