---
description: Las siguientes funciones se usan en el control de excepciones estructurado.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funciones de control de excepciones estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659455"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="28a53-103">Funciones de control de excepciones estructurado</span><span class="sxs-lookup"><span data-stu-id="28a53-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="28a53-104">Las siguientes funciones se usan en el control de excepciones estructurado.</span><span class="sxs-lookup"><span data-stu-id="28a53-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="28a53-105">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="28a53-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="28a53-106">Indica si el bloque **\_ \_ try** de un controlador de terminación terminó normalmente.</span><span class="sxs-lookup"><span data-stu-id="28a53-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="28a53-107">**AddVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="28a53-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="28a53-108">Registra un controlador de continuación de vectores.</span><span class="sxs-lookup"><span data-stu-id="28a53-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="28a53-109">**AddVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="28a53-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="28a53-110">Registra un controlador de excepciones vectorizado.</span><span class="sxs-lookup"><span data-stu-id="28a53-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="28a53-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="28a53-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="28a53-112">Recupera un código que identifica el tipo de excepción que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="28a53-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="28a53-113">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="28a53-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="28a53-114">Recupera una descripción independiente de la máquina de una excepción e información sobre el estado del equipo que existía para el subproceso cuando se produjo la excepción.</span><span class="sxs-lookup"><span data-stu-id="28a53-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="28a53-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="28a53-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="28a53-116">Genera una excepción en el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="28a53-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="28a53-117">**RemoveVectoredContinueHandler**</span><span class="sxs-lookup"><span data-stu-id="28a53-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="28a53-118">Anula el registro de un controlador de continuación vectorizado.</span><span class="sxs-lookup"><span data-stu-id="28a53-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="28a53-119">**RemoveVectoredExceptionHandler**</span><span class="sxs-lookup"><span data-stu-id="28a53-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="28a53-120">Anula el registro de un controlador de excepciones vectorizado.</span><span class="sxs-lookup"><span data-stu-id="28a53-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="28a53-121">**RtlAddGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="28a53-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="28a53-122">Informa al sistema de una tabla de funciones dinámicas que representa una región de memoria que contiene código.</span><span class="sxs-lookup"><span data-stu-id="28a53-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="28a53-123">**RtlDeleteGrowableFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="28a53-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="28a53-124">Informa al sistema de que una tabla de funciones dinámicas notificada previamente ya no está en uso.</span><span class="sxs-lookup"><span data-stu-id="28a53-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="28a53-125">**RtlGrowFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="28a53-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="28a53-126">Informa de que una tabla de funciones dinámicas ha aumentado de tamaño.</span><span class="sxs-lookup"><span data-stu-id="28a53-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="28a53-127">**SetUnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="28a53-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="28a53-128">Permite a una aplicación sustituir el controlador de excepciones de nivel superior de cada subproceso y proceso.</span><span class="sxs-lookup"><span data-stu-id="28a53-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="28a53-129">**UnhandledExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="28a53-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="28a53-130">Pasa las excepciones no controladas al depurador, si se está depurando el proceso.</span><span class="sxs-lookup"><span data-stu-id="28a53-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="28a53-131">**VectoredHandler**</span><span class="sxs-lookup"><span data-stu-id="28a53-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="28a53-132">Función definida por la aplicación que actúa como controlador de excepciones vectorizadas.</span><span class="sxs-lookup"><span data-stu-id="28a53-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="28a53-133">Las siguientes funciones solo se usan en Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="28a53-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="28a53-134">**RtlAddFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="28a53-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="28a53-135">Agrega una tabla de funciones dinámicas a la lista de tablas de funciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="28a53-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="28a53-136">**RtlCaptureContext**</span><span class="sxs-lookup"><span data-stu-id="28a53-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="28a53-137">Recupera un registro de contexto en el contexto del llamador.</span><span class="sxs-lookup"><span data-stu-id="28a53-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="28a53-138">**RtlDeleteFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="28a53-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="28a53-139">Quita una tabla de funciones dinámicas de la lista de tablas de funciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="28a53-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="28a53-140">**RtlInstallFunctionTableCallback**</span><span class="sxs-lookup"><span data-stu-id="28a53-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="28a53-141">Agrega una tabla de funciones dinámicas a la lista de tablas de funciones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="28a53-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="28a53-142">**RtlRestoreContext**</span><span class="sxs-lookup"><span data-stu-id="28a53-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="28a53-143">Restaura el contexto del llamador en el registro de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="28a53-143">Restores the context of the caller to the specified context record.</span></span>

 

 
