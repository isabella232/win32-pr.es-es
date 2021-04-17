---
title: Mensaje WM_POINTERROUTEDTO
description: Se envía cuando la entrada de puntero continua, para un identificador de puntero existente, realiza la transición de un proceso a otro en el contenido configurado para el encadenamiento entre procesos (AddContentWithCrossProcessChaining).
ms.assetid: 163E2C31-4E29-4CBA-B079-1963D4762D7B
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERROUTEDTO
topic_type:
- apiref
api_name:
- WM_POINTERROUTEDTO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 7658aeef77a0f7e19f2449213e9332b4e60c9450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422189"
---
# <a name="wm_pointerroutedto-message"></a><span data-ttu-id="10fe0-104">Mensaje WM_POINTERROUTEDTO</span><span class="sxs-lookup"><span data-stu-id="10fe0-104">WM_POINTERROUTEDTO message</span></span>

<span data-ttu-id="10fe0-105">Se envía cuando la entrada de puntero continua, para un identificador de puntero existente, realiza la transición de un proceso a otro en el contenido configurado para el encadenamiento entre procesos ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span><span class="sxs-lookup"><span data-stu-id="10fe0-105">Sent when ongoing pointer input, for an existing pointer ID, transitions from one process to another across content configured for cross-process chaining ([**AddContentWithCrossProcessChaining**](/windows/win32/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining)).</span></span>

<span data-ttu-id="10fe0-106">Este mensaje se envía al proceso que no recibe actualmente la entrada de puntero.</span><span class="sxs-lookup"><span data-stu-id="10fe0-106">This message is sent to the process not currently receiving pointer input.</span></span>


```C++
#define WM_POINTERROUTEDTO       0x0251
```



## <a name="parameters"></a><span data-ttu-id="10fe0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10fe0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10fe0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10fe0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10fe0-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="10fe0-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="10fe0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10fe0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10fe0-111">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="10fe0-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10fe0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10fe0-112">Return value</span></span>

<span data-ttu-id="10fe0-113">NULL</span><span class="sxs-lookup"><span data-stu-id="10fe0-113">NULL</span></span>

## <a name="remarks"></a><span data-ttu-id="10fe0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10fe0-114">Remarks</span></span>

<span data-ttu-id="10fe0-115">Este mensaje no se envía cuando se envía un mensaje de [**WM_POINTERDOWN**](wm-pointerdown.md) para un nuevo identificador de puntero en un proceso diferente.</span><span class="sxs-lookup"><span data-stu-id="10fe0-115">This message is not sent when a [**WM_POINTERDOWN**](wm-pointerdown.md) message is posted for a new pointer ID on a different process.</span></span>

<span data-ttu-id="10fe0-116">No se envía un mensaje de [**WM_POINTERDOWN**](wm-pointerdown.md) si se publica primero un mensaje **WM_POINTERROUTEDTO** .</span><span class="sxs-lookup"><span data-stu-id="10fe0-116">A [**WM_POINTERDOWN**](wm-pointerdown.md) message is not sent if a **WM_POINTERROUTEDTO** message is posted first.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fe0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10fe0-117">Requirements</span></span>



| <span data-ttu-id="10fe0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10fe0-118">Requirement</span></span> | <span data-ttu-id="10fe0-119">Value</span><span class="sxs-lookup"><span data-stu-id="10fe0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10fe0-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10fe0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10fe0-121">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="10fe0-121">Windows 10 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="10fe0-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10fe0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10fe0-123">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="10fe0-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10fe0-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="10fe0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="10fe0-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10fe0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fe0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="10fe0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fe0-127">Mensajes</span><span class="sxs-lookup"><span data-stu-id="10fe0-127">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="10fe0-128">**WM_POINTERROUTEDAWAY**</span><span class="sxs-lookup"><span data-stu-id="10fe0-128">**WM_POINTERROUTEDAWAY**</span></span>](wm-pointerroutedaway.md)
</dt> </dl>

 

