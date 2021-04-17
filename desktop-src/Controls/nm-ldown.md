---
title: Código de notificación de NM_LDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control que se ha presionado el botón primario del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 59546fc3-f7c5-4b2d-9fd7-2ff89d72cd9f
keywords:
- NM_LDOWN controles de código de notificación de Windows
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
ms.openlocfilehash: 3d62d1570fc0c10ccb64ae6c1f9af6433025ec79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656471"
---
# <a name="nm_ldown-notification-code"></a><span data-ttu-id="281c5-105">Código de notificación de NM \_ LDOWN</span><span class="sxs-lookup"><span data-stu-id="281c5-105">NM\_LDOWN notification code</span></span>

<span data-ttu-id="281c5-106">Notifica a la ventana primaria de un control que se ha presionado el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="281c5-106">Notifies a control's parent window that the left mouse button has been pressed.</span></span> <span data-ttu-id="281c5-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="281c5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_LDOWN

   lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="281c5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="281c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="281c5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="281c5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="281c5-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="281c5-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="281c5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="281c5-111">Return value</span></span>

<span data-ttu-id="281c5-112">El control omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="281c5-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="281c5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="281c5-113">Requirements</span></span>



| <span data-ttu-id="281c5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="281c5-114">Requirement</span></span> | <span data-ttu-id="281c5-115">Value</span><span class="sxs-lookup"><span data-stu-id="281c5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="281c5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="281c5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="281c5-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="281c5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="281c5-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="281c5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="281c5-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="281c5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="281c5-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="281c5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="281c5-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="281c5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





