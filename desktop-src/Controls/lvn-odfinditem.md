---
title: Mensaje de LVN_ODFINDITEM (commctrl. h)
description: Lo envía un control de vista de lista virtual cuando necesita que el propietario busque un elemento de devolución de llamada determinado.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- LVN_ODFINDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150663"
---
# <a name="lvn_odfinditem-message"></a><span data-ttu-id="3a57b-104">LVN \_ ODFINDITEM</span><span class="sxs-lookup"><span data-stu-id="3a57b-104">LVN\_ODFINDITEM message</span></span>

<span data-ttu-id="3a57b-105">Lo envía un control [de vista de lista virtual](list-view-controls-overview.md) cuando necesita que el propietario busque un elemento de devolución de llamada determinado.</span><span class="sxs-lookup"><span data-stu-id="3a57b-105">Sent by a [virtual list-view](list-view-controls-overview.md) control when it needs the owner to find a particular callback item.</span></span> <span data-ttu-id="3a57b-106">Por ejemplo, el control enviará este código de notificación cuando reciba entradas de teclado de acceso directo o cuando reciba un mensaje de [**LVM de LVM \_**](lvm-finditem.md) .</span><span class="sxs-lookup"><span data-stu-id="3a57b-106">For example, the control will send this notification code when it receives shortcut keyboard input or when it receives an [**LVM\_FINDITEM**](lvm-finditem.md) message.</span></span> <span data-ttu-id="3a57b-107">El \_ código de notificación ODFINDITEM de LVN se envía en forma de mensaje de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3a57b-107">The LVN\_ODFINDITEM notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3a57b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a57b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a57b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a57b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a57b-110">Puntero a una estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que incluye la información que se va a usar para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3a57b-110">Pointer to an [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that includes information to be used for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a57b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a57b-111">Return value</span></span>

<span data-ttu-id="3a57b-112">Devuelve el índice del elemento encontrado o-1 si no se encuentra ningún elemento.</span><span class="sxs-lookup"><span data-stu-id="3a57b-112">Return the index of the item found, or -1 if no item is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a57b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a57b-113">Remarks</span></span>

<span data-ttu-id="3a57b-114">La información de búsqueda se envía en forma de una estructura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , que es un miembro de la estructura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="3a57b-114">Search information is sent in the form of an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure, which is a member of the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a57b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a57b-115">Requirements</span></span>



| <span data-ttu-id="3a57b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a57b-116">Requirement</span></span> | <span data-ttu-id="3a57b-117">Value</span><span class="sxs-lookup"><span data-stu-id="3a57b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a57b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a57b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a57b-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a57b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a57b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a57b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a57b-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a57b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a57b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a57b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a57b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a57b-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="3a57b-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="3a57b-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3a57b-125">**LVN \_ ODFINDITEMW** (Unicode) y **LVN \_ ODFINDITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3a57b-125">**LVN\_ODFINDITEMW** (Unicode) and **LVN\_ODFINDITEMA** (ANSI)</span></span><br/>             |



 

 





