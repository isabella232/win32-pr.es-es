---
title: Código de notificación de LVN_ITEMCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que un elemento está cambiando. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997184"
---
# <a name="lvn_itemchanging-notification-code"></a><span data-ttu-id="170c7-105">Código de notificación de ITEMCHANGING de LVN \_</span><span class="sxs-lookup"><span data-stu-id="170c7-105">LVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="170c7-106">Notifica a la ventana primaria de un control de vista de lista que un elemento está cambiando.</span><span class="sxs-lookup"><span data-stu-id="170c7-106">Notifies a list-view control's parent window that an item is changing.</span></span> <span data-ttu-id="170c7-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="170c7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="170c7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="170c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="170c7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="170c7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="170c7-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica el elemento y especifica cuál de sus atributos está cambiando.</span><span class="sxs-lookup"><span data-stu-id="170c7-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure that identifies the item and specifies which of its attributes are changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="170c7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="170c7-111">Return value</span></span>

<span data-ttu-id="170c7-112">Devuelve **true** para evitar el cambio o **false** para permitir el cambio.</span><span class="sxs-lookup"><span data-stu-id="170c7-112">Returns **TRUE** to prevent the change, or **FALSE** to allow the change.</span></span>

## <a name="remarks"></a><span data-ttu-id="170c7-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="170c7-113">Remarks</span></span>

<span data-ttu-id="170c7-114">Si el control de vista de lista tiene el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , \_ no se envían los códigos de notificación de LVN ITEMCHANGING.</span><span class="sxs-lookup"><span data-stu-id="170c7-114">If the list-view control has the [**LVS\_OWNERDATA**](list-view-window-styles.md) style, LVN\_ITEMCHANGING notification codes are not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="170c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="170c7-115">Requirements</span></span>



| <span data-ttu-id="170c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="170c7-116">Requirement</span></span> | <span data-ttu-id="170c7-117">Value</span><span class="sxs-lookup"><span data-stu-id="170c7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="170c7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="170c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="170c7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="170c7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="170c7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="170c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="170c7-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="170c7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="170c7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="170c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="170c7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="170c7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





