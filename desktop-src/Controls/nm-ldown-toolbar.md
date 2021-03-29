---
title: Código de notificación de NM_LDOWN (barra de herramientas) (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que se ha presionado el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- Código de notificación de NM_LDOWN (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60f1f05d85aa8885acf31a36098056d68612ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904991"
---
# <a name="nm_ldown-toolbar-notification-code"></a><span data-ttu-id="aeeb4-105">NM \_ LDOWN (barra de herramientas) código de notificación</span><span class="sxs-lookup"><span data-stu-id="aeeb4-105">NM\_LDOWN (toolbar) notification code</span></span>

<span data-ttu-id="aeeb4-106">Notifica a la ventana primaria de una barra de herramientas que se ha presionado el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="aeeb4-106">Notifies a toolbar's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="aeeb4-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aeeb4-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="aeeb4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aeeb4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeeb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aeeb4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aeeb4-110">Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="aeeb4-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about this notification code.</span></span> <span data-ttu-id="aeeb4-111">Si se hizo clic con el mouse en un elemento de la barra de herramientas, el miembro **dwItemSpec** contiene el identificador del elemento y el miembro **dwItemData** contiene los datos del elemento.</span><span class="sxs-lookup"><span data-stu-id="aeeb4-111">If the mouse was clicked on a toolbar item, the **dwItemSpec** member contains the item identifier and the **dwItemData** member contains the item data.</span></span> <span data-ttu-id="aeeb4-112">Si se hizo clic con el mouse en un separador o en un espacio en blanco en la barra de herramientas, el miembro **dwItemSpec** contendrá-1.</span><span class="sxs-lookup"><span data-stu-id="aeeb4-112">If the mouse was clicked on a separator or white space in the toolbar, the **dwItemSpec** member will contain -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeeb4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aeeb4-113">Return value</span></span>

<span data-ttu-id="aeeb4-114">Devuelve **false** para permitir que el control de barra de herramientas realice el procesamiento predeterminado del evento, o bien **true** para evitar que el control procese el evento.</span><span class="sxs-lookup"><span data-stu-id="aeeb4-114">Returns **FALSE** to allow the toolbar control to perform default processing of the event, or **TRUE** to prevent the control from processing the event.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeeb4-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aeeb4-115">Remarks</span></span>

<span data-ttu-id="aeeb4-116">Esta notificación se envía una vez enviado el código de notificación de la [ \_ lista desplegable TBN](tbn-dropdown.md) .</span><span class="sxs-lookup"><span data-stu-id="aeeb4-116">This notification is sent after the [TBN\_DROPDOWN](tbn-dropdown.md) notification code has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeeb4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeeb4-117">Requirements</span></span>



| <span data-ttu-id="aeeb4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeeb4-118">Requirement</span></span> | <span data-ttu-id="aeeb4-119">Value</span><span class="sxs-lookup"><span data-stu-id="aeeb4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aeeb4-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeeb4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aeeb4-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aeeb4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aeeb4-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeeb4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aeeb4-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="aeeb4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aeeb4-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aeeb4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aeeb4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeeb4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





