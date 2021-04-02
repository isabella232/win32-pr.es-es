---
title: Código de notificación de NM_CLICK (vista de lista) (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario hace clic en un elemento con el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d766767bfb742e5d7ea7c22a1266540a40d65b9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151275"
---
# <a name="nm_click-list-view-notification-code"></a><span data-ttu-id="7b5bc-105">NM \_ haga clic en el código de notificación (vista de lista)</span><span class="sxs-lookup"><span data-stu-id="7b5bc-105">NM\_CLICK (list view) notification code</span></span>

<span data-ttu-id="7b5bc-106">Lo envía un control de vista de lista cuando el usuario hace clic en un elemento con el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-106">Sent by a list-view control when the user clicks an item with the left mouse button.</span></span> <span data-ttu-id="7b5bc-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5bc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7b5bc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b5bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b5bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b5bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7b5bc-110">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7b5bc-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="7b5bc-111">Puntero a una estructura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-111">Pointer to an [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) structure that contains additional information about this notification.</span></span> <span data-ttu-id="7b5bc-112">Los miembros **iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-112">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b5bc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b5bc-113">Return value</span></span>

<span data-ttu-id="7b5bc-114">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5bc-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b5bc-115">Remarks</span></span>

<span data-ttu-id="7b5bc-116">El miembro **iItem** de *lParam* solo es válido si se hace clic en el icono o la etiqueta de la primera columna.</span><span class="sxs-lookup"><span data-stu-id="7b5bc-116">The **iItem** member of *lParam* is only valid if the icon or first-column label has been clicked.</span></span> <span data-ttu-id="7b5bc-117">Para determinar qué elemento se selecciona cuando tiene lugar un clic en otro lugar de una fila, envíe un mensaje de [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5bc-117">To determine which item is selected when a click takes place elsewhere in a row, send an [**LVM\_SUBITEMHITTEST**](lvm-subitemhittest.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5bc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b5bc-118">Requirements</span></span>



| <span data-ttu-id="7b5bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b5bc-119">Requirement</span></span> | <span data-ttu-id="7b5bc-120">Value</span><span class="sxs-lookup"><span data-stu-id="7b5bc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5bc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b5bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b5bc-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7b5bc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b5bc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b5bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b5bc-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b5bc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b5bc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b5bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b5bc-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b5bc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





