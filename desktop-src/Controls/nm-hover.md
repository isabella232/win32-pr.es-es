---
title: Código de notificación de NM_HOVER (commctrl. h)
description: Se envía por un control cuando se mantiene el mouse sobre un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0eef3e88-c1f0-4f9c-9ccf-580d8e464157
keywords:
- NM_HOVER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69344b1aae78ebee99b86c78f4442df20f66187a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801094"
---
# <a name="nm_hover-notification-code"></a><span data-ttu-id="d5ec8-105">Código de notificación de desplazamiento de NM \_</span><span class="sxs-lookup"><span data-stu-id="d5ec8-105">NM\_HOVER notification code</span></span>

<span data-ttu-id="d5ec8-106">Se envía por un control cuando se mantiene el mouse sobre un elemento.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-106">Sent by a control when the mouse hovers over an item.</span></span> <span data-ttu-id="d5ec8-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ec8-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d5ec8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5ec8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ec8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5ec8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5ec8-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ec8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5ec8-111">Return value</span></span>

<span data-ttu-id="d5ec8-112">A menos que se especifique lo contrario, devuelva cero para permitir que el control procese el desplazamiento normal, o un valor distinto de cero para evitar que se procese el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="d5ec8-112">Unless otherwise specified, return zero to allow the control to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ec8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5ec8-113">Requirements</span></span>



| <span data-ttu-id="d5ec8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ec8-114">Requirement</span></span> | <span data-ttu-id="d5ec8-115">Value</span><span class="sxs-lookup"><span data-stu-id="d5ec8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ec8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5ec8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ec8-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d5ec8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5ec8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5ec8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ec8-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5ec8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5ec8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5ec8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5ec8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ec8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





