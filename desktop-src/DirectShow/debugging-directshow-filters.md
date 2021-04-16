---
description: Muchas de las funciones de depuración que se describen en este tema se implementan en la biblioteca de clases base de DirectShow. Para obtener más información, vea clases base de DirectShow.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: Depurar filtros de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1198e17f438d57775ea0f74d5920f63dc4761743
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538068"
---
# <a name="debugging-directshow-filters"></a><span data-ttu-id="64867-104">Depurar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="64867-104">Debugging DirectShow Filters</span></span>

<span data-ttu-id="64867-105">Muchas de las funciones de depuración que se describen en este tema se implementan en la biblioteca de clases base de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="64867-105">Many of the debugging facilities described in this topic are implemented in the DirectShow base class library.</span></span> <span data-ttu-id="64867-106">Para obtener más información, vea [clases base de DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="64867-106">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="assertion-checking"></a><span data-ttu-id="64867-107">Comprobación de aserciones</span><span class="sxs-lookup"><span data-stu-id="64867-107">Assertion Checking</span></span>

<span data-ttu-id="64867-108">Usar la comprobación de aserción libremente.</span><span class="sxs-lookup"><span data-stu-id="64867-108">Use assertion checking liberally.</span></span> <span data-ttu-id="64867-109">Las aserciones pueden comprobar las suposiciones que se realizan en el código sobre las condiciones previas y posteriores.</span><span class="sxs-lookup"><span data-stu-id="64867-109">Assertions can verify assumptions that you make in your code about preconditions and postconditions.</span></span> <span data-ttu-id="64867-110">DirectShow proporciona varias macros de aserción.</span><span class="sxs-lookup"><span data-stu-id="64867-110">DirectShow provides several assertion macros.</span></span> <span data-ttu-id="64867-111">Para obtener más información, vea [macros Assert y Breakpoint](assert-and-breakpoint-macros.md).</span><span class="sxs-lookup"><span data-stu-id="64867-111">For more information, see [Assert and Breakpoint Macros](assert-and-breakpoint-macros.md).</span></span>

## <a name="object-names"></a><span data-ttu-id="64867-112">Nombres de objeto</span><span class="sxs-lookup"><span data-stu-id="64867-112">Object Names</span></span>

<span data-ttu-id="64867-113">En las compilaciones de depuración, hay una lista global de objetos que derivan de la clase [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="64867-113">In debug builds, there is a global list of objects that derive from the [**CBaseObject**](cbaseobject.md) class.</span></span> <span data-ttu-id="64867-114">A medida que se crean objetos, se agregan a la lista.</span><span class="sxs-lookup"><span data-stu-id="64867-114">As objects are created, they are added to the list.</span></span> <span data-ttu-id="64867-115">Cuando se destruyen, se quitan de la lista.</span><span class="sxs-lookup"><span data-stu-id="64867-115">When they are destroyed, they are removed from the list.</span></span> <span data-ttu-id="64867-116">Para mostrar una lista de esos objetos, llame a la función [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .</span><span class="sxs-lookup"><span data-stu-id="64867-116">To display a list of those objects, call the [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) function.</span></span>

<span data-ttu-id="64867-117">El método constructor para la clase base [**CBaseObject**](cbaseobject.md) (y la mayoría de las clases derivadas de ella) incluye un parámetro para el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="64867-117">The constructor method for the [**CBaseObject**](cbaseobject.md) base class—and most classes derived from it—includes a parameter for the name of the object.</span></span> <span data-ttu-id="64867-118">Asigne nombres únicos a sus objetos para identificarlos.</span><span class="sxs-lookup"><span data-stu-id="64867-118">Give your objects unique names to identify them.</span></span> <span data-ttu-id="64867-119">Use la macro [**Name**](name.md) al declarar el nombre, de modo que el nombre se asigne solo en las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="64867-119">Use the [**NAME**](name.md) macro when you declare the name, so that the name is allocated only in debug builds.</span></span> <span data-ttu-id="64867-120">En las compilaciones comerciales, el nombre se convierte en **null**.</span><span class="sxs-lookup"><span data-stu-id="64867-120">In retail builds, the name becomes **NULL**.</span></span>

## <a name="debug-logging"></a><span data-ttu-id="64867-121">Depurar registro</span><span class="sxs-lookup"><span data-stu-id="64867-121">Debug Logging</span></span>

<span data-ttu-id="64867-122">La función [**DbgLog**](dbglog.md) muestra los mensajes de depuración cuando se ejecuta el programa.</span><span class="sxs-lookup"><span data-stu-id="64867-122">The [**DbgLog**](dbglog.md) function displays debugging messages as your program executes.</span></span> <span data-ttu-id="64867-123">Utilice esta función para realizar un seguimiento de la ejecución de la aplicación o el filtro.</span><span class="sxs-lookup"><span data-stu-id="64867-123">Use this function to trace the execution of your application or filter.</span></span> <span data-ttu-id="64867-124">Puede registrar los códigos de retorno, los valores de las variables y cualquier otra información relevante.</span><span class="sxs-lookup"><span data-stu-id="64867-124">You can log return codes, the values of variables, and any other relevant information.</span></span>

<span data-ttu-id="64867-125">Cada mensaje de depuración tiene un tipo, como un registro de \_ seguimiento o \_ un error de registro, y un nivel de depuración, que indica la importancia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="64867-125">Every debug message has a type, such as LOG\_TRACE or LOG\_ERROR, and a debug level, which indicates the importance of the message.</span></span> <span data-ttu-id="64867-126">Los mensajes con niveles de depuración inferiores son más importantes que los de niveles superiores.</span><span class="sxs-lookup"><span data-stu-id="64867-126">Messages with lower debug levels are more important than those with higher levels.</span></span>

<span data-ttu-id="64867-127">En el ejemplo siguiente, un filtro hipotético desconecta un PIN de una matriz de clavijas.</span><span class="sxs-lookup"><span data-stu-id="64867-127">In the following example, a hypothetical filter disconnects a pin from an array of pins.</span></span> <span data-ttu-id="64867-128">Si el intento de desconexión se realiza correctamente, el filtro muestra un mensaje de seguimiento de registro \_ .</span><span class="sxs-lookup"><span data-stu-id="64867-128">If the disconnect attempt succeeds, the filter displays a LOG\_TRACE message.</span></span> <span data-ttu-id="64867-129">Si se produce un error en el intento, se muestra un mensaje de error de registro \_ :</span><span class="sxs-lookup"><span data-stu-id="64867-129">If the attempt fails, it displays a LOG\_ERROR message:</span></span>


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



<span data-ttu-id="64867-130">Al depurar, puede establecer el nivel de depuración para cada tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="64867-130">When you are debugging, you can set the debug level for each message type.</span></span> <span data-ttu-id="64867-131">Además, cada módulo (DLL o ejecutable) mantiene sus propios niveles de depuración.</span><span class="sxs-lookup"><span data-stu-id="64867-131">Also, each module (DLL or executable) maintains its own debugging levels.</span></span> <span data-ttu-id="64867-132">Si está probando un filtro, aumente los niveles de depuración para el archivo DLL que contiene el filtro.</span><span class="sxs-lookup"><span data-stu-id="64867-132">If you are testing a filter, raise the debug levels for the DLL that contains the filter.</span></span>

<span data-ttu-id="64867-133">Para obtener más información, vea [funciones de salida de depuración](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="64867-133">For more information, see [Debug Output Functions](debug-output-functions.md).</span></span>

## <a name="critical-sections"></a><span data-ttu-id="64867-134">Secciones críticas</span><span class="sxs-lookup"><span data-stu-id="64867-134">Critical Sections</span></span>

<span data-ttu-id="64867-135">Para facilitar el seguimiento de los interbloqueos, incluya aserciones que determinen si el código de llamada posee una sección crítica determinada.</span><span class="sxs-lookup"><span data-stu-id="64867-135">To make deadlocks easier to track, include assertions that determine whether the calling code owns a given critical section.</span></span> <span data-ttu-id="64867-136">Las funciones [**CritCheckIn**](critcheckin.md) y [**CritCheckOut**](critcheckout.md) indican si el subproceso que realiza la llamada es el propietario de una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="64867-136">The [**CritCheckIn**](critcheckin.md) and [**CritCheckOut**](critcheckout.md) functions indicate whether the calling thread owns a critical section.</span></span> <span data-ttu-id="64867-137">Normalmente, se llamaría a estas funciones desde una macro Assert.</span><span class="sxs-lookup"><span data-stu-id="64867-137">Typically, you would call these functions from inside an assert macro.</span></span>

<span data-ttu-id="64867-138">También puede usar la función [**DbgLockTrace**](dbglocktrace.md) para realizar un seguimiento cuando se mantienen o liberan secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="64867-138">You can also use the [**DbgLockTrace**](dbglocktrace.md) function to trace when critical sections are held or released.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64867-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64867-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64867-140">Depurar en DirectShow</span><span class="sxs-lookup"><span data-stu-id="64867-140">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



