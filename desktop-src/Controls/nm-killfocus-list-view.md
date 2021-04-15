---
title: Código de notificación de NM_KILLFOCUS (vista de lista) (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que el control ha perdido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: f60064da-21e1-4555-ae72-cda8bd76175a
keywords:
- NM_KILLFOCUS (vista de lista) controles de Windows de código de notificación
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c031f3ab23d9f79ccf7f29dcfdf5472162214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489040"
---
# <a name="nm_killfocus-list-view-notification-code"></a><span data-ttu-id="22f1f-105">NM \_ KILLFOCUS (vista de lista) código de notificación</span><span class="sxs-lookup"><span data-stu-id="22f1f-105">NM\_KILLFOCUS (list view) notification code</span></span>

<span data-ttu-id="22f1f-106">Notifica a la ventana primaria de un control de vista de lista que el control ha perdido el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="22f1f-106">Notifies a list-view control's parent window that the control has lost the input focus.</span></span> <span data-ttu-id="22f1f-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="22f1f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="22f1f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22f1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22f1f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22f1f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22f1f-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="22f1f-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22f1f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22f1f-111">Return value</span></span>

<span data-ttu-id="22f1f-112">No se utiliza el valor devuelto para esta notificación.</span><span class="sxs-lookup"><span data-stu-id="22f1f-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="22f1f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22f1f-113">Requirements</span></span>



| <span data-ttu-id="22f1f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="22f1f-114">Requirement</span></span> | <span data-ttu-id="22f1f-115">Value</span><span class="sxs-lookup"><span data-stu-id="22f1f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22f1f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22f1f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22f1f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="22f1f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="22f1f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22f1f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22f1f-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="22f1f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="22f1f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22f1f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22f1f-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="22f1f-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





