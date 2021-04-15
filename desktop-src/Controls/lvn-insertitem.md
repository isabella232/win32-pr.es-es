---
title: Código de notificación de LVN_INSERTITEM (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de lista que se ha insertado un nuevo elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- LVN_INSERTITEM controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493330"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="1ee70-105">LVN \_ código de notificación INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="1ee70-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="1ee70-106">Notifica a la ventana primaria de un control de vista de lista que se ha insertado un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="1ee70-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="1ee70-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee70-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1ee70-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ee70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ee70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee70-110">Puntero a una estructura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="1ee70-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="1ee70-111">El miembro **iItem** identifica el nuevo elemento y los demás miembros son cero.</span><span class="sxs-lookup"><span data-stu-id="1ee70-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee70-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ee70-112">Return value</span></span>

<span data-ttu-id="1ee70-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1ee70-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee70-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee70-114">Requirements</span></span>



| <span data-ttu-id="1ee70-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee70-115">Requirement</span></span> | <span data-ttu-id="1ee70-116">Value</span><span class="sxs-lookup"><span data-stu-id="1ee70-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee70-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ee70-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee70-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1ee70-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ee70-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ee70-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee70-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ee70-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ee70-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ee70-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee70-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ee70-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





