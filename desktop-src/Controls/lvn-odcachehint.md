---
title: Código de notificación de LVN_ODCACHEHINT (commctrl. h)
description: Lo envía un control de vista de lista virtual cuando cambia el contenido de su área de presentación.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997182"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="7144d-104">Código de notificación de ODCACHEHINT de LVN \_</span><span class="sxs-lookup"><span data-stu-id="7144d-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="7144d-105">Lo envía un control de vista de lista virtual cuando cambia el contenido de su área de presentación.</span><span class="sxs-lookup"><span data-stu-id="7144d-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="7144d-106">Por ejemplo, un control de vista de lista envía este código de notificación cuando el usuario desplaza la pantalla del control.</span><span class="sxs-lookup"><span data-stu-id="7144d-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="7144d-107">El \_ código de notificación ODCACHEHINT de LVN se envía en forma de mensaje de notificación de [**WM \_**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7144d-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7144d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7144d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7144d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7144d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7144d-110">Puntero a una estructura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) que contiene información sobre el intervalo de elementos que se va a almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="7144d-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7144d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7144d-111">Return value</span></span>

<span data-ttu-id="7144d-112">La aplicación que recibe este código de notificación debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="7144d-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7144d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7144d-113">Remarks</span></span>

<span data-ttu-id="7144d-114">El control de este mensaje permite que la aplicación actualice la información del elemento que se mantiene en la memoria caché para que esté disponible fácilmente cuando se envíe un código de notificación [ \_ GETDISPINFO de LVN](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="7144d-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="7144d-115">Tenga en cuenta que este código de notificación no siempre es una representación exacta de los elementos que [LVN \_ GETDISPINFO](lvn-getdispinfo.md)solicitará.</span><span class="sxs-lookup"><span data-stu-id="7144d-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="7144d-116">Por lo tanto, si el elemento solicitado no se almacena en la memoria caché mientras se controla LVN \_ GETDISPINFO, la aplicación debe estar preparada para proporcionar la información solicitada de un origen fuera de la caché.</span><span class="sxs-lookup"><span data-stu-id="7144d-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="7144d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7144d-117">Requirements</span></span>



| <span data-ttu-id="7144d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7144d-118">Requirement</span></span> | <span data-ttu-id="7144d-119">Value</span><span class="sxs-lookup"><span data-stu-id="7144d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7144d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7144d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7144d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7144d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7144d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7144d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7144d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7144d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7144d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7144d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7144d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7144d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





