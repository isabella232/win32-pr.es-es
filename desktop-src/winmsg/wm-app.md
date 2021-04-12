---
description: Se usa para definir mensajes privados, normalmente con el formato WM \_ App + x, donde x es un valor entero.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277769"
---
# <a name="wm_app"></a><span data-ttu-id="d418a-103">aplicación de WM \_</span><span class="sxs-lookup"><span data-stu-id="d418a-103">WM\_APP</span></span>

<span data-ttu-id="d418a-104">Se usa para definir mensajes privados, normalmente con el formato **WM \_ App** + *x*, donde *x* es un valor entero.</span><span class="sxs-lookup"><span data-stu-id="d418a-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="d418a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d418a-105">Remarks</span></span>

<span data-ttu-id="d418a-106">La constante de **\_ aplicación de WM** se usa para distinguir entre los valores de mensaje que se reservan para su uso por el sistema y los valores que una aplicación puede usar para enviar mensajes dentro de una clase de ventana privada.</span><span class="sxs-lookup"><span data-stu-id="d418a-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="d418a-107">A continuación se indican los intervalos de números de mensajes disponibles.</span><span class="sxs-lookup"><span data-stu-id="d418a-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="d418a-108">Intervalo</span><span class="sxs-lookup"><span data-stu-id="d418a-108">Range</span></span>                                                 | <span data-ttu-id="d418a-109">Significado</span><span class="sxs-lookup"><span data-stu-id="d418a-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d418a-110">de 0 a [**WM \_ usuario**](wm-user.md) – 1</span><span class="sxs-lookup"><span data-stu-id="d418a-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="d418a-111">Mensajes reservados para su uso por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d418a-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="d418a-112">[**WM \_ USUARIO**](wm-user.md) a través de 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="d418a-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="d418a-113">Mensajes enteros para su uso por las clases de ventana privadas.</span><span class="sxs-lookup"><span data-stu-id="d418a-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="d418a-114">**WM \_ APLICACIÓN** a través de 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="d418a-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="d418a-115">Mensajes disponibles para que las usen las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d418a-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="d418a-116">0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="d418a-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="d418a-117">Mensajes de cadena para su uso por parte de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d418a-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="d418a-118">Mayor que 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="d418a-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="d418a-119">Reservado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d418a-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="d418a-120">El sistema define los números de mensaje en el primer intervalo (del 0 al [**\_ usuario de WM**](wm-user.md) -1).</span><span class="sxs-lookup"><span data-stu-id="d418a-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="d418a-121">El sistema reserva los valores de este intervalo que no se definen explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d418a-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="d418a-122">Los números de mensajes del segundo intervalo [**( \_ usuario de WM**](wm-user.md) a través de 0x7FFF) se pueden definir y usar en una aplicación para enviar mensajes dentro de una clase de ventana privada.</span><span class="sxs-lookup"><span data-stu-id="d418a-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="d418a-123">Estos valores no se pueden usar para definir mensajes que sean significativos en una aplicación porque algunas clases de ventana predefinidas ya definen valores en este intervalo.</span><span class="sxs-lookup"><span data-stu-id="d418a-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="d418a-124">Por ejemplo, las clases de control predefinidas como **Button**, **Edit**, **ListBox** y **ComboBox** pueden utilizar estos valores.</span><span class="sxs-lookup"><span data-stu-id="d418a-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="d418a-125">Los mensajes de este intervalo no se deben enviar a otras aplicaciones a menos que las aplicaciones se hayan diseñado para intercambiar mensajes y adjuntar el mismo significado a los números de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d418a-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="d418a-126">Los números de mensaje en el tercer intervalo (de 0x8000 a 0xBFFF) están disponibles para que las aplicaciones lo usen como mensajes privados.</span><span class="sxs-lookup"><span data-stu-id="d418a-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="d418a-127">Los mensajes de este intervalo no entran en conflicto con los mensajes del sistema.</span><span class="sxs-lookup"><span data-stu-id="d418a-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="d418a-128">Los números de mensaje del cuarto intervalo (de 0xC000 a 0xFFFF) se definen en tiempo de ejecución cuando una aplicación llama a la función [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar un número de mensaje para una cadena.</span><span class="sxs-lookup"><span data-stu-id="d418a-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="d418a-129">Todas las aplicaciones que registran la misma cadena pueden usar el número de mensaje asociado para intercambiar mensajes.</span><span class="sxs-lookup"><span data-stu-id="d418a-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="d418a-130">Sin embargo, el número de mensaje real no es una constante y no se puede suponer que sea el mismo entre distintas sesiones.</span><span class="sxs-lookup"><span data-stu-id="d418a-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="d418a-131">El sistema reserva los números de mensaje del quinto intervalo (mayor que 0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="d418a-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="d418a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d418a-132">Requirements</span></span>



| <span data-ttu-id="d418a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d418a-133">Requirement</span></span> | <span data-ttu-id="d418a-134">Value</span><span class="sxs-lookup"><span data-stu-id="d418a-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d418a-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d418a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d418a-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d418a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d418a-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d418a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d418a-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d418a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d418a-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d418a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d418a-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d418a-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d418a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="d418a-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="d418a-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d418a-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d418a-143">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="d418a-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="d418a-144">**usuario de WM \_**</span><span class="sxs-lookup"><span data-stu-id="d418a-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="d418a-145">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d418a-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d418a-146">Mensajes y colas de mensajes</span><span class="sxs-lookup"><span data-stu-id="d418a-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
