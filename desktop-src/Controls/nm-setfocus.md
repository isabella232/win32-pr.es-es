---
title: Código de notificación de NM_SETFOCUS (commctrl. h)
description: Notifica a la ventana primaria de un control que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 4810afd3-c8a8-4813-b44a-eba3d409d4f1
keywords:
- NM_SETFOCUS controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd3d50596f39359fe2aeeeb4fe61b8bc73603efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996743"
---
# <a name="nm_setfocus-notification-code"></a><span data-ttu-id="c9b1e-105">Código de notificación de SETFOCUS de NM \_</span><span class="sxs-lookup"><span data-stu-id="c9b1e-105">NM\_SETFOCUS notification code</span></span>

<span data-ttu-id="c9b1e-106">Notifica a la ventana primaria de un control que el control ha recibido el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="c9b1e-106">Notifies a control's parent window that the control has received the input focus.</span></span> <span data-ttu-id="c9b1e-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c9b1e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c9b1e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9b1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9b1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9b1e-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="c9b1e-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b1e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9b1e-111">Return value</span></span>

<span data-ttu-id="c9b1e-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="c9b1e-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b1e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9b1e-113">Requirements</span></span>



| <span data-ttu-id="c9b1e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b1e-114">Requirement</span></span> | <span data-ttu-id="c9b1e-115">Value</span><span class="sxs-lookup"><span data-stu-id="c9b1e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b1e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9b1e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b1e-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c9b1e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9b1e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9b1e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b1e-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9b1e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9b1e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9b1e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b1e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b1e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





