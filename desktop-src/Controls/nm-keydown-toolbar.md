---
title: Código de notificación de NM_KEYDOWN (barra de herramientas) (commctrl. h)
description: Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: bdfcf9da-118b-4fe6-9a0a-6329eb9196ef
keywords:
- Código de notificación de NM_KEYDOWN (barra de herramientas) controles de Windows
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
ms.openlocfilehash: e7326946a8234122c81b2fd057dab0ad313d49a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078858"
---
# <a name="nm_keydown-toolbar-notification-code"></a><span data-ttu-id="2eefc-105">NM \_ código de notificación de KEYDOWN (Toolbar)</span><span class="sxs-lookup"><span data-stu-id="2eefc-105">NM\_KEYDOWN (toolbar) notification code</span></span>

<span data-ttu-id="2eefc-106">Se envía por un control cuando el control tiene el foco de teclado y el usuario presiona una tecla.</span><span class="sxs-lookup"><span data-stu-id="2eefc-106">Sent by a control when the control has the keyboard focus and the user presses a key.</span></span> <span data-ttu-id="2eefc-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2eefc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2eefc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2eefc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eefc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2eefc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2eefc-110">Puntero a una estructura [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contiene información adicional sobre la clave que produjo el código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2eefc-110">Pointer to an [**NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) structure that contains additional information about the key that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eefc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2eefc-111">Return value</span></span>

<span data-ttu-id="2eefc-112">Devuelve un valor distinto de cero para evitar que el control procese la clave o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="2eefc-112">Return nonzero to prevent the control from processing the key, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2eefc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2eefc-113">Remarks</span></span>

<span data-ttu-id="2eefc-114">Actualmente, solo el control de barra de herramientas envía este código de notificación.</span><span class="sxs-lookup"><span data-stu-id="2eefc-114">Currently, only the toolbar control sends this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eefc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eefc-115">Requirements</span></span>



| <span data-ttu-id="2eefc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eefc-116">Requirement</span></span> | <span data-ttu-id="2eefc-117">Value</span><span class="sxs-lookup"><span data-stu-id="2eefc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2eefc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eefc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2eefc-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2eefc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2eefc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2eefc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2eefc-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2eefc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eefc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2eefc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eefc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eefc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





