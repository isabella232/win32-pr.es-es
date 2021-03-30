---
description: Notifica a una Appbar cuando se ha producido un evento que puede afectar al tamaño y la posición de la Appbar.
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: Mensaje de ABN_POSCHANGED (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984374"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="12d63-103">Mensaje de ABN \_ POSCHANGED</span><span class="sxs-lookup"><span data-stu-id="12d63-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="12d63-104">Notifica a una Appbar cuando se ha producido un evento que puede afectar al tamaño y la posición de la Appbar.</span><span class="sxs-lookup"><span data-stu-id="12d63-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="12d63-105">Los eventos incluyen cambios en el tamaño, la posición y el estado de visibilidad de la barra de tareas, así como la adición, eliminación o cambio de tamaño de otro Appbar en el mismo lado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="12d63-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="12d63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12d63-106">Parameters</span></span>

<span data-ttu-id="12d63-107">Este mensaje no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="12d63-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12d63-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12d63-108">Return value</span></span>

<span data-ttu-id="12d63-109">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="12d63-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d63-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12d63-110">Remarks</span></span>

<span data-ttu-id="12d63-111">Un Appbar debe responder a este mensaje de notificación mediante el envío de los mensajes [**ABN \_ QUERYPOS**](abm-querypos.md) y [**ABN \_ SETPOS**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="12d63-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="12d63-112">Si su posición ha cambiado, el Appbar debe llamar a la función [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) para moverse a la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="12d63-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12d63-113">Requirements</span></span>



| <span data-ttu-id="12d63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d63-114">Requirement</span></span> | <span data-ttu-id="12d63-115">Value</span><span class="sxs-lookup"><span data-stu-id="12d63-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12d63-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12d63-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12d63-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="12d63-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12d63-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12d63-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12d63-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12d63-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12d63-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12d63-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d63-121"><dt>ShellAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="12d63-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

