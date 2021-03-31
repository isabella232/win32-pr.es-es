---
title: Código de notificación de TTN_POP (commctrl. h)
description: Notifica a la ventana propietaria que la información sobre herramientas está a punto de ocultarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- TTN_POP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576aa382f571fb6ded7205d2df3b0abd938c704d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802234"
---
# <a name="ttn_pop-notification-code"></a><span data-ttu-id="f1966-105">Código de notificación de pop de TTN \_</span><span class="sxs-lookup"><span data-stu-id="f1966-105">TTN\_POP notification code</span></span>

<span data-ttu-id="f1966-106">Notifica a la ventana propietaria que la información sobre herramientas está a punto de ocultarse.</span><span class="sxs-lookup"><span data-stu-id="f1966-106">Notifies the owner window that a tooltip is about to be hidden.</span></span> <span data-ttu-id="f1966-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f1966-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f1966-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1966-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1966-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1966-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1966-110">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="f1966-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1966-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1966-111">Return value</span></span>

<span data-ttu-id="f1966-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f1966-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1966-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1966-113">Requirements</span></span>



| <span data-ttu-id="f1966-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1966-114">Requirement</span></span> | <span data-ttu-id="f1966-115">Value</span><span class="sxs-lookup"><span data-stu-id="f1966-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1966-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1966-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1966-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f1966-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1966-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1966-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1966-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1966-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1966-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1966-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1966-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1966-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





