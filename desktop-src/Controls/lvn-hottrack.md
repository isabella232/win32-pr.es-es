---
title: Código de notificación de LVN_HOTTRACK (commctrl. h)
description: Lo envía un control de vista de lista cuando el usuario mueve el mouse sobre un elemento. Este código de notificación solo lo envían los controles de vista de lista que tienen \_ el \_ estilo de vista de lista extendido LVS ex TRACKSELECT. Se envía en forma de un mensaje de notificación de WM \_ .
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c677b69fa21cdbe3680442304f6745cfb3a907de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905695"
---
# <a name="lvn_hottrack-notification-code"></a><span data-ttu-id="5e3d4-106">Código de notificación de HOTTRACK de LVN \_</span><span class="sxs-lookup"><span data-stu-id="5e3d4-106">LVN\_HOTTRACK notification code</span></span>

<span data-ttu-id="5e3d4-107">Lo envía un control de vista de lista cuando el usuario mueve el mouse sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-107">Sent by a list-view control when the user moves the mouse over an item.</span></span> <span data-ttu-id="5e3d4-108">Este código de notificación solo lo envían los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3d4-108">This notification code is only sent by list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) extended list-view style.</span></span> <span data-ttu-id="5e3d4-109">Se envía en forma de un mensaje de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3d4-109">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5e3d4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e3d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e3d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e3d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e3d4-112">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que contiene información sobre este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-112">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that contains information about this notification code.</span></span> <span data-ttu-id="5e3d4-113">Los miembros **iItem**, **iSubItem** y **ptAction** de esta estructura contienen información sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-113">The **iItem**, **iSubItem**, and **ptAction** members of this structure contain information about the item.</span></span> <span data-ttu-id="5e3d4-114">La aplicación receptora puede modificar el miembro **iItem** para especificar el elemento que se seleccionará.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-114">The receiving application can modify the **iItem** member to specify the item that will be selected.</span></span> <span data-ttu-id="5e3d4-115">Si **iItem** se establece en-1, no se seleccionará ningún elemento.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-115">If **iItem** is set to -1, no item will be selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e3d4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e3d4-116">Return value</span></span>

<span data-ttu-id="5e3d4-117">Devuelve cero para permitir que la vista de lista realice su procesamiento de selección de pista normal.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-117">Return zero to allow the list view to perform its normal track select processing.</span></span> <span data-ttu-id="5e3d4-118">Si la aplicación devuelve un valor distinto de cero, el elemento no se seleccionará.</span><span class="sxs-lookup"><span data-stu-id="5e3d4-118">If the application returns nonzero, the item will not be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3d4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e3d4-119">Requirements</span></span>



| <span data-ttu-id="5e3d4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3d4-120">Requirement</span></span> | <span data-ttu-id="5e3d4-121">Value</span><span class="sxs-lookup"><span data-stu-id="5e3d4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3d4-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3d4-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e3d4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e3d4-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e3d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3d4-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e3d4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e3d4-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e3d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e3d4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3d4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





