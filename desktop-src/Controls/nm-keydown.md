---
title: Código de notificación de NM_KEYDOWN (commctrl. h)
description: Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222a47733a60590e7d56ca0adba038164c430fab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904993"
---
# <a name="nm_keydown-notification-code"></a><span data-ttu-id="8f635-105">\_Código de notificación KEYDOWN de nm</span><span class="sxs-lookup"><span data-stu-id="8f635-105">NM\_KEYDOWN notification code</span></span>

<span data-ttu-id="8f635-106">Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="8f635-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="8f635-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8f635-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8f635-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f635-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f635-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f635-110">Puntero a una estructura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contiene información adicional sobre la clave que produjo el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="8f635-110">A pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f635-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f635-111">Return value</span></span>

<span data-ttu-id="8f635-112">Devuelve un valor distinto de cero para evitar que el control procese la clave o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8f635-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f635-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f635-113">Requirements</span></span>



| <span data-ttu-id="8f635-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f635-114">Requirement</span></span> | <span data-ttu-id="8f635-115">Value</span><span class="sxs-lookup"><span data-stu-id="8f635-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f635-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f635-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8f635-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f635-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f635-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f635-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8f635-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f635-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f635-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f635-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f635-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f635-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





