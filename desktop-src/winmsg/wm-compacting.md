---
description: Se envía a todas las ventanas de nivel superior cuando el sistema detecta más del 12,5 por ciento de la hora del sistema durante un intervalo de 30 a 60 segundos en la compactación de la memoria. Esto indica que la memoria del sistema es baja.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Mensaje de WM_COMPACTING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706673"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="90915-104">\_Mensaje de compactación de WM</span><span class="sxs-lookup"><span data-stu-id="90915-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="90915-105">Se envía a todas las ventanas de nivel superior cuando el sistema detecta más del 12,5 por ciento de la hora del sistema durante un intervalo de 30 a 60 segundos en la compactación de la memoria.</span><span class="sxs-lookup"><span data-stu-id="90915-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="90915-106">Esto indica que la memoria del sistema es baja.</span><span class="sxs-lookup"><span data-stu-id="90915-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="90915-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="90915-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="90915-108">Este mensaje se proporciona solo para ofrecer compatibilidad con aplicaciones basadas en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="90915-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="90915-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90915-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90915-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90915-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90915-111">La proporción de tiempo de la unidad central de procesamiento (CPU) empleada actualmente por el sistema que compacta la memoria en el tiempo de CPU empleado actualmente por el sistema que realiza otras operaciones.</span><span class="sxs-lookup"><span data-stu-id="90915-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="90915-112">Por ejemplo, 0x8000 representa el 50 por ciento del tiempo de CPU empleado en compactar la memoria.</span><span class="sxs-lookup"><span data-stu-id="90915-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="90915-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90915-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90915-114">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="90915-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90915-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90915-115">Return value</span></span>

<span data-ttu-id="90915-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="90915-116">Type: **LRESULT**</span></span>

<span data-ttu-id="90915-117">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="90915-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="90915-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90915-118">Remarks</span></span>

<span data-ttu-id="90915-119">Cuando una aplicación recibe este mensaje, debe liberar toda la memoria posible, teniendo en cuenta el nivel actual de actividad de la aplicación y el número total de aplicaciones que se ejecutan en el sistema.</span><span class="sxs-lookup"><span data-stu-id="90915-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="90915-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90915-120">Requirements</span></span>



| <span data-ttu-id="90915-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="90915-121">Requirement</span></span> | <span data-ttu-id="90915-122">Value</span><span class="sxs-lookup"><span data-stu-id="90915-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90915-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90915-123">Minimum supported client</span></span><br/> | <span data-ttu-id="90915-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90915-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="90915-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90915-125">Minimum supported server</span></span><br/> | <span data-ttu-id="90915-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90915-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90915-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90915-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="90915-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90915-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90915-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="90915-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90915-130">Información general de Windows</span><span class="sxs-lookup"><span data-stu-id="90915-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
