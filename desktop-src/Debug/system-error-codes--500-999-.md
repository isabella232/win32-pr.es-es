---
description: Describe los códigos de error 500-999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Códigos de error del sistema (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275031"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="f32a5-103">Códigos de error del sistema (500-999)</span><span class="sxs-lookup"><span data-stu-id="f32a5-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="f32a5-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="f32a5-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f32a5-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="f32a5-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 500 a 999).</span><span class="sxs-lookup"><span data-stu-id="f32a5-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="f32a5-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="f32a5-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="f32a5-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="f32a5-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="f32a5-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR \_ al \_ cargar el perfil de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-110">500 (0x1F4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-111">No se puede cargar el perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="f32a5-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**\_desbordamiento aritmético de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-113">534 (0x216)</span><span class="sxs-lookup"><span data-stu-id="f32a5-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-114">El resultado aritmético superó 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f32a5-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**\_canalización de errores \_ conectada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-116">535 (0x217)</span><span class="sxs-lookup"><span data-stu-id="f32a5-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-117">Hay un proceso en otro extremo de la canalización.</span><span class="sxs-lookup"><span data-stu-id="f32a5-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**canalización de errores en \_ \_ escucha**</span><span class="sxs-lookup"><span data-stu-id="f32a5-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-119">536 (0x218)</span><span class="sxs-lookup"><span data-stu-id="f32a5-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-120">Esperando a que un proceso Abra el otro extremo de la canalización.</span><span class="sxs-lookup"><span data-stu-id="f32a5-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**\_detención del comprobador de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-122">537 (0x219)</span><span class="sxs-lookup"><span data-stu-id="f32a5-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-123">El comprobador de aplicaciones ha encontrado un error en el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**error \_ ABIOS \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-125">538 (0x21A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-126">Error en el subsistema ABIOS.</span><span class="sxs-lookup"><span data-stu-id="f32a5-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR \_ WX86 \_ ADVERTENCIA**</span><span class="sxs-lookup"><span data-stu-id="f32a5-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-128">539 (0x21B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-129">Se produjo una advertencia en el subsistema WX86.</span><span class="sxs-lookup"><span data-stu-id="f32a5-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Error \_ WX86 \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-131">540 (0x21C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-132">Error en el subsistema WX86.</span><span class="sxs-lookup"><span data-stu-id="f32a5-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**\_no se \_ canceló el temporizador de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-134">541 (0x21D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-135">Se intentó cancelar o establecer un temporizador que tiene un APC asociado y el subproceso de asunto no es el subproceso que estableció originalmente el temporizador con una rutina APC asociada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR de \_ DESenredado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-137">542 (0x21E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-138">Código de la excepción de desenredado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR en la \_ \_ pila incorrecta**</span><span class="sxs-lookup"><span data-stu-id="f32a5-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-140">543 (0x21F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-141">Se encontró una pila no válida o no alineada durante una operación de desenredo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR \_ de \_ desenredado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-143">544 (0x220)</span><span class="sxs-lookup"><span data-stu-id="f32a5-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-144">Se encontró un destino de desenredado no válido durante una operación de desenredo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR \_ de \_ atributos de puerto no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-146">545 (0x221)</span><span class="sxs-lookup"><span data-stu-id="f32a5-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-147">Atributos de objeto no válidos especificados para NtCreatePort o atributos de puerto no válidos especificados en NtConnectPort</span><span class="sxs-lookup"><span data-stu-id="f32a5-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**mensaje de puerto de ERROR \_ \_ \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-149">546 (0x222)</span><span class="sxs-lookup"><span data-stu-id="f32a5-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-150">La longitud del mensaje pasado a NtRequestPort o NtRequestWaitReplyPort era mayor que el mensaje máximo permitido por el puerto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR \_ de \_ cuota \_ inferior no válida**</span><span class="sxs-lookup"><span data-stu-id="f32a5-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-152">547 (0x223)</span><span class="sxs-lookup"><span data-stu-id="f32a5-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-153">Se intentó reducir un límite de cuota por debajo del uso actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**el \_ dispositivo de error \_ ya está \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-155">548 (0x224)</span><span class="sxs-lookup"><span data-stu-id="f32a5-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-156">Se intentó asociar a un dispositivo que ya estaba conectado a otro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR de alineación de la instrucción de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-158">549 (0x225)</span><span class="sxs-lookup"><span data-stu-id="f32a5-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-159">Se intentó ejecutar una instrucción en una dirección no alineada y el sistema host no admite referencias de instrucciones no alineadas.</span><span class="sxs-lookup"><span data-stu-id="f32a5-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR de \_ generación de perfiles \_ no \_ iniciada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-161">550 (0x226)</span><span class="sxs-lookup"><span data-stu-id="f32a5-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-162">No se ha iniciado la generación de perfiles.</span><span class="sxs-lookup"><span data-stu-id="f32a5-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**\_ \_ no se \_ ha detenido la generación de perfiles de errores**</span><span class="sxs-lookup"><span data-stu-id="f32a5-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-164">551 (0x227)</span><span class="sxs-lookup"><span data-stu-id="f32a5-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-165">La generación de perfiles no se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR \_ no se pudo \_ \_ interpretar**</span><span class="sxs-lookup"><span data-stu-id="f32a5-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-167">552 (0x228)</span><span class="sxs-lookup"><span data-stu-id="f32a5-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-168">La ACL pasada no contenía la información mínima necesaria.</span><span class="sxs-lookup"><span data-stu-id="f32a5-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR \_ al generar perfiles \_ en el \_ límite**</span><span class="sxs-lookup"><span data-stu-id="f32a5-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-170">553 (0x229)</span><span class="sxs-lookup"><span data-stu-id="f32a5-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-171">El número de objetos de generación de perfiles activos es el máximo y no se pueden iniciar más.</span><span class="sxs-lookup"><span data-stu-id="f32a5-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR de espera de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-173">554 (0x22A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-174">Se utiliza para indicar que una operación no puede continuar sin bloqueos para e/s.</span><span class="sxs-lookup"><span data-stu-id="f32a5-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR no se pudo \_ \_ finalizar por \_ sí mismo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-176">555 (0x22B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-177">Indica que un subproceso intentó finalizarse de forma predeterminada (denominada NtTerminateThread con **null**) y era el último subproceso del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR \_ inesperado \_ mm \_ Create \_ Err**</span><span class="sxs-lookup"><span data-stu-id="f32a5-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-179">556 (0x22C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-180">Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que está en el filtro.</span><span class="sxs-lookup"><span data-stu-id="f32a5-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="f32a5-181">En este caso, la información se pierde; sin embargo, el filtro controla la excepción correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**error \_ inesperado de \_ asignación de mm \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-183">557 (0x22D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-184">Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que está en el filtro.</span><span class="sxs-lookup"><span data-stu-id="f32a5-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="f32a5-185">En este caso, la información se pierde; sin embargo, el filtro controla la excepción correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR \_ inesperado \_ mm \_ Extend \_ Err**</span><span class="sxs-lookup"><span data-stu-id="f32a5-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-187">558 (0x22E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-188">Si se devuelve un error MM que no está definido en el filtro FsRtl estándar, se convierte en uno de los siguientes errores que se garantiza que está en el filtro.</span><span class="sxs-lookup"><span data-stu-id="f32a5-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="f32a5-189">En este caso, la información se pierde; sin embargo, el filtro controla la excepción correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR en la \_ tabla de funciones erróneas \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-191">559 (0x22F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-192">Se encontró una tabla de funciones incorrecta durante una operación de desenredo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR \_ sin \_ traducción de GUID \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-194">560 (0x230)</span><span class="sxs-lookup"><span data-stu-id="f32a5-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-195">Indica que se ha intentado asignar la protección a un archivo o directorio del sistema de archivos y uno de los SID del descriptor de seguridad no se puede traducir en un GUID que el sistema de archivos pudiera almacenar.</span><span class="sxs-lookup"><span data-stu-id="f32a5-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="f32a5-196">Esto hace que se produzca un error en el intento de protección, lo que puede provocar un error al intentar crear un archivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR \_ de \_ tamaño de LDT no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-198">561 (0x231)</span><span class="sxs-lookup"><span data-stu-id="f32a5-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-199">Indica que se ha intentado aumentar un LDT estableciendo su tamaño o que el tamaño no era un número par de selectores.</span><span class="sxs-lookup"><span data-stu-id="f32a5-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR en el \_ \_ desplazamiento LDT no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-201">563 (0x233)</span><span class="sxs-lookup"><span data-stu-id="f32a5-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-202">Indica que el valor inicial para la información de LDT no era un múltiplo entero del tamaño del selector.</span><span class="sxs-lookup"><span data-stu-id="f32a5-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR \_ de \_ \_ descriptor LDT no válido**</span><span class="sxs-lookup"><span data-stu-id="f32a5-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-204">564 (0x234)</span><span class="sxs-lookup"><span data-stu-id="f32a5-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-205">Indica que el usuario proporcionó un descriptor no válido al intentar configurar los descriptores de LDT.</span><span class="sxs-lookup"><span data-stu-id="f32a5-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR \_ demasiados \_ \_ subprocesos**</span><span class="sxs-lookup"><span data-stu-id="f32a5-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-207">565 (0x235)</span><span class="sxs-lookup"><span data-stu-id="f32a5-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-208">Indica que un proceso tiene demasiados subprocesos para realizar la acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="f32a5-209">Por ejemplo, la asignación de un token principal solo se puede realizar cuando un proceso tiene cero o un subproceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_subproceso \_ de error no \_ en \_ proceso**</span><span class="sxs-lookup"><span data-stu-id="f32a5-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-211">566 (0x236)</span><span class="sxs-lookup"><span data-stu-id="f32a5-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-212">Se intentó operar en un subproceso en un proceso específico, pero el subproceso especificado no se encuentra en el proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**cuota de archivo de ERROR \_ \_ \_ superada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-214">567 (0x237)</span><span class="sxs-lookup"><span data-stu-id="f32a5-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-215">Se superó la cuota del archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**conflicto de servidor de inicio de sesión de ERROR \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-217">568 (0x238)</span><span class="sxs-lookup"><span data-stu-id="f32a5-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-218">No se puede iniciar el servicio NetLogon porque otro servicio NetLogon que se ejecuta en el dominio está en conflicto con el rol especificado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**sincronización de errores \_ \_ requerida**</span><span class="sxs-lookup"><span data-stu-id="f32a5-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-220">569 (0x239)</span><span class="sxs-lookup"><span data-stu-id="f32a5-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-221">La base de datos SAM de un servidor de Windows está muy fuera de sincronización con la copia en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f32a5-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="f32a5-222">Se requiere una sincronización completa.</span><span class="sxs-lookup"><span data-stu-id="f32a5-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR \_ \_ al abrir net Open \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-224">570 (0x23A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-225">Error de la API de NtCreateFile.</span><span class="sxs-lookup"><span data-stu-id="f32a5-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="f32a5-226">Este error nunca debe devolverse a una aplicación, sino que es un marcador de posición para que el redirector de Windows LAN Manager lo use en sus rutinas de asignación de errores internas.</span><span class="sxs-lookup"><span data-stu-id="f32a5-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR de \_ privilegio de e/s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-228">571 (0x23B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-229">{Error de privilegio} No se pudieron cambiar los permisos de e/s para el proceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**salida de control de errores \_ \_ C \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-231">572 (0x23C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-232">{Cierre de la aplicación con CTRL + C} La aplicación terminó como resultado de CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="f32a5-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR: \_ falta \_ SYSTEMFILE**</span><span class="sxs-lookup"><span data-stu-id="f32a5-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-234">573 (0x23D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-235">{Falta el archivo del sistema} Falta el archivo de sistema requerido% HS o no es válido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR de \_ excepción no controlada \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-237">574 (0x23E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-238">{Error de aplicación} La excepción% s (0x% 08lX) se produjo en la aplicación en la ubicación 0x% 08lX.</span><span class="sxs-lookup"><span data-stu-id="f32a5-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR \_ de \_ inicialización de la aplicación \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-240">575 (0x23F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-241">{Error de aplicación} La aplicación no pudo iniciarse correctamente (0x% LX).</span><span class="sxs-lookup"><span data-stu-id="f32a5-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="f32a5-242">Haga clic en Aceptar para cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR \_ \_ al crear el archivo de paginación \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-244">576 (0x240)</span><span class="sxs-lookup"><span data-stu-id="f32a5-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-245">{No se puede crear el archivo de paginación} No se pudo crear el archivo de paginación% HS (% LX).</span><span class="sxs-lookup"><span data-stu-id="f32a5-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="f32a5-246">El tamaño solicitado era% ld.</span><span class="sxs-lookup"><span data-stu-id="f32a5-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR \_ de \_ valor hash de imagen no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-248">577 (0x241)</span><span class="sxs-lookup"><span data-stu-id="f32a5-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-249">Windows no puede comprobar la firma digital de este archivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="f32a5-250">Un cambio de hardware o software reciente podría haber instalado un archivo firmado incorrectamente o dañado, o que podría ser software malintencionado de un origen desconocido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR \_ sin archivo de \_ paginación**</span><span class="sxs-lookup"><span data-stu-id="f32a5-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-252">578 (0x242)</span><span class="sxs-lookup"><span data-stu-id="f32a5-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-253">{No se especificó ningún archivo de paginación} No se especificó ningún archivo de paginación en la configuración del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR \_ de \_ contexto de punto flotante no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-255">579 (0x243)</span><span class="sxs-lookup"><span data-stu-id="f32a5-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-256">EXCEPCIONAL Una aplicación en modo real emitió una instrucción de punto flotante y el hardware de punto flotante no está presente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**\_no hay \_ ningún \_ par de eventos de error**</span><span class="sxs-lookup"><span data-stu-id="f32a5-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-258">580 (0x244)</span><span class="sxs-lookup"><span data-stu-id="f32a5-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-259">Se ha realizado una operación de sincronización de un par de eventos mediante el objeto de par de eventos cliente/servidor específico del subproceso, pero no hay ningún objeto de par de eventos asociado al subproceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**error de configuración del dominio de ERROR del \_ \_ control \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-261">581 (0x245)</span><span class="sxs-lookup"><span data-stu-id="f32a5-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-262">Un servidor de Windows tiene una configuración incorrecta.</span><span class="sxs-lookup"><span data-stu-id="f32a5-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR \_ de \_ carácter no válido**</span><span class="sxs-lookup"><span data-stu-id="f32a5-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-264">582 (0x246)</span><span class="sxs-lookup"><span data-stu-id="f32a5-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-265">Se encontró un carácter no válido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-265">An illegal character was encountered.</span></span> <span data-ttu-id="f32a5-266">Para un juego de caracteres de varios bytes, esto incluye un byte inicial sin un byte final subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="f32a5-267">En el caso del juego de caracteres Unicode, se incluyen los caracteres 0xFFFF y 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="f32a5-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**carácter no definido de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-269">583 (0x247)</span><span class="sxs-lookup"><span data-stu-id="f32a5-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-270">El carácter Unicode no está definido en el juego de caracteres Unicode instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**\_volumen de disquete de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-272">584 (0x248)</span><span class="sxs-lookup"><span data-stu-id="f32a5-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-273">No se puede crear el archivo de paginación en un disquete.</span><span class="sxs-lookup"><span data-stu-id="f32a5-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR \_ \_ de BIOS \_ al \_ conectar la \_ interrupción**</span><span class="sxs-lookup"><span data-stu-id="f32a5-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-275">585 (0x249)</span><span class="sxs-lookup"><span data-stu-id="f32a5-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-276">El BIOS del sistema no pudo conectar una interrupción del sistema al dispositivo o al bus al que está conectado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR de \_ controlador de copia de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-278">586 (0x24A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-279">Esta operación solo se permite para el controlador de dominio principal del dominio.</span><span class="sxs-lookup"><span data-stu-id="f32a5-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_límite de mutaciones de error \_ \_ superado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-281">587 (0x24B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-282">Se intentó adquirir un mutante, de modo que se habría superado su recuento máximo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR \_ de \_ controlador de FS \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="f32a5-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-284">588 (0x24C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-285">Se ha tenido acceso a un volumen para el que se requiere un controlador del sistema de archivos que aún no se ha cargado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR: \_ no se puede \_ cargar el \_ archivo de registro \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-287">589 (0x24D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-288">{Error del archivo de registro} El registro no puede cargar el subárbol (archivo):% HS o su registro o alternativo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="f32a5-289">Está dañado, no existe o no se puede escribir en él.</span><span class="sxs-lookup"><span data-stu-id="f32a5-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR \_ \_ al adjuntar error de depuración \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-291">590 (0x24E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-292">{Error inesperado en [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Error inesperado al procesar una solicitud de API **DebugActiveProcess** .</span><span class="sxs-lookup"><span data-stu-id="f32a5-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="f32a5-293">Puede elegir aceptar para finalizar el proceso o cancelar para omitir el error.</span><span class="sxs-lookup"><span data-stu-id="f32a5-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR en el \_ proceso del sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-295">591 (0x24F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-296">{Error irrecuperable del sistema} El proceso del sistema% HS terminó inesperadamente con un estado de 0x% 08x (0x% 08x 0x% 08x).</span><span class="sxs-lookup"><span data-stu-id="f32a5-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="f32a5-297">El sistema se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**\_no se \_ \_ aceptan datos de error**</span><span class="sxs-lookup"><span data-stu-id="f32a5-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-299">592 (0x250)</span><span class="sxs-lookup"><span data-stu-id="f32a5-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-300">{Datos no aceptados} El cliente TDI no pudo controlar los datos recibidos durante una indicación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**error \_ de \_ VDM \_ error**</span><span class="sxs-lookup"><span data-stu-id="f32a5-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-302">593 (0x251)</span><span class="sxs-lookup"><span data-stu-id="f32a5-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-303">NTVDM ha detectado un error de hardware.</span><span class="sxs-lookup"><span data-stu-id="f32a5-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**\_tiempo de \_ espera de cancelación del controlador de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-305">594 (0x252)</span><span class="sxs-lookup"><span data-stu-id="f32a5-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-306">{Cancelar tiempo de espera} El controlador% HS no pudo completar una solicitud de e/s cancelada en el tiempo asignado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR \_ de \_ coincidencia de mensaje de respuesta \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-308">595 (0x253)</span><span class="sxs-lookup"><span data-stu-id="f32a5-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-309">{Error de coincidencia del mensaje de respuesta} Se intentó responder a un mensaje LPC, pero el subproceso especificado por el identificador de cliente en el mensaje no estaba esperando en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f32a5-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR al \_ perder los \_ datos de WRITEBEHIND \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-311">596 (0x254)</span><span class="sxs-lookup"><span data-stu-id="f32a5-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-312">{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS.</span><span class="sxs-lookup"><span data-stu-id="f32a5-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="f32a5-313">Se han perdido los datos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-313">The data has been lost.</span></span> <span data-ttu-id="f32a5-314">Este error puede deberse a un error del hardware del equipo o de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="f32a5-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="f32a5-315">Intente guardar este archivo en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR de \_ parámetros de servidor de cliente \_ \_ \_ no válidos**</span><span class="sxs-lookup"><span data-stu-id="f32a5-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-317">597 (0x255)</span><span class="sxs-lookup"><span data-stu-id="f32a5-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-318">Los parámetros pasados al servidor en la ventana memoria compartida de cliente/servidor no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="f32a5-319">Es posible que se hayan colocado demasiados datos en la ventana memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="f32a5-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR \_ no es un \_ \_ flujo reducido**</span><span class="sxs-lookup"><span data-stu-id="f32a5-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-321">598 (0x256)</span><span class="sxs-lookup"><span data-stu-id="f32a5-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-322">La secuencia no es una secuencia pequeña.</span><span class="sxs-lookup"><span data-stu-id="f32a5-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR de \_ desbordamiento de pila de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-324">599 (0x257)</span><span class="sxs-lookup"><span data-stu-id="f32a5-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-325">La solicitud debe controlarse mediante el código de desbordamiento de pila.</span><span class="sxs-lookup"><span data-stu-id="f32a5-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR \_ \_ al convertir a \_ grande**</span><span class="sxs-lookup"><span data-stu-id="f32a5-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-327">600 (0x258)</span><span class="sxs-lookup"><span data-stu-id="f32a5-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-328">Códigos de estado de OFS internos que indican cómo se controla una operación de asignación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="f32a5-329">Se reintentará después de que se mueva el onode contenedor o hasta que el flujo de la extensión se convierta en una secuencia grande.</span><span class="sxs-lookup"><span data-stu-id="f32a5-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR \_ detectado \_ fuera \_ de \_ ámbito**</span><span class="sxs-lookup"><span data-stu-id="f32a5-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-331">601 (0x259)</span><span class="sxs-lookup"><span data-stu-id="f32a5-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-332">El intento de buscar el objeto encontró un objeto que coincide con el identificador en el volumen pero está fuera del ámbito del identificador usado para la operación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR al \_ asignar el \_ depósito**</span><span class="sxs-lookup"><span data-stu-id="f32a5-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-334">602 (0x25A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-335">La matriz de depósitos debe crecer.</span><span class="sxs-lookup"><span data-stu-id="f32a5-335">The bucket array must be grown.</span></span> <span data-ttu-id="f32a5-336">Vuelva a intentar la transacción después de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**\_desbordamiento de serialización de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-338">603 (0x25B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-339">Se ha desbordado el búfer de serialización de usuario/kernel.</span><span class="sxs-lookup"><span data-stu-id="f32a5-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR \_ de \_ variante no válida**</span><span class="sxs-lookup"><span data-stu-id="f32a5-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-341">604 (0x25C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-342">La estructura de variante proporcionada contiene datos no válidos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR \_ de \_ búfer de compresión incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-344">605 (0x25D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-345">El búfer especificado contiene datos con formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR de auditoría de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-347">606 (0x25E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-348">{Error de auditoría} Error al tratar de generar una auditoría de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f32a5-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**\_no se \_ estableció la resolución del temporizador \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-350">607 (0x25F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-351">La resolución del temporizador no se estableció previamente en el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR \_ : \_ información de inicio de sesión insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-353">608 (0x260)</span><span class="sxs-lookup"><span data-stu-id="f32a5-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-354">No hay suficiente información de cuenta para iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="f32a5-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR de punto de entrada de \_ \_ dll incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-356">609 (0x261)</span><span class="sxs-lookup"><span data-stu-id="f32a5-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-357">{Punto de entrada de DLL no válido} La biblioteca de vínculos dinámicos% HS no se ha escrito correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="f32a5-358">El puntero de pila se ha dejado en un estado incoherente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="f32a5-359">El punto de entrada debe declararse como WINAPI o STDCALL.</span><span class="sxs-lookup"><span data-stu-id="f32a5-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="f32a5-360">Seleccione Sí para no realizar la carga de la DLL.</span><span class="sxs-lookup"><span data-stu-id="f32a5-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="f32a5-361">Seleccione NO para continuar con la ejecución.</span><span class="sxs-lookup"><span data-stu-id="f32a5-361">Select NO to continue execution.</span></span> <span data-ttu-id="f32a5-362">La selección de NO puede hacer que la aplicación NO funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR de punto de entrada de \_ \_ servicio incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-364">610 (0x262)</span><span class="sxs-lookup"><span data-stu-id="f32a5-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-365">{Punto de entrada de devolución de llamada de servicio no válido} El servicio% HS no se ha escrito correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="f32a5-366">El puntero de pila se ha dejado en un estado incoherente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="f32a5-367">El punto de entrada de devolución de llamada debe declararse como WINAPI o STDCALL.</span><span class="sxs-lookup"><span data-stu-id="f32a5-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="f32a5-368">Si selecciona Aceptar, el servicio continuará la operación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="f32a5-369">Sin embargo, es posible que el proceso de servicio no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR \_ de \_ dirección IP \_ CONFLICT1**</span><span class="sxs-lookup"><span data-stu-id="f32a5-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-371">611 (0x263)</span><span class="sxs-lookup"><span data-stu-id="f32a5-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-372">Hay un conflicto de dirección IP con otro sistema de la red.</span><span class="sxs-lookup"><span data-stu-id="f32a5-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR \_ de \_ dirección IP \_ CONFLICT2**</span><span class="sxs-lookup"><span data-stu-id="f32a5-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-374">612 (0x264)</span><span class="sxs-lookup"><span data-stu-id="f32a5-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-375">Hay un conflicto de dirección IP con otro sistema de la red.</span><span class="sxs-lookup"><span data-stu-id="f32a5-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_límite de \_ cuota del registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-377">613 (0x265)</span><span class="sxs-lookup"><span data-stu-id="f32a5-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-378">{Espacio insuficiente en el registro} El sistema ha alcanzado el tamaño máximo permitido para la parte del sistema del registro.</span><span class="sxs-lookup"><span data-stu-id="f32a5-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="f32a5-379">Se omitirán las solicitudes de almacenamiento adicionales.</span><span class="sxs-lookup"><span data-stu-id="f32a5-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR: \_ no hay ninguna \_ devolución de llamada \_ activa**</span><span class="sxs-lookup"><span data-stu-id="f32a5-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-381">614 (0x266)</span><span class="sxs-lookup"><span data-stu-id="f32a5-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-382">No se puede ejecutar un servicio de sistema de devolución de devolución de llamada cuando no hay ninguna devolución de llamada activa.</span><span class="sxs-lookup"><span data-stu-id="f32a5-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR \_ pwd \_ demasiado \_ corto**</span><span class="sxs-lookup"><span data-stu-id="f32a5-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-384">615 (0x267)</span><span class="sxs-lookup"><span data-stu-id="f32a5-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-385">La contraseña proporcionada es demasiado corta para cumplir con la Directiva de su cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f32a5-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="f32a5-386">Elija una contraseña más larga.</span><span class="sxs-lookup"><span data-stu-id="f32a5-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR \_ pwd \_ demasiado \_ reciente**</span><span class="sxs-lookup"><span data-stu-id="f32a5-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-388">616 (0x268)</span><span class="sxs-lookup"><span data-stu-id="f32a5-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-389">La Directiva de su cuenta de usuario no permite cambiar las contraseñas con demasiada frecuencia.</span><span class="sxs-lookup"><span data-stu-id="f32a5-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="f32a5-390">Esto se hace para evitar que los usuarios cambien a una contraseña conocida, pero potencialmente detectada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="f32a5-391">Si cree que la contraseña se ha puesto en peligro, póngase en contacto con el administrador inmediatamente para tener una nueva asignada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**conflicto de historial de ERROR \_ pwd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-393">617 (0x269)</span><span class="sxs-lookup"><span data-stu-id="f32a5-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-394">Ha intentado cambiar la contraseña por una que ha usado en el pasado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="f32a5-395">La Directiva de su cuenta de usuario no lo permite.</span><span class="sxs-lookup"><span data-stu-id="f32a5-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="f32a5-396">Seleccione una contraseña que no haya usado previamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR de \_ compresión no admitida \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-398">618 (0x26A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-399">El formato de compresión especificado no es compatible.</span><span class="sxs-lookup"><span data-stu-id="f32a5-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR \_ de \_ Perfil de HW no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-401">619 (0x26B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-402">La configuración de Perfil de hardware especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="f32a5-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR en la \_ \_ ruta de acceso del dispositivo PLUGPLAY no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-404">620 (0x26C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-405">La ruta de acceso del dispositivo del registro de Plug and Play especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="f32a5-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**lista de cuotas de ERROR \_ \_ \_ incoherente**</span><span class="sxs-lookup"><span data-stu-id="f32a5-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-407">621 (0x26D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-408">La lista de cuotas especificada es incoherente internamente con su descriptor.</span><span class="sxs-lookup"><span data-stu-id="f32a5-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**expiración de la evaluación de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-410">622 (0x26E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-411">{Notificación de evaluación de Windows} El período de evaluación de esta instalación de Windows ha expirado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="f32a5-412">Este sistema se apagará en 1 hora.</span><span class="sxs-lookup"><span data-stu-id="f32a5-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="f32a5-413">Para restaurar el acceso a esta instalación de Windows, actualice esta instalación mediante una distribución con licencia de este producto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR \_ de \_ reubicación de dll no válida \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-415">623 (0x26F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-416">{Reubicación de DLL del sistema no válida} La DLL del sistema% HS se reubicaba en la memoria.</span><span class="sxs-lookup"><span data-stu-id="f32a5-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="f32a5-417">La aplicación no se ejecutará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-417">The application will not run properly.</span></span> <span data-ttu-id="f32a5-418">La reubicación se produjo porque el archivo DLL% HS ocupaba un intervalo de direcciones reservado para los archivos DLL del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="f32a5-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="f32a5-419">Se debe poner en contacto con el proveedor que suministra el archivo DLL para obtener un nuevo archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="f32a5-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR \_ \_ \_ al cerrar la sesión de dll init \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-421">624 (0x270)</span><span class="sxs-lookup"><span data-stu-id="f32a5-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-422">{Error de inicialización de DLL} No se pudo inicializar la aplicación porque la estación de ventana se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="f32a5-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR al \_ validar la validación \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-424">625 (0x271)</span><span class="sxs-lookup"><span data-stu-id="f32a5-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-425">El proceso de validación debe continuar con el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR: \_ no hay \_ más \_ coincidencias**</span><span class="sxs-lookup"><span data-stu-id="f32a5-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-427">626 (0x272)</span><span class="sxs-lookup"><span data-stu-id="f32a5-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-428">No hay más coincidencias para la enumeración de índice actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_conflicto de \_ lista de intervalos de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-430">627 (0x273)</span><span class="sxs-lookup"><span data-stu-id="f32a5-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-431">No se pudo agregar el intervalo a la lista de intervalos debido a un conflicto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR \_ de \_ coincidencia de SID de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-433">628 (0x274)</span><span class="sxs-lookup"><span data-stu-id="f32a5-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-434">El proceso de servidor se está ejecutando con un SID diferente del que requiere el cliente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR no se \_ \_ permite habilitar \_ solo denegar \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-436">629 (0x275)</span><span class="sxs-lookup"><span data-stu-id="f32a5-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-437">No se puede habilitar un grupo marcado como usar para denegar únicamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR \_ float \_ varios \_ errores**</span><span class="sxs-lookup"><span data-stu-id="f32a5-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-439">630 (0x276)</span><span class="sxs-lookup"><span data-stu-id="f32a5-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-440">EXCEPCIONAL Varios errores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f32a5-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR \_ float \_ varias \_ capturas**</span><span class="sxs-lookup"><span data-stu-id="f32a5-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-442">631 (0x277)</span><span class="sxs-lookup"><span data-stu-id="f32a5-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-443">EXCEPCIONAL Varias capturas de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="f32a5-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR \_ NOinterface**</span><span class="sxs-lookup"><span data-stu-id="f32a5-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-445">632 (0x278)</span><span class="sxs-lookup"><span data-stu-id="f32a5-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-446">No se admite la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR \_ \_ al \_ suspender el controlador**</span><span class="sxs-lookup"><span data-stu-id="f32a5-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-448">633 (0x279)</span><span class="sxs-lookup"><span data-stu-id="f32a5-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-449">{Error de espera del sistema} El controlador% HS no admite el modo de espera.</span><span class="sxs-lookup"><span data-stu-id="f32a5-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="f32a5-450">La actualización de este controlador puede permitir que el sistema entre en modo de espera.</span><span class="sxs-lookup"><span data-stu-id="f32a5-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR \_ de \_ archivo de sistema dañado \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-452">634 (0x27A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-453">El archivo de sistema %1 se ha dañado y se ha reemplazado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**compromiso de ERROR \_ \_ mínimo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-455">635 (0x27B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-456">{Memoria virtual mínima demasiado baja} El sistema tiene poca memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="f32a5-457">Windows está aumentando el tamaño del archivo de paginación de la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="f32a5-458">Durante este proceso, es posible que se denieguen las solicitudes de memoria para algunas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f32a5-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="f32a5-459">Para obtener más información, vea la ayuda de.</span><span class="sxs-lookup"><span data-stu-id="f32a5-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR \_ de \_ enumeración de reinicio PNP \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-461">636 (0x27C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-462">Se quitó un dispositivo, por lo que la enumeración debe reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="f32a5-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**\_ \_ firma incorrecta de imagen de sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-464">637 (0x27D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-465">{Error irrecuperable del sistema} La imagen del sistema% s no está firmada correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="f32a5-466">El archivo se ha reemplazado por el archivo firmado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="f32a5-467">El sistema se ha cerrado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR \_ se \_ requiere reinicio de PNP \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-469">638 (0x27E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-470">El dispositivo no se iniciará sin necesidad de reiniciar.</span><span class="sxs-lookup"><span data-stu-id="f32a5-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR \_ de \_ energía insuficiente**</span><span class="sxs-lookup"><span data-stu-id="f32a5-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-472">639 (0x27F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-473">No hay suficiente capacidad para completar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR \_ de \_ infracción de varios errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-475">640 (0x280)</span><span class="sxs-lookup"><span data-stu-id="f32a5-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-476">ERROR \_ de \_ infracción de varios errores \_</span><span class="sxs-lookup"><span data-stu-id="f32a5-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR \_ de \_ apagado del sistema**</span><span class="sxs-lookup"><span data-stu-id="f32a5-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-478">641 (0x281)</span><span class="sxs-lookup"><span data-stu-id="f32a5-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-479">El sistema está en proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="f32a5-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**\_no se \_ ha \_ establecido el puerto de error**</span><span class="sxs-lookup"><span data-stu-id="f32a5-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-481">642 (0x282)</span><span class="sxs-lookup"><span data-stu-id="f32a5-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-482">Se ha intentado quitar un proceso depurado, pero aún no se ha asociado un puerto al proceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR \_ de \_ comprobación de versión de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-484">643 (0x283)</span><span class="sxs-lookup"><span data-stu-id="f32a5-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-485">Esta versión de Windows no es compatible con la versión de comportamiento del bosque de directorio, el dominio o el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="f32a5-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_ \_ no \_ se encontró el intervalo de errores**</span><span class="sxs-lookup"><span data-stu-id="f32a5-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-487">644 (0x284)</span><span class="sxs-lookup"><span data-stu-id="f32a5-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-488">No se pudo encontrar el intervalo especificado en la lista de intervalos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR \_ de \_ \_ controlador de modo seguro \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-490">646 (0x286)</span><span class="sxs-lookup"><span data-stu-id="f32a5-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-491">No se cargó el controlador porque el sistema se está iniciando en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="f32a5-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR en la \_ \_ entrada del controlador \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-493">647 (0x287)</span><span class="sxs-lookup"><span data-stu-id="f32a5-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-494">No se cargó el controlador porque no se pudo realizar la llamada de inicialización.</span><span class="sxs-lookup"><span data-stu-id="f32a5-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**error \_ de \_ enumeración de dispositivos error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-496">648 (0x288)</span><span class="sxs-lookup"><span data-stu-id="f32a5-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-497">"% HS" encontró un error al aplicar la energía o leer la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="f32a5-498">Esto puede deberse a un error del hardware o a una mala conexión.</span><span class="sxs-lookup"><span data-stu-id="f32a5-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**\_no se \_ \_ ha \_ resuelto el punto de montaje de error**</span><span class="sxs-lookup"><span data-stu-id="f32a5-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-500">649 (0x289)</span><span class="sxs-lookup"><span data-stu-id="f32a5-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-501">No se pudo realizar la operación de creación porque el nombre contenía al menos un punto de montaje que se resuelve en un volumen al que no está asociado el objeto de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR \_ de \_ \_ parámetro de objeto de dispositivo no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-503">650 (0x28A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-504">El parámetro de objeto de dispositivo no es un objeto de dispositivo válido o no está asociado al volumen especificado por el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR \_ MCA \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-506">651 (0x28B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-507">Se ha producido un error de comprobación del equipo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="f32a5-508">Compruebe el registro de eventos del sistema para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="f32a5-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**error \_ de \_ base de datos de controlador de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-510">652 (0x28C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-511">Error \[ %2 al \] procesar la base de datos del controlador.</span><span class="sxs-lookup"><span data-stu-id="f32a5-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**\_subárbol del sistema de errores \_ \_ demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="f32a5-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-513">653 (0x28D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-514">El tamaño de Hive del sistema ha superado el límite.</span><span class="sxs-lookup"><span data-stu-id="f32a5-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR de la \_ \_ \_ \_ descarga anterior del controlador de errores**</span><span class="sxs-lookup"><span data-stu-id="f32a5-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-516">654 (0x28E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-517">No se pudo cargar el controlador porque una versión anterior del controlador todavía está en la memoria.</span><span class="sxs-lookup"><span data-stu-id="f32a5-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR de \_ VOLSNAP \_ preparar \_ hibernación**</span><span class="sxs-lookup"><span data-stu-id="f32a5-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-519">655 (0x28F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-520">{Servicio de instantáneas de volumen} Espere mientras el Servicio de instantáneas de volumen prepara el volumen% HS para la hibernación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR de \_ hibernación de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-522">656 (0x290)</span><span class="sxs-lookup"><span data-stu-id="f32a5-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-523">No se pudo hibernar el sistema (el código de error es% HS).</span><span class="sxs-lookup"><span data-stu-id="f32a5-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="f32a5-524">La hibernación se deshabilitará hasta que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR \_ pwd \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-526">657 (0x291)</span><span class="sxs-lookup"><span data-stu-id="f32a5-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-527">La contraseña proporcionada es demasiado larga para cumplir con la Directiva de su cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="f32a5-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="f32a5-528">Elija una contraseña más corta.</span><span class="sxs-lookup"><span data-stu-id="f32a5-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_ \_ limitación del sistema de archivos de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-530">665 (0x299)</span><span class="sxs-lookup"><span data-stu-id="f32a5-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-531">no se pudo completar la operación solicitada por una limitación del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**error de aserción de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-533">668 (0x29C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-534">Error de aserción.</span><span class="sxs-lookup"><span data-stu-id="f32a5-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**error \_ ACPI de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-536">669 (0x29D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-537">Error en el subsistema ACPI.</span><span class="sxs-lookup"><span data-stu-id="f32a5-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR \_ de \_ aserción wow**</span><span class="sxs-lookup"><span data-stu-id="f32a5-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-539">670 (0x29E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-540">Error de aserción WOW.</span><span class="sxs-lookup"><span data-stu-id="f32a5-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR en la \_ \_ \_ \_ tabla MPS errónea de PNP**</span><span class="sxs-lookup"><span data-stu-id="f32a5-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-542">671 (0x29F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-543">Falta un dispositivo en la tabla MPS del BIOS del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="f32a5-544">Este dispositivo no se usará.</span><span class="sxs-lookup"><span data-stu-id="f32a5-544">This device will not be used.</span></span> <span data-ttu-id="f32a5-545">Póngase en contacto con el proveedor del sistema para actualizar el BIOS del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR \_ de \_ traducción de PNP \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-547">672 (0x2A0)</span><span class="sxs-lookup"><span data-stu-id="f32a5-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-548">Un traductor no pudo traducir los recursos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR \_ de \_ conversión de IRQ PNP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-550">673 (0x2A1)</span><span class="sxs-lookup"><span data-stu-id="f32a5-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-551">Un traductor de IRQ no pudo traducir los recursos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR \_ de \_ identificador no válido de PNP \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-553">674 (0x2A2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-554">El controlador %2 devolvió un ID. no válido para un dispositivo secundario (%3).</span><span class="sxs-lookup"><span data-stu-id="f32a5-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR de \_ reactivación \_ del sistema del \_ depurador**</span><span class="sxs-lookup"><span data-stu-id="f32a5-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-556">675 (0x2A3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-557">{Se activó el depurador de kernel} una interrupción activó el depurador del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**\_identificadores de error \_ cerrados**</span><span class="sxs-lookup"><span data-stu-id="f32a5-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-559">676 (0x2A4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-560">{Identificadores cerrados} Los identificadores de los objetos se han cerrado automáticamente como resultado de la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**\_información extraña de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-562">677 (0x2A5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-563">{Demasiada información} La lista de control de acceso (ACL) especificada contiene más información de la esperada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR \_ RXACT la \_ confirmación \_ necesaria**</span><span class="sxs-lookup"><span data-stu-id="f32a5-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-565">678 (0x2A6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-566">Este estado de nivel de advertencia indica que el estado de la transacción ya existe para el subárbol del registro, pero que se anuló previamente una confirmación de transacción.</span><span class="sxs-lookup"><span data-stu-id="f32a5-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="f32a5-567">La confirmación no se ha completado, pero no se ha revertido (por lo que se puede seguir confirmando si se desea).</span><span class="sxs-lookup"><span data-stu-id="f32a5-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_comprobación de medios de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-569">679 (0x2A7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-570">{Contenido multimedia cambiado} Es posible que el medio haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**sustitución de GUID de ERROR \_ \_ \_ realizada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-572">680 (0x2A8)</span><span class="sxs-lookup"><span data-stu-id="f32a5-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-573">{Sustitución de GUID} Durante la traducción de un identificador global (GUID) a un identificador de seguridad de Windows (SID), no se encontró ningún prefijo GUID definido por el administrador.</span><span class="sxs-lookup"><span data-stu-id="f32a5-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="f32a5-574">Se usó un prefijo sustitutivo, lo que no afectará A la seguridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="f32a5-575">Sin embargo, esto puede proporcionar un acceso más restrictivo que el previsto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR \_ detenido \_ en \_ SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="f32a5-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-577">681 (0x2A9)</span><span class="sxs-lookup"><span data-stu-id="f32a5-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-578">La operación de creación se detuvo después de llegar a un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="f32a5-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR \_ LONGJUMP**</span><span class="sxs-lookup"><span data-stu-id="f32a5-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-580">682 (0x2AA)</span><span class="sxs-lookup"><span data-stu-id="f32a5-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-581">Se ha ejecutado un salto largo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR \_ PLUGPLAY \_ consulta \_ vetada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-583">683 (0x2AB)</span><span class="sxs-lookup"><span data-stu-id="f32a5-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-584">La operación de consulta de Plug and Play no se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR al \_ DESenredar la \_ consolidación**</span><span class="sxs-lookup"><span data-stu-id="f32a5-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-586">684 (0x2AC)</span><span class="sxs-lookup"><span data-stu-id="f32a5-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-587">Se ha ejecutado una consolidación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="f32a5-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR \_ de \_ subárbol del registro \_ recuperado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-589">685 (0x2AD)</span><span class="sxs-lookup"><span data-stu-id="f32a5-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-590">{Subárbol del registro recuperado} El subárbol del registro (archivo):% HS estaba dañado y se ha recuperado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="f32a5-591">Algunos datos podrían haberse perdido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**el \_ archivo dll de error \_ puede no \_ ser \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="f32a5-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-593">686 (0x2AE)</span><span class="sxs-lookup"><span data-stu-id="f32a5-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-594">La aplicación está intentando ejecutar código ejecutable desde el módulo% HS.</span><span class="sxs-lookup"><span data-stu-id="f32a5-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="f32a5-595">Esto puede ser inseguro.</span><span class="sxs-lookup"><span data-stu-id="f32a5-595">This may be insecure.</span></span> <span data-ttu-id="f32a5-596">Existe una alternativa,% HS, disponible.</span><span class="sxs-lookup"><span data-stu-id="f32a5-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="f32a5-597">¿La aplicación debe usar el módulo seguro% HS?</span><span class="sxs-lookup"><span data-stu-id="f32a5-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**\_es posible que la dll de error no \_ \_ sea \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="f32a5-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-599">687 (0x2AF)</span><span class="sxs-lookup"><span data-stu-id="f32a5-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-600">La aplicación está cargando código ejecutable del módulo% HS.</span><span class="sxs-lookup"><span data-stu-id="f32a5-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="f32a5-601">Esto es seguro, pero puede que no sea compatible con las versiones anteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="f32a5-602">Existe una alternativa,% HS, disponible.</span><span class="sxs-lookup"><span data-stu-id="f32a5-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="f32a5-603">¿La aplicación debe usar el módulo seguro% HS?</span><span class="sxs-lookup"><span data-stu-id="f32a5-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR \_ dbg \_ \_ no se ha controlado la excepción \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-605">688 (0x2B0)</span><span class="sxs-lookup"><span data-stu-id="f32a5-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-606">El depurador no controló la excepción.</span><span class="sxs-lookup"><span data-stu-id="f32a5-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR \_ dbg: \_ respuesta \_ posterior**</span><span class="sxs-lookup"><span data-stu-id="f32a5-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-608">689 (0x2B1)</span><span class="sxs-lookup"><span data-stu-id="f32a5-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-609">El depurador responderá más adelante.</span><span class="sxs-lookup"><span data-stu-id="f32a5-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR \_ dbg \_ no se puede \_ \_ proporcionar el \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="f32a5-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-611">690 (0x2B2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-612">El depurador no puede proporcionar el identificador.</span><span class="sxs-lookup"><span data-stu-id="f32a5-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR \_ dbg: \_ finalizar \_ subproceso**</span><span class="sxs-lookup"><span data-stu-id="f32a5-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-614">691 (0x2B3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-615">El depurador finalizó el subproceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR \_ dbg: \_ finalizar \_ proceso**</span><span class="sxs-lookup"><span data-stu-id="f32a5-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-617">692 (0x2B4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-618">El depurador finalizó el proceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR \_ dbg ( \_ control) \_ C**</span><span class="sxs-lookup"><span data-stu-id="f32a5-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-620">693 (0x2B5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-621">El depurador tiene el control C.</span><span class="sxs-lookup"><span data-stu-id="f32a5-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR \_ dbg \_ PRINTEXCEPTION \_ C**</span><span class="sxs-lookup"><span data-stu-id="f32a5-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-623">694 (0x2B6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-624">Excepción impresa del depurador en el control C.</span><span class="sxs-lookup"><span data-stu-id="f32a5-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR \_ dbg \_ RIPEXCEPTION**</span><span class="sxs-lookup"><span data-stu-id="f32a5-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-626">695 (0x2B7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-627">El depurador recibió una excepción RIP.</span><span class="sxs-lookup"><span data-stu-id="f32a5-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR \_ dbg \_ ( \_ interrupción de control)**</span><span class="sxs-lookup"><span data-stu-id="f32a5-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-629">696 (0x2B8)</span><span class="sxs-lookup"><span data-stu-id="f32a5-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-630">El depurador recibió un salto de control.</span><span class="sxs-lookup"><span data-stu-id="f32a5-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR \_ dbg \_ excepción del comando \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-632">697 (0x2B9)</span><span class="sxs-lookup"><span data-stu-id="f32a5-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-633">Excepción de comunicación de comandos del depurador.</span><span class="sxs-lookup"><span data-stu-id="f32a5-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**\_el nombre del objeto de error \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="f32a5-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-635">698 (0x2BA)</span><span class="sxs-lookup"><span data-stu-id="f32a5-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-636">{Objeto existente} Se intentó crear un objeto y el nombre del objeto ya existía.</span><span class="sxs-lookup"><span data-stu-id="f32a5-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**el \_ subproceso de error \_ se \_ suspendió**</span><span class="sxs-lookup"><span data-stu-id="f32a5-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-638">699 (0x2BB)</span><span class="sxs-lookup"><span data-stu-id="f32a5-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-639">{Subproceso suspendido} Se ha producido una terminación del subproceso mientras se suspendió el subproceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="f32a5-640">El subproceso se reanudó y la terminación continuó.</span><span class="sxs-lookup"><span data-stu-id="f32a5-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_imagen \_ de error no \_ en \_ base**</span><span class="sxs-lookup"><span data-stu-id="f32a5-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-642">700 (0x2BC)</span><span class="sxs-lookup"><span data-stu-id="f32a5-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-643">{Imagen reubicada} No se pudo asignar un archivo de imagen en la dirección especificada en el archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="f32a5-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="f32a5-644">Las correcciones locales deben realizarse en esta imagen.</span><span class="sxs-lookup"><span data-stu-id="f32a5-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR de \_ RXACT de \_ estado \_ creado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-646">701 (0x2BD)</span><span class="sxs-lookup"><span data-stu-id="f32a5-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-647">Este estado de nivel informativo indica que el estado de una transacción de subárbol del registro especificada no existía todavía y se tenía que crear.</span><span class="sxs-lookup"><span data-stu-id="f32a5-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notificación de segmento de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-649">702 (0x2BE)</span><span class="sxs-lookup"><span data-stu-id="f32a5-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-650">{Carga de segmento} Una máquina DOS virtual (VDM) está cargando, descargando o moviendo una imagen de segmento de programa de MS-DOS o Win16.</span><span class="sxs-lookup"><span data-stu-id="f32a5-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="f32a5-651">Se produce una excepción para que un depurador pueda cargar, descargar o realizar un seguimiento de símbolos y puntos de interrupción dentro de estos segmentos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f32a5-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR \_ de \_ directorio actual no válido \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-653">703 (0x2BF)</span><span class="sxs-lookup"><span data-stu-id="f32a5-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-654">{Directorio actual no válido} El proceso no puede cambiar al directorio actual de inicio% HS.</span><span class="sxs-lookup"><span data-stu-id="f32a5-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="f32a5-655">Seleccione Aceptar para establecer el directorio actual en% HS o seleccione Cancelar para salir.</span><span class="sxs-lookup"><span data-stu-id="f32a5-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR \_ ft \_ leer \_ recuperación \_ de \_ copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="f32a5-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-657">704 (0x2C0)</span><span class="sxs-lookup"><span data-stu-id="f32a5-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-658">{Lectura redundante} Para satisfacer una solicitud de lectura, el sistema de archivos tolerante a errores de NT leyó correctamente los datos solicitados de una copia redundante.</span><span class="sxs-lookup"><span data-stu-id="f32a5-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="f32a5-659">Esto se ha hecho porque el sistema de archivos encontró un error en un miembro del volumen tolerante a errores, pero no pudo reasignar el área de error del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR en la recuperación de escritura de \_ ft \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-661">705 (0x2C1)</span><span class="sxs-lookup"><span data-stu-id="f32a5-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-662">{Escritura redundante} Para satisfacer una solicitud de escritura, el sistema de archivos tolerante a errores de NT escribió correctamente una copia redundante de la información.</span><span class="sxs-lookup"><span data-stu-id="f32a5-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="f32a5-663">Esto se ha hecho porque el sistema de archivos encontró un error en un miembro del volumen tolerante a errores, pero no pudo reasignar el área de error del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de tipo de máquina de imagen \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-665">706 (0x2C2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-666">{Error de coincidencia de tipo de máquina} El archivo de imagen% HS es válido, pero es para un tipo de máquina distinto del equipo actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="f32a5-667">Seleccione Aceptar para continuar o cancelar para que se produzca un error en la carga del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="f32a5-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR de \_ recepción \_ parcial**</span><span class="sxs-lookup"><span data-stu-id="f32a5-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-669">707 (0x2C3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-670">{Datos parciales recibidos} El transporte de red devolvió datos parciales a su cliente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="f32a5-671">Los datos restantes se enviarán más adelante.</span><span class="sxs-lookup"><span data-stu-id="f32a5-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR de \_ recepción \_ acelerada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-673">708 (0x2C4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-674">{Datos expedidos recibidos} El transporte de red devolvió datos a su cliente que se marcó como expedido por el sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR de \_ recepción \_ parcial \_ rápida**</span><span class="sxs-lookup"><span data-stu-id="f32a5-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-676">709 (0x2C5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-677">{Se recibieron datos inmediatos parciales} El transporte de red devolvió datos parciales a su cliente y estos datos se marcaron como expedidos por el sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="f32a5-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="f32a5-678">Los datos restantes se enviarán más adelante.</span><span class="sxs-lookup"><span data-stu-id="f32a5-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**evento de ERROR \_ \_ finalizado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-680">710 (0x2C6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-681">{Evento TDI terminado} La indicación TDI se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**evento de ERROR \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="f32a5-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-683">711 (0x2C7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-684">{Evento TDI pendiente} La indicación TDI ha entrado en el estado pendiente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR al \_ comprobar el \_ sistema de archivos \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-686">712 (0x2C8)</span><span class="sxs-lookup"><span data-stu-id="f32a5-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-687">Comprobando el sistema de archivos en% wZ.</span><span class="sxs-lookup"><span data-stu-id="f32a5-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR \_ irrecuperable de salida de la \_ aplicación \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-689">713 (0x2C9)</span><span class="sxs-lookup"><span data-stu-id="f32a5-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-690">{Final de aplicación irrecuperable}% HS.</span><span class="sxs-lookup"><span data-stu-id="f32a5-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_identificador PREdefinido de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-692">714 (0x2CA)</span><span class="sxs-lookup"><span data-stu-id="f32a5-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-693">Un identificador predefinido hace referencia a la clave del registro especificada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR \_ \_ desbloqueado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-695">715 (0x2CB)</span><span class="sxs-lookup"><span data-stu-id="f32a5-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-696">{Página desbloqueada} La protección de página de una página bloqueada se cambió a "sin acceso" y la página se desbloqueó de la memoria y del proceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notificación del servicio de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-698">716 (0x2CC)</span><span class="sxs-lookup"><span data-stu-id="f32a5-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-699">% HS</span><span class="sxs-lookup"><span data-stu-id="f32a5-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-701">717 (0x2CD)</span><span class="sxs-lookup"><span data-stu-id="f32a5-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-702">{Page Locked} Una de las páginas que se van a bloquear ya estaba bloqueada.</span><span class="sxs-lookup"><span data-stu-id="f32a5-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_error de registro de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-704">718 (0x2CE)</span><span class="sxs-lookup"><span data-stu-id="f32a5-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-705">Menú emergente de aplicación: %1: %2</span><span class="sxs-lookup"><span data-stu-id="f32a5-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR \_ ya \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="f32a5-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-707">719 (0x2CF)</span><span class="sxs-lookup"><span data-stu-id="f32a5-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-708">ERROR \_ ya \_ Win32</span><span class="sxs-lookup"><span data-stu-id="f32a5-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR \_ de \_ falta de \_ coincidencia de tipo de máquina de \_ imagen \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-710">720 (0x2D0)</span><span class="sxs-lookup"><span data-stu-id="f32a5-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-711">{Error de coincidencia de tipo de máquina} El archivo de imagen% HS es válido, pero es para un tipo de máquina distinto del equipo actual.</span><span class="sxs-lookup"><span data-stu-id="f32a5-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR: no se ha \_ \_ realizado ningún resultado \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-713">721 (0x2D1)</span><span class="sxs-lookup"><span data-stu-id="f32a5-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-714">Se ha realizado una ejecución de Yield y no hay ningún subproceso disponible para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="f32a5-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**se \_ ha \_ omitido el reanudación del temporizador \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-716">722 (0x2D2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-717">Se omitió la marca reanudable de una API de temporizador.</span><span class="sxs-lookup"><span data-stu-id="f32a5-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**Arbitraje de ERROR \_ \_ no controlado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-719">723 (0x2D3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-720">El árbitro ha diferido el arbitraje de estos recursos a su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="f32a5-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR \_ CardBus \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="f32a5-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-722">724 (0x2D4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-723">No se puede iniciar el dispositivo CardBus insertado debido a un error de configuración en "% HS".</span><span class="sxs-lookup"><span data-stu-id="f32a5-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR \_ de \_ incoherencia del procesador MP \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-725">725 (0x2D5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-726">Las CPU de este sistema multiprocesador no tienen el mismo nivel de revisión.</span><span class="sxs-lookup"><span data-stu-id="f32a5-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="f32a5-727">Para usar todos los procesadores, el sistema operativo se restringe a las características del procesador menos capaz en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="f32a5-728">En caso de que se produzcan problemas con este sistema, póngase en contacto con el fabricante de la CPU para ver si se admite esta combinación de procesadores.</span><span class="sxs-lookup"><span data-stu-id="f32a5-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR \_ hibernado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-730">726 (0x2D6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-731">El sistema se puso en hibernación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR al \_ reanudar la \_ hibernación**</span><span class="sxs-lookup"><span data-stu-id="f32a5-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-733">727 (0x2D7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-734">El sistema se reanudó de la hibernación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE de ERROR \_ \_ actualizado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-736">728 (0x2D8)</span><span class="sxs-lookup"><span data-stu-id="f32a5-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-737">Windows ha detectado que el firmware del sistema (BIOS) se actualizó en la \[ fecha de firmware anterior = %2, fecha de firmware actual %3 \] .</span><span class="sxs-lookup"><span data-stu-id="f32a5-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERRORES \_ en \_ \_ las páginas bloqueadas de los controladores de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-739">729 (0x2D9)</span><span class="sxs-lookup"><span data-stu-id="f32a5-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-740">Un controlador de dispositivo pierde las páginas de e/s bloqueadas que causan la degradación del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="f32a5-741">El sistema ha habilitado automáticamente el código de seguimiento para intentar detectar la causa.</span><span class="sxs-lookup"><span data-stu-id="f32a5-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR de \_ Wake \_ System**</span><span class="sxs-lookup"><span data-stu-id="f32a5-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-743">730 (0x2DA)</span><span class="sxs-lookup"><span data-stu-id="f32a5-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-744">El sistema tiene awoken.</span><span class="sxs-lookup"><span data-stu-id="f32a5-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR de \_ espera \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f32a5-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-746">731 (0x2DB)</span><span class="sxs-lookup"><span data-stu-id="f32a5-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-747">ERROR de \_ espera \_ 1</span><span class="sxs-lookup"><span data-stu-id="f32a5-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**Espera de ERROR \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f32a5-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-749">732 (0x2DC)</span><span class="sxs-lookup"><span data-stu-id="f32a5-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-750">Espera de ERROR \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="f32a5-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR de \_ espera \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f32a5-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-752">733 (0x2DD)</span><span class="sxs-lookup"><span data-stu-id="f32a5-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-753">ERROR de \_ espera \_ 3</span><span class="sxs-lookup"><span data-stu-id="f32a5-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR de \_ espera \_ 63**</span><span class="sxs-lookup"><span data-stu-id="f32a5-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-755">734 (0x2DE)</span><span class="sxs-lookup"><span data-stu-id="f32a5-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-756">ERROR de \_ espera \_ 63</span><span class="sxs-lookup"><span data-stu-id="f32a5-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR \_ abandonada \_ Wait \_ 0**</span><span class="sxs-lookup"><span data-stu-id="f32a5-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-758">735 (0x2DF)</span><span class="sxs-lookup"><span data-stu-id="f32a5-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-759">ERROR \_ abandonada \_ Wait \_ 0</span><span class="sxs-lookup"><span data-stu-id="f32a5-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR \_ abandonada \_ Wait \_ 63**</span><span class="sxs-lookup"><span data-stu-id="f32a5-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-761">736 (0x2E0)</span><span class="sxs-lookup"><span data-stu-id="f32a5-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-762">ERROR \_ abandonada \_ Wait \_ 63</span><span class="sxs-lookup"><span data-stu-id="f32a5-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR de \_ usuario \_ APC**</span><span class="sxs-lookup"><span data-stu-id="f32a5-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-764">737 (0x2E1)</span><span class="sxs-lookup"><span data-stu-id="f32a5-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-765">ERROR de \_ usuario \_ APC</span><span class="sxs-lookup"><span data-stu-id="f32a5-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR \_ de \_ APC kernel**</span><span class="sxs-lookup"><span data-stu-id="f32a5-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-767">738 (0x2E2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-768">ERROR \_ de \_ APC kernel</span><span class="sxs-lookup"><span data-stu-id="f32a5-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR de \_ alerta**</span><span class="sxs-lookup"><span data-stu-id="f32a5-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-770">739 (0x2E3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-771">ERROR de \_ alerta</span><span class="sxs-lookup"><span data-stu-id="f32a5-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**elevación de errores \_ \_ necesaria**</span><span class="sxs-lookup"><span data-stu-id="f32a5-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-773">740 (0x2E4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-774">La operación solicitada requiere elevación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR al volver a \_ analizar**</span><span class="sxs-lookup"><span data-stu-id="f32a5-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-776">741 (0x2E5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-777">El administrador de objetos debe realizar un reanálisis, ya que el nombre del archivo dio como resultado un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="f32a5-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**\_ \_ interrupción del error \_ de bloqueo oportunista en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="f32a5-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-779">742 (0x2E6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-780">Se completó una operación de apertura/creación mientras se está realizando una interrupción de bloqueo oportunista.</span><span class="sxs-lookup"><span data-stu-id="f32a5-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**volumen de ERROR \_ \_ montado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-782">743 (0x2E7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-783">Un sistema de archivos ha montado un nuevo volumen.</span><span class="sxs-lookup"><span data-stu-id="f32a5-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR \_ RXACT \_ confirmado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-785">744 (0x2E8)</span><span class="sxs-lookup"><span data-stu-id="f32a5-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-786">Este estado de nivel de éxito indica que el estado de la transacción ya existe para el subárbol del registro, pero que se anuló previamente una confirmación de transacción.</span><span class="sxs-lookup"><span data-stu-id="f32a5-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="f32a5-787">La confirmación se ha completado ahora.</span><span class="sxs-lookup"><span data-stu-id="f32a5-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR de \_ notificación de \_ limpieza**</span><span class="sxs-lookup"><span data-stu-id="f32a5-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-789">745 (0x2E9)</span><span class="sxs-lookup"><span data-stu-id="f32a5-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-790">Esto indica que se ha completado una solicitud NOTIFY Change debido al cierre del identificador que realizó la solicitud NOTIFY Change.</span><span class="sxs-lookup"><span data-stu-id="f32a5-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR \_ de \_ conexión de transporte principal \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-792">746 (0x2EA)</span><span class="sxs-lookup"><span data-stu-id="f32a5-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-793">{Error de conexión en el transporte principal} Se intentó conectar con el servidor remoto% HS en el transporte principal, pero se produjo un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="f32a5-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="f32a5-794">El equipo pudo conectarse en un transporte secundario.</span><span class="sxs-lookup"><span data-stu-id="f32a5-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transición de \_ errores de página de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-796">747 (0x2EB)</span><span class="sxs-lookup"><span data-stu-id="f32a5-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-797">El error de página era un error de transición.</span><span class="sxs-lookup"><span data-stu-id="f32a5-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**solicitud de ERROR de \_ página \_ \_ \_ cero**</span><span class="sxs-lookup"><span data-stu-id="f32a5-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-799">748 (0x2EC)</span><span class="sxs-lookup"><span data-stu-id="f32a5-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-800">El error de página era un error de petición cero.</span><span class="sxs-lookup"><span data-stu-id="f32a5-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR \_ \_ en la \_ copia \_ de errores de página al \_ escribir**</span><span class="sxs-lookup"><span data-stu-id="f32a5-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-802">749 (0x2ED)</span><span class="sxs-lookup"><span data-stu-id="f32a5-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-803">El error de página era un error de petición cero.</span><span class="sxs-lookup"><span data-stu-id="f32a5-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**Página de ERROR: \_ \_ protección de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-805">750 (0x2EE)</span><span class="sxs-lookup"><span data-stu-id="f32a5-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-806">El error de página era un error de petición cero.</span><span class="sxs-lookup"><span data-stu-id="f32a5-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_archivo de \_ \_ paginación de errores de página \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-808">751 (0x2EF)</span><span class="sxs-lookup"><span data-stu-id="f32a5-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-809">El error de página se ha satisfecho mediante la lectura de un dispositivo de almacenamiento secundario.</span><span class="sxs-lookup"><span data-stu-id="f32a5-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**\_Página caché de errores \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-811">752 (0x2F0)</span><span class="sxs-lookup"><span data-stu-id="f32a5-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-812">La página en caché se bloqueó durante la operación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**volcado de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-814">753 (0x2F1)</span><span class="sxs-lookup"><span data-stu-id="f32a5-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-815">El volcado de memoria existe en el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**búfer de ERROR: \_ \_ todos \_ ceros**</span><span class="sxs-lookup"><span data-stu-id="f32a5-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-817">754 (0x2F2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-818">El búfer especificado contiene ceros.</span><span class="sxs-lookup"><span data-stu-id="f32a5-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR al volver a \_ analizar el \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="f32a5-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-820">755 (0x2F3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-821">El administrador de objetos debe realizar un reanálisis, ya que el nombre del archivo dio como resultado un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="f32a5-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**requisitos de recursos de ERROR \_ \_ \_ modificados**</span><span class="sxs-lookup"><span data-stu-id="f32a5-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-823">756 (0x2F4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-824">El dispositivo ha finalizado correctamente una detención de consulta y sus requisitos de recursos han cambiado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**traducción de errores \_ \_ completada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-826">757 (0x2F5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-827">El traductor ha traducido estos recursos al espacio global y no se deben realizar más traducciones.</span><span class="sxs-lookup"><span data-stu-id="f32a5-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**no \_ \_ se pudo \_ Finalizar nada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-829">758 (0x2F6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-830">Un proceso terminado no tiene ningún subproceso para finalizar.</span><span class="sxs-lookup"><span data-stu-id="f32a5-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**el \_ proceso \_ de error no está \_ en el \_ trabajo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-832">759 (0x2F7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-833">El proceso especificado no forma parte de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR \_ \_ de proceso en el \_ trabajo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-835">760 (0x2F8)</span><span class="sxs-lookup"><span data-stu-id="f32a5-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-836">El proceso especificado forma parte de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR \_ VOLSNAP \_ \_ preparado para hibernar**</span><span class="sxs-lookup"><span data-stu-id="f32a5-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-838">761 (0x2F9)</span><span class="sxs-lookup"><span data-stu-id="f32a5-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-839">{Servicio de instantáneas de volumen} El sistema ya está listo para la hibernación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR \_ FSFILTER \_ operación \_ completada \_ correctamente**</span><span class="sxs-lookup"><span data-stu-id="f32a5-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-841">762 (0x2FA)</span><span class="sxs-lookup"><span data-stu-id="f32a5-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-842">Un sistema de archivos o un controlador de filtro del sistema de archivos ha completado correctamente una operación de FsFilter.</span><span class="sxs-lookup"><span data-stu-id="f32a5-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**Vector de interrupción de ERROR \_ \_ \_ ya \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-844">763 (0x2FB)</span><span class="sxs-lookup"><span data-stu-id="f32a5-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-845">El vector de interrupción especificado ya estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**interrupción de ERROR \_ \_ todavía \_ conectada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-847">764 (0x2FC)</span><span class="sxs-lookup"><span data-stu-id="f32a5-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-848">El vector de interrupción especificado todavía está conectado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR \_ \_ de espera de \_ bloqueo oportunista**</span><span class="sxs-lookup"><span data-stu-id="f32a5-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-850">765 (0x2FD)</span><span class="sxs-lookup"><span data-stu-id="f32a5-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-851">Una operación está bloqueada a la espera de un bloqueo oportunista.</span><span class="sxs-lookup"><span data-stu-id="f32a5-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR \_ dbg \_ excepción \_ controlada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-853">766 (0x2FE)</span><span class="sxs-lookup"><span data-stu-id="f32a5-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-854">Excepción controlada por el depurador.</span><span class="sxs-lookup"><span data-stu-id="f32a5-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR \_ dbg \_ continue**</span><span class="sxs-lookup"><span data-stu-id="f32a5-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-856">767 (0x2FF)</span><span class="sxs-lookup"><span data-stu-id="f32a5-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-857">El depurador continuó.</span><span class="sxs-lookup"><span data-stu-id="f32a5-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_pila pop de devolución de llamada de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-859">768 (0x300)</span><span class="sxs-lookup"><span data-stu-id="f32a5-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-860">Se produjo una excepción en una devolución de llamada del modo de usuario y debe quitarse el marco de devolución de llamada del kernel.</span><span class="sxs-lookup"><span data-stu-id="f32a5-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**compresión de ERROR \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-862">769 (0x301)</span><span class="sxs-lookup"><span data-stu-id="f32a5-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-863">La compresión está deshabilitada para este volumen.</span><span class="sxs-lookup"><span data-stu-id="f32a5-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR \_ CANTFETCHBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="f32a5-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-865">770 (0x302)</span><span class="sxs-lookup"><span data-stu-id="f32a5-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-866">El proveedor de datos no puede recuperarse hacia atrás a través de un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="f32a5-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR \_ CANTSCROLLBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="f32a5-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-868">771 (0x303)</span><span class="sxs-lookup"><span data-stu-id="f32a5-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-869">El proveedor de datos no se puede desplazar hacia atrás a través de un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="f32a5-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR \_ ROWSNOTRELEASED**</span><span class="sxs-lookup"><span data-stu-id="f32a5-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-871">772 (0x304)</span><span class="sxs-lookup"><span data-stu-id="f32a5-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-872">El proveedor de datos requiere que se liberen los datos capturados anteriormente antes de solicitar más datos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR \_ de \_ marcas de descriptor de acceso incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-874">773 (0x305)</span><span class="sxs-lookup"><span data-stu-id="f32a5-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-875">El proveedor de datos no pudo interpretar las marcas establecidas para un enlace de columna en un descriptor de acceso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_errores \_ encontrados**</span><span class="sxs-lookup"><span data-stu-id="f32a5-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-877">774 (0x306)</span><span class="sxs-lookup"><span data-stu-id="f32a5-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-878">Se produjeron uno o más errores al procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f32a5-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="f32a5-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-880">775 (0x307)</span><span class="sxs-lookup"><span data-stu-id="f32a5-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-881">La implementación no es capaz de realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f32a5-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_solicitud \_ de error fuera \_ de \_ secuencia**</span><span class="sxs-lookup"><span data-stu-id="f32a5-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-883">776 (0x308)</span><span class="sxs-lookup"><span data-stu-id="f32a5-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-884">El cliente de un componente solicitó una operación que no es válida dado el estado de la instancia del componente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**error de \_ análisis de versión de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-886">777 (0x309)</span><span class="sxs-lookup"><span data-stu-id="f32a5-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-887">No se pudo analizar un número de versión.</span><span class="sxs-lookup"><span data-stu-id="f32a5-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR \_ BADSTARTPOSITION**</span><span class="sxs-lookup"><span data-stu-id="f32a5-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-889">778 (0x30A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-890">La posición inicial del iterador no es válida.</span><span class="sxs-lookup"><span data-stu-id="f32a5-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_hardware de memoria de error \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-892">779 (0x30B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-893">El hardware ha detectado un error de memoria incorregible.</span><span class="sxs-lookup"><span data-stu-id="f32a5-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR \_ al \_ reparar el disco \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-895">780 (0x30C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-896">La operación que se ha intentado requiere que se habilite la recuperación automática.</span><span class="sxs-lookup"><span data-stu-id="f32a5-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR \_ \_ de recurso insuficiente \_ para \_ \_ \_ \_ el tamaño de sección compartida especificado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-898">781 (0x30D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-899">El montón de escritorio encontró un error al asignar memoria de sesión.</span><span class="sxs-lookup"><span data-stu-id="f32a5-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="f32a5-900">Hay más información en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="f32a5-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**transición de sistema de errores \_ \_ POWERSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-902">782 (0x30E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-903">El estado de la alimentación del sistema está pasando de %2 a %3.</span><span class="sxs-lookup"><span data-stu-id="f32a5-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**\_ \_ \_ transición compleja del sistema de errores \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-905">783 (0x30F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-906">El estado de la alimentación del sistema está pasando de %2 a %3, pero puede escribir %4.</span><span class="sxs-lookup"><span data-stu-id="f32a5-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR \_ MCA \_ excepción**</span><span class="sxs-lookup"><span data-stu-id="f32a5-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-908">784 (0x310)</span><span class="sxs-lookup"><span data-stu-id="f32a5-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-909">Un subproceso se envía con excepción de MCA debido a la MCA.</span><span class="sxs-lookup"><span data-stu-id="f32a5-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR \_ \_ de auditoría \_ de acceso por \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="f32a5-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-911">785 (0x311)</span><span class="sxs-lookup"><span data-stu-id="f32a5-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-912">El acceso a %1 está supervisado por la regla de directiva %2.</span><span class="sxs-lookup"><span data-stu-id="f32a5-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR \_ \_ de acceso deshabilitado \_ sin \_ \_ interfaz de usuario más segura \_ por \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="f32a5-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-914">786 (0x312)</span><span class="sxs-lookup"><span data-stu-id="f32a5-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-915">La regla de directiva %2 ha restringido el acceso a %1.</span><span class="sxs-lookup"><span data-stu-id="f32a5-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR al \_ abandonar \_ hibernación**</span><span class="sxs-lookup"><span data-stu-id="f32a5-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-917">787 (0x313)</span><span class="sxs-lookup"><span data-stu-id="f32a5-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-918">Se ha invalidado un archivo de hibernación válido y debe abandonarse.</span><span class="sxs-lookup"><span data-stu-id="f32a5-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR \_ perdido \_ WRITEBEHIND de \_ red de datos \_ \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-920">788 (0x314)</span><span class="sxs-lookup"><span data-stu-id="f32a5-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-921">{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS; se han perdido los datos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="f32a5-922">Este error puede deberse a problemas de conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="f32a5-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="f32a5-923">Intente guardar este archivo en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**error \_ perdido \_ WRITEBEHIND \_ de \_ servidor de red de datos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-925">789 (0x315)</span><span class="sxs-lookup"><span data-stu-id="f32a5-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-926">{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS; se han perdido los datos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="f32a5-927">Este error fue devuelto por el servidor en el que existe el archivo.</span><span class="sxs-lookup"><span data-stu-id="f32a5-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="f32a5-928">Intente guardar este archivo en otra ubicación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**error \_ perdido error de \_ \_ \_ disco local de datos WRITEBEHIND \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-930">790 (0x316)</span><span class="sxs-lookup"><span data-stu-id="f32a5-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-931">{Error de escritura retrasada} Windows no pudo guardar todos los datos del archivo% HS; se han perdido los datos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="f32a5-932">Este error puede deberse a que se ha quitado el dispositivo o a que el medio está protegido contra escritura.</span><span class="sxs-lookup"><span data-stu-id="f32a5-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR en la \_ \_ tabla MCFG errónea \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-934">791 (0x317)</span><span class="sxs-lookup"><span data-stu-id="f32a5-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-935">Los recursos necesarios para este dispositivo entran en conflicto con la tabla MCFG.</span><span class="sxs-lookup"><span data-stu-id="f32a5-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR \_ al \_ reparar el disco \_ Redirigido**</span><span class="sxs-lookup"><span data-stu-id="f32a5-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-937">792 (0x318)</span><span class="sxs-lookup"><span data-stu-id="f32a5-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-938">No se pudo reparar el volumen mientras está en línea.</span><span class="sxs-lookup"><span data-stu-id="f32a5-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="f32a5-939">Programe la desconexión del volumen para que se pueda reparar.</span><span class="sxs-lookup"><span data-stu-id="f32a5-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR \_ de \_ reparación de disco \_ incorrecta**</span><span class="sxs-lookup"><span data-stu-id="f32a5-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-941">793 (0x319)</span><span class="sxs-lookup"><span data-stu-id="f32a5-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-942">La reparación del volumen no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR \_ de \_ Registro \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-944">794 (0x31A)</span><span class="sxs-lookup"><span data-stu-id="f32a5-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-945">Uno de los registros de daños del volumen está lleno.</span><span class="sxs-lookup"><span data-stu-id="f32a5-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="f32a5-946">No se registrarán más daños que puedan detectarse.</span><span class="sxs-lookup"><span data-stu-id="f32a5-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR \_ de \_ Registro \_ dañado dañado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-948">795 (0x31B)</span><span class="sxs-lookup"><span data-stu-id="f32a5-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-949">Uno de los registros de daños del volumen está dañado internamente y debe volver a crearse.</span><span class="sxs-lookup"><span data-stu-id="f32a5-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="f32a5-950">El volumen puede contener daños no detectados y se debe analizar.</span><span class="sxs-lookup"><span data-stu-id="f32a5-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR \_ de \_ registro dañado \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="f32a5-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-952">796 (0x31C)</span><span class="sxs-lookup"><span data-stu-id="f32a5-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-953">Uno de los registros de daños del volumen no está disponible para su funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="f32a5-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR \_ de \_ registro dañado \_ eliminado \_ completo**</span><span class="sxs-lookup"><span data-stu-id="f32a5-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-955">797 (0x31D)</span><span class="sxs-lookup"><span data-stu-id="f32a5-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-956">Se eliminó uno de los registros de daños del volumen al seguir teniendo registros dañados en ellos.</span><span class="sxs-lookup"><span data-stu-id="f32a5-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="f32a5-957">El volumen contiene daños detectados y debe analizarse.</span><span class="sxs-lookup"><span data-stu-id="f32a5-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR \_ de \_ Registro \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-959">798 (0x31E)</span><span class="sxs-lookup"><span data-stu-id="f32a5-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-960">CHKDSK borró uno de los registros de daños del volumen y ya no contiene daños reales.</span><span class="sxs-lookup"><span data-stu-id="f32a5-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR \_ de \_ nombre huérfano \_ agotado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-962">799 (0x31F)</span><span class="sxs-lookup"><span data-stu-id="f32a5-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-963">Existen archivos huérfanos en el volumen, pero no se pudieron recuperar porque no se pueden crear más nombres nuevos en el directorio de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="f32a5-964">Los archivos deben moverse desde el directorio de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR \_ de bloqueo oportunista \_ cambiado \_ a \_ nuevo \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="f32a5-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-966">800 (0x320)</span><span class="sxs-lookup"><span data-stu-id="f32a5-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-967">El bloqueo oportunista asociado a este identificador está asociado ahora a un identificador diferente.</span><span class="sxs-lookup"><span data-stu-id="f32a5-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR \_ no se puede \_ conceder el \_ \_ bloqueo oportunista solicitado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-969">801 (0x321)</span><span class="sxs-lookup"><span data-stu-id="f32a5-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-970">No se puede conceder un bloqueo oportunista del nivel solicitado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="f32a5-971">Puede haber disponible un bloqueo oportunista de un nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="f32a5-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR \_ no se puede \_ interrumpir el \_ bloqueo oportunista**</span><span class="sxs-lookup"><span data-stu-id="f32a5-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-973">802 (0x322)</span><span class="sxs-lookup"><span data-stu-id="f32a5-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-974">La operación no se completó correctamente porque haría que se interrumpiera un bloqueo oportunista.</span><span class="sxs-lookup"><span data-stu-id="f32a5-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="f32a5-975">El autor de la llamada ha solicitado que bloqueos oportunistas existente no se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="f32a5-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**\_identificador de bloqueo oportunista de error \_ \_ cerrado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-977">803 (0x323)</span><span class="sxs-lookup"><span data-stu-id="f32a5-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-978">Se ha cerrado el identificador con el que se asoció este bloqueo oportunista.</span><span class="sxs-lookup"><span data-stu-id="f32a5-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="f32a5-979">El bloqueo oportunista se ha interrumpido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR: \_ no hay ninguna \_ \_ condición ACE**</span><span class="sxs-lookup"><span data-stu-id="f32a5-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-981">804 (0x324)</span><span class="sxs-lookup"><span data-stu-id="f32a5-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-982">La entrada de control de acceso (ACE) especificada no contiene ninguna condición.</span><span class="sxs-lookup"><span data-stu-id="f32a5-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR de la \_ \_ condición ACE no válida \_**</span><span class="sxs-lookup"><span data-stu-id="f32a5-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-984">805 (0x325)</span><span class="sxs-lookup"><span data-stu-id="f32a5-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-985">La entrada de control de acceso (ACE) especificada contiene una condición no válida.</span><span class="sxs-lookup"><span data-stu-id="f32a5-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**identificador de archivo de ERROR \_ \_ \_ revocado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-987">806 (0x326)</span><span class="sxs-lookup"><span data-stu-id="f32a5-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-988">Se ha revocado el acceso al identificador de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_imagen \_ de error en \_ \_ base diferente**</span><span class="sxs-lookup"><span data-stu-id="f32a5-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-990">807 (0x327)</span><span class="sxs-lookup"><span data-stu-id="f32a5-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-991">Un archivo de imagen se asignó a una dirección diferente a la especificada en el archivo de imagen, pero las correcciones se seguirán realizando automáticamente en la imagen.</span><span class="sxs-lookup"><span data-stu-id="f32a5-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR \_ EA \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="f32a5-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-993">994 (0x3E2)</span><span class="sxs-lookup"><span data-stu-id="f32a5-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-994">Se denegó el acceso al atributo extendido.</span><span class="sxs-lookup"><span data-stu-id="f32a5-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**operación de ERROR \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="f32a5-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-996">995 (0x3E3)</span><span class="sxs-lookup"><span data-stu-id="f32a5-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-997">La operación de e/s se ha anulado debido a una salida de subproceso o una solicitud de aplicación.</span><span class="sxs-lookup"><span data-stu-id="f32a5-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**\_e/s de error \_ incompleta**</span><span class="sxs-lookup"><span data-stu-id="f32a5-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-999">996 (0x3E4)</span><span class="sxs-lookup"><span data-stu-id="f32a5-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-1000">El evento de e/s superpuesta no se encuentra en un estado señalado.</span><span class="sxs-lookup"><span data-stu-id="f32a5-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**\_e/s de errores \_ pendientes**</span><span class="sxs-lookup"><span data-stu-id="f32a5-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-1002">997 (0x3E5)</span><span class="sxs-lookup"><span data-stu-id="f32a5-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-1003">La operación de e/s superpuesta está en curso.</span><span class="sxs-lookup"><span data-stu-id="f32a5-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR \_ NOaccess**</span><span class="sxs-lookup"><span data-stu-id="f32a5-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-1005">998 (0x3E6)</span><span class="sxs-lookup"><span data-stu-id="f32a5-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-1006">Acceso no válido a la ubicación de memoria.</span><span class="sxs-lookup"><span data-stu-id="f32a5-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f32a5-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR \_ SWAPERROR**</span><span class="sxs-lookup"><span data-stu-id="f32a5-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f32a5-1008">999 (0x3E7)</span><span class="sxs-lookup"><span data-stu-id="f32a5-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="f32a5-1009">Error al realizar la operación de INPAGE.</span><span class="sxs-lookup"><span data-stu-id="f32a5-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="f32a5-1010">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f32a5-1010">Requirements</span></span>



| <span data-ttu-id="f32a5-1011">Requisito</span><span class="sxs-lookup"><span data-stu-id="f32a5-1011">Requirement</span></span> | <span data-ttu-id="f32a5-1012">Value</span><span class="sxs-lookup"><span data-stu-id="f32a5-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f32a5-1013">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f32a5-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="f32a5-1014">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f32a5-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f32a5-1015">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f32a5-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="f32a5-1016">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f32a5-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f32a5-1017">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f32a5-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="f32a5-1018"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="f32a5-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f32a5-1019">Vea también</span><span class="sxs-lookup"><span data-stu-id="f32a5-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f32a5-1020">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="f32a5-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
