---
title: Mensaje WM_POINTERROUTEDRELEASED
description: Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de AddContentWithCrossProcessChaining y no que actualmente controla la entrada de puntero) que se asocian a un identificador de puntero específico, cuando se recibe un mensaje de WM_POINTERUP en el proceso actual.
ms.assetid: B031ED80-6F1B-42A7-B4E2-55934E2C456C
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERROUTEDRELEASED
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDRELEASED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 8e24a0df1a2bbdf2b0a9df97057686aa6045eff8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422326"
---
# <a name="wm_pointerroutedreleased-message"></a><span data-ttu-id="d17d3-104">Mensaje WM_POINTERROUTEDRELEASED</span><span class="sxs-lookup"><span data-stu-id="d17d3-104">WM_POINTERROUTEDRELEASED message</span></span>

<span data-ttu-id="d17d3-105">Se envía a todos los procesos (configurados para el encadenamiento entre procesos a través de [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) y no que actualmente controla la entrada de puntero) que se asocian a un identificador de puntero específico, cuando se recibe un mensaje de [**WM_POINTERUP**](wm-pointerup.md) en el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="d17d3-105">Sent to all processes (configured for cross-process chaining through [**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining) and not currently handling pointer input) ever associated with a specific pointer ID, when a [**WM_POINTERUP**](wm-pointerup.md) message is received on the current process.</span></span>


```C++
#define WM_POINTERROUTEDRELEASED       0x0253
```



## <a name="parameters"></a><span data-ttu-id="d17d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d17d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d17d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d17d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d17d3-108">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="d17d3-108">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d17d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d17d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d17d3-110">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="d17d3-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d17d3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d17d3-111">Return value</span></span>

<span data-ttu-id="d17d3-112">NULL</span><span class="sxs-lookup"><span data-stu-id="d17d3-112">NULL</span></span>

## <a name="requirements"></a><span data-ttu-id="d17d3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d17d3-113">Requirements</span></span>



| <span data-ttu-id="d17d3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d17d3-114">Requirement</span></span> | <span data-ttu-id="d17d3-115">Value</span><span class="sxs-lookup"><span data-stu-id="d17d3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d17d3-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d17d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d17d3-117">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d17d3-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d17d3-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d17d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d17d3-119">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="d17d3-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d17d3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d17d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d17d3-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d17d3-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d17d3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d17d3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d17d3-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="d17d3-123">Messages</span></span>](messages.md)
</dt> </dl>

 

