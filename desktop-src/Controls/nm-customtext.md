---
title: Código de notificación de NM_CUSTOMTEXT (commctrl. h)
description: Notifica a la ventana primaria de un control sobre las operaciones de texto personalizado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eebc4033a76d137e28a0c4170c5c613c7933562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421915"
---
# <a name="nm_customtext-notification-code"></a><span data-ttu-id="3824a-105">Código de notificación de NM \_ CUSTOMTEXT</span><span class="sxs-lookup"><span data-stu-id="3824a-105">NM\_CUSTOMTEXT notification code</span></span>

<span data-ttu-id="3824a-106">Notifica a la ventana primaria de un control sobre las operaciones de texto personalizado.</span><span class="sxs-lookup"><span data-stu-id="3824a-106">Notifies a control's parent window about custom text operations.</span></span> <span data-ttu-id="3824a-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3824a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3824a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3824a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3824a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3824a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3824a-110">Puntero a una estructura [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="3824a-110">A pointer to an [**NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3824a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3824a-111">Return value</span></span>

<span data-ttu-id="3824a-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3824a-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3824a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3824a-113">Requirements</span></span>



| <span data-ttu-id="3824a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3824a-114">Requirement</span></span> | <span data-ttu-id="3824a-115">Value</span><span class="sxs-lookup"><span data-stu-id="3824a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3824a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3824a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3824a-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3824a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3824a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3824a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3824a-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3824a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3824a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3824a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3824a-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3824a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





