---
title: Código de notificación de TRBN_THUMBPOSCHANGING (commctrl. h)
description: Notifica que la posición del control en una barra de desplazamiento está cambiando. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003619"
---
# <a name="trbn_thumbposchanging-notification-code"></a><span data-ttu-id="e26ce-105">Código de notificación de THUMBPOSCHANGING de TRBN \_</span><span class="sxs-lookup"><span data-stu-id="e26ce-105">TRBN\_THUMBPOSCHANGING notification code</span></span>

<span data-ttu-id="e26ce-106">Notifica que la posición del control en una barra de desplazamiento está cambiando.</span><span class="sxs-lookup"><span data-stu-id="e26ce-106">Notifies that the thumb position on a trackbar is changing.</span></span> <span data-ttu-id="e26ce-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e26ce-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e26ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e26ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e26ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e26ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e26ce-110">Puntero a una estructura [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) .</span><span class="sxs-lookup"><span data-stu-id="e26ce-110">Pointer to a [**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) structure.</span></span> <span data-ttu-id="e26ce-111">El autor de la llamada es responsable de asignar esta estructura y establecer sus miembros, incluidos los miembros de la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida.</span><span class="sxs-lookup"><span data-stu-id="e26ce-111">The caller is responsible for allocating this structure and setting its members, including the members of the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e26ce-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e26ce-112">Return value</span></span>

<span data-ttu-id="e26ce-113">Devuelve **true** para evitar que el control se mueva a la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="e26ce-113">Return **TRUE** to prevent the thumb from moving to the specified position.</span></span>

## <a name="remarks"></a><span data-ttu-id="e26ce-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e26ce-114">Remarks</span></span>

<span data-ttu-id="e26ce-115">Envíe esta notificación a los clientes que no escuchen los mensajes de [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="e26ce-115">Send this notification to clients that do not listen for [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e26ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e26ce-116">Requirements</span></span>



| <span data-ttu-id="e26ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e26ce-117">Requirement</span></span> | <span data-ttu-id="e26ce-118">Value</span><span class="sxs-lookup"><span data-stu-id="e26ce-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e26ce-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e26ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e26ce-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e26ce-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e26ce-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e26ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e26ce-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e26ce-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e26ce-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e26ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e26ce-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e26ce-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





