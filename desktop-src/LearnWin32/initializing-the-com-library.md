---
title: Inicializar la biblioteca COM
description: Inicializar la biblioteca COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676378"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="810b5-103">Inicializar la biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="810b5-103">Initializing the COM Library</span></span>

<span data-ttu-id="810b5-104">Cualquier programa de Windows que use COM debe inicializar la biblioteca COM mediante una llamada a la función [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="810b5-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="810b5-105">Cada subproceso que usa una interfaz COM debe hacer una llamada independiente a esta función.</span><span class="sxs-lookup"><span data-stu-id="810b5-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="810b5-106">**CoInitializeEx** tiene la firma siguiente:</span><span class="sxs-lookup"><span data-stu-id="810b5-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="810b5-107">El primer parámetro está reservado y debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="810b5-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="810b5-108">El segundo parámetro especifica el modelo de subprocesos que utilizará el programa.</span><span class="sxs-lookup"><span data-stu-id="810b5-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="810b5-109">COM admite dos modelos de subprocesos diferentes, *Apartamento* y *multiproceso*.</span><span class="sxs-lookup"><span data-stu-id="810b5-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="810b5-110">Si especifica el subprocesamiento de apartamento, está realizando las siguientes garantías:</span><span class="sxs-lookup"><span data-stu-id="810b5-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="810b5-111">Tendrá acceso a cada objeto COM desde un único subproceso; no se compartirán punteros de interfaz COM entre varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="810b5-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="810b5-112">El subproceso tendrá un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="810b5-112">The thread will have a message loop.</span></span> <span data-ttu-id="810b5-113">(Consulte [mensajes de ventana](window-messages.md) en el módulo 1).</span><span class="sxs-lookup"><span data-stu-id="810b5-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="810b5-114">Si alguna de estas restricciones no es true, utilice el modelo multiproceso.</span><span class="sxs-lookup"><span data-stu-id="810b5-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="810b5-115">Para especificar el modelo de subprocesos, establezca una de las marcas siguientes en el parámetro *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="810b5-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="810b5-116">Marca</span><span class="sxs-lookup"><span data-stu-id="810b5-116">Flag</span></span>                          | <span data-ttu-id="810b5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="810b5-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="810b5-118">**APARTMENTTHREADED de coinit \_**</span><span class="sxs-lookup"><span data-stu-id="810b5-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="810b5-119">Subproceso de apartamento.</span><span class="sxs-lookup"><span data-stu-id="810b5-119">Apartment threaded.</span></span> |
| <span data-ttu-id="810b5-120">**multiproceso de coinit \_**</span><span class="sxs-lookup"><span data-stu-id="810b5-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="810b5-121">Multiproceso.</span><span class="sxs-lookup"><span data-stu-id="810b5-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="810b5-122">Debe establecer exactamente una de estas marcas.</span><span class="sxs-lookup"><span data-stu-id="810b5-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="810b5-123">Normalmente, un subproceso que crea una ventana debe usar la marca **\_ APARTMENTTHREADED de coinit** y otros subprocesos deben usar **coinit \_ multithreaded**.</span><span class="sxs-lookup"><span data-stu-id="810b5-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="810b5-124">Sin embargo, algunos componentes COM requieren un modelo de subprocesos determinado.</span><span class="sxs-lookup"><span data-stu-id="810b5-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="810b5-125">La documentación de MSDN le indicará cuándo es así.</span><span class="sxs-lookup"><span data-stu-id="810b5-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="810b5-126">En realidad, incluso si se especifica el subprocesamiento de apartamento, todavía es posible compartir interfaces entre subprocesos mediante una técnica denominada *serialización*.</span><span class="sxs-lookup"><span data-stu-id="810b5-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="810b5-127">El cálculo de referencias está fuera del ámbito de este módulo.</span><span class="sxs-lookup"><span data-stu-id="810b5-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="810b5-128">Lo importante es que con el subprocesamiento de apartamento, nunca debe copiar simplemente un puntero de interfaz a otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="810b5-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="810b5-129">Para obtener más información sobre los modelos de subprocesos COM, consulte [procesos, subprocesos y apartamentos](/windows/desktop/com/processes--threads--and-apartments).</span><span class="sxs-lookup"><span data-stu-id="810b5-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="810b5-130">Además de las marcas ya mencionadas, es una buena idea establecer la marca de **\_ \_ OLE1DDE deshabilitar coinit** en el parámetro *dwCoInit* .</span><span class="sxs-lookup"><span data-stu-id="810b5-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="810b5-131">La configuración de esta marca evita la sobrecarga asociada con la vinculación e incrustación de objetos (OLE) 1,0, una tecnología obsoleta.</span><span class="sxs-lookup"><span data-stu-id="810b5-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="810b5-132">Aquí se muestra cómo inicializar COM para el subprocesamiento de apartamento:</span><span class="sxs-lookup"><span data-stu-id="810b5-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="810b5-133">El tipo de valor devuelto **HRESULT** contiene un error o código de operación correcta.</span><span class="sxs-lookup"><span data-stu-id="810b5-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="810b5-134">Veremos el control de errores COM en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="810b5-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="810b5-135">Anular la inicialización de la biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="810b5-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="810b5-136">Para cada llamada correcta a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), debe llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) antes de que se cierre el subproceso.</span><span class="sxs-lookup"><span data-stu-id="810b5-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="810b5-137">Esta función no toma ningún parámetro y no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="810b5-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="810b5-138">Siguientes</span><span class="sxs-lookup"><span data-stu-id="810b5-138">Next</span></span>

[<span data-ttu-id="810b5-139">Códigos de error en COM</span><span class="sxs-lookup"><span data-stu-id="810b5-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 