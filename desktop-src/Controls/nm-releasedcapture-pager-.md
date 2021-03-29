---
title: Código de notificación de NM_RELEASEDCAPTURE (buscapersonas) (commctrl. h)
description: Notifica a la ventana primaria de un control de paginación que el control ha liberado la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- Controles de Windows de código de notificación de NM_RELEASEDCAPTURE (buscapersonas)
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905309"
---
# <a name="nm_releasedcapture-pager-notification-code"></a><span data-ttu-id="948ba-105">Código de notificación de NM \_ RELEASEDCAPTURE (buscapersonas)</span><span class="sxs-lookup"><span data-stu-id="948ba-105">NM\_RELEASEDCAPTURE (pager) notification code</span></span>

<span data-ttu-id="948ba-106">Notifica a la ventana primaria de un control de paginación que el control ha liberado la captura del mouse.</span><span class="sxs-lookup"><span data-stu-id="948ba-106">Notifies a pager control's parent window that the control has released the mouse capture.</span></span> <span data-ttu-id="948ba-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="948ba-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="948ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="948ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="948ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="948ba-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="948ba-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948ba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="948ba-111">Return value</span></span>

<span data-ttu-id="948ba-112">El control de paginación omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="948ba-112">The return value is ignored by the pager control.</span></span>

## <a name="requirements"></a><span data-ttu-id="948ba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948ba-113">Requirements</span></span>



| <span data-ttu-id="948ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="948ba-114">Requirement</span></span> | <span data-ttu-id="948ba-115">Value</span><span class="sxs-lookup"><span data-stu-id="948ba-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="948ba-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="948ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="948ba-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="948ba-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="948ba-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="948ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="948ba-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="948ba-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="948ba-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="948ba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="948ba-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="948ba-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





