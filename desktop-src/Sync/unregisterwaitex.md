---
description: Cancela una operación de espera registrada emitida por la función RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Función UnregisterWaitEx (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910022"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="0da5e-103">UnregisterWaitEx función)</span><span class="sxs-lookup"><span data-stu-id="0da5e-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="0da5e-104">Cancela una operación de espera registrada emitida por la función [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="0da5e-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0da5e-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="0da5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0da5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da5e-107">*WaitHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0da5e-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5e-108">Identificador de espera.</span><span class="sxs-lookup"><span data-stu-id="0da5e-108">The wait handle.</span></span> <span data-ttu-id="0da5e-109">Este identificador es devuelto por la función [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="0da5e-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="0da5e-110">*CompletionEvent* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0da5e-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0da5e-111">Identificador del objeto de evento que se va a señalar cuando se haya anulado el registro de la operación de espera.</span><span class="sxs-lookup"><span data-stu-id="0da5e-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="0da5e-112">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0da5e-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="0da5e-113">Si este parámetro es **un \_ \_ valor de identificador no válido**, la función espera a que todas las funciones de devolución de llamada se completen antes de devolver.</span><span class="sxs-lookup"><span data-stu-id="0da5e-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="0da5e-114">Si este parámetro es **null**, la función marca el temporizador para su eliminación y vuelve inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0da5e-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="0da5e-115">Sin embargo, la mayoría de los llamadores deben esperar a que se complete la función de devolución de llamada para que puedan realizar cualquier limpieza necesaria.</span><span class="sxs-lookup"><span data-stu-id="0da5e-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="0da5e-116">Si el autor de la llamada proporciona este evento y la función se ejecuta correctamente, o si se produce un error en la función de **\_ e/s \_ pendiente**, no cierre el evento hasta que se señale.</span><span class="sxs-lookup"><span data-stu-id="0da5e-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da5e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0da5e-117">Return value</span></span>

<span data-ttu-id="0da5e-118">Si la función se realiza correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="0da5e-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="0da5e-119">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="0da5e-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="0da5e-120">Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0da5e-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="0da5e-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0da5e-121">Remarks</span></span>

<span data-ttu-id="0da5e-122">No se puede hacer una llamada de bloqueo a **UnregisterWaitEx** desde una función de devolución de llamada para la misma operación de espera.</span><span class="sxs-lookup"><span data-stu-id="0da5e-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="0da5e-123">De lo contrario, la devolución de llamada estará esperando a que finalice.</span><span class="sxs-lookup"><span data-stu-id="0da5e-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="0da5e-124">En general, una llamada de bloqueo a **UnregisterWaitEx** crea una dependencia entre el subproceso actual y la devolución de llamada, por lo que para realizar una llamada de bloqueo de anulación de registro en otra operación de espera, debe asegurarse de que las funciones de devolución de llamada no dependen entre sí y que la segunda operación de espera no realiza también una llamada de anulación de registro en la primera operación.</span><span class="sxs-lookup"><span data-stu-id="0da5e-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="0da5e-125">Tenga cuidado al realizar una llamada de bloqueo de **UnregisterWaitEx** en un subproceso persistente.</span><span class="sxs-lookup"><span data-stu-id="0da5e-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="0da5e-126">Si la operación de espera que se va a eliminar del registro se creó con **WT \_ EXECUTEINPERSISTENTTHREAD**, puede producirse un interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="0da5e-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="0da5e-127">Después de realizar una llamada de no bloqueo a **UnregisterWaitEx**, no se pueden poner en cola las nuevas funciones de devolución de llamada asociadas a *WaitHandle* .</span><span class="sxs-lookup"><span data-stu-id="0da5e-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="0da5e-128">Sin embargo, puede haber funciones de devolución de llamada pendientes que ya estén en la cola de subprocesos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="0da5e-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="0da5e-129">En algunas condiciones, la función generará un **error de \_ e/s \_ pendiente** si *CompletionEvent* es **null**.</span><span class="sxs-lookup"><span data-stu-id="0da5e-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="0da5e-130">Esto indica que hay funciones de devolución de llamada pendientes.</span><span class="sxs-lookup"><span data-stu-id="0da5e-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="0da5e-131">Esas devoluciones de llamada se ejecutarán o estarán en medio de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="0da5e-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="0da5e-132">Si *CompletionEvent* es un identificador de un evento proporcionado por el autor de la llamada, es posible que la función se ejecute correctamente, se produzca un **error de \_ e/s \_ pendiente** o se produzca un error con un código de error diferente.</span><span class="sxs-lookup"><span data-stu-id="0da5e-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="0da5e-133">Si la función se ejecuta correctamente, o si se produce un error en la función de **\_ e/s \_ pendiente**, el llamador siempre debe esperar hasta que se señale el evento para cerrar el evento.</span><span class="sxs-lookup"><span data-stu-id="0da5e-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="0da5e-134">Si se produce un error en la función con un código de error diferente, no es necesario esperar hasta que se señale el evento para cerrar el evento.</span><span class="sxs-lookup"><span data-stu-id="0da5e-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="0da5e-135">**Windows XP:** Si *CompletionEvent* es un identificador de un evento proporcionado por el autor de la llamada y se produce un error en la función de **\_ e/s \_ pendiente**, el llamador debe esperar hasta que se señale el evento para cerrar el evento.</span><span class="sxs-lookup"><span data-stu-id="0da5e-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="0da5e-136">Este comportamiento ha cambiado a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0da5e-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="0da5e-137">Para compilar una aplicación que usa esta función, defina **\_ Win32 \_ WinNT** como 0x0500 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0da5e-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="0da5e-138">Para obtener más información, consulte [uso de los encabezados de Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="0da5e-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0da5e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0da5e-139">Requirements</span></span>



| <span data-ttu-id="0da5e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0da5e-140">Requirement</span></span> | <span data-ttu-id="0da5e-141">Value</span><span class="sxs-lookup"><span data-stu-id="0da5e-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0da5e-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0da5e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0da5e-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0da5e-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0da5e-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0da5e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0da5e-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0da5e-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="0da5e-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0da5e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="0da5e-147"><dt>Threadpoollegacyapiset. h en Windows 8 y Windows Server 2012 (incluido Windows. h); </dt> <dt>Winbase. h en Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP y Windows server 2003 (incluido Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0da5e-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0da5e-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0da5e-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="0da5e-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0da5e-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="0da5e-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0da5e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0da5e-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0da5e-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="0da5e-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="0da5e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da5e-153">**RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="0da5e-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="0da5e-154">Funciones de sincronización</span><span class="sxs-lookup"><span data-stu-id="0da5e-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="0da5e-155">Agrupación de subprocesos</span><span class="sxs-lookup"><span data-stu-id="0da5e-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
