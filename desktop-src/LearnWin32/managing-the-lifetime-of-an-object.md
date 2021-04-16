---
title: Administrar la duración de un objeto
description: Obtenga información sobre cómo administrar los métodos AddRef y RELEASE para controlar la duración de un objeto.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104557141"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="d8185-103">Administrar la duración de un objeto</span><span class="sxs-lookup"><span data-stu-id="d8185-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="d8185-104">Hay una regla para las interfaces COM que todavía no hemos mencionado.</span><span class="sxs-lookup"><span data-stu-id="d8185-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="d8185-105">Cada interfaz COM debe heredar, directa o indirectamente, de una interfaz denominada [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="d8185-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="d8185-106">Esta interfaz proporciona algunas funciones de línea base que todos los objetos COM deben admitir.</span><span class="sxs-lookup"><span data-stu-id="d8185-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="d8185-107">La interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) define tres métodos:</span><span class="sxs-lookup"><span data-stu-id="d8185-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="d8185-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="d8185-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="d8185-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="d8185-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="d8185-110">**Release**</span><span class="sxs-lookup"><span data-stu-id="d8185-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="d8185-111">El método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) permite a un programa consultar las capacidades del objeto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d8185-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="d8185-112">En el tema siguiente se indicará más sobre eso, [donde se pide un objeto para una interfaz](asking-an-object-for-an-interface.md).</span><span class="sxs-lookup"><span data-stu-id="d8185-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="d8185-113">Los métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) se utilizan para controlar la duración de un objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="d8185-114">Este es el asunto de este tema.</span><span class="sxs-lookup"><span data-stu-id="d8185-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="d8185-115">Recuento de referencias</span><span class="sxs-lookup"><span data-stu-id="d8185-115">Reference Counting</span></span>

<span data-ttu-id="d8185-116">Lo que pueda hacer un programa, en algún momento se asignarán y liberarán recursos.</span><span class="sxs-lookup"><span data-stu-id="d8185-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="d8185-117">Es fácil asignar un recurso.</span><span class="sxs-lookup"><span data-stu-id="d8185-117">Allocating a resource is easy.</span></span> <span data-ttu-id="d8185-118">Saber cuándo liberar el recurso es difícil, especialmente si la duración del recurso se extiende más allá del ámbito actual.</span><span class="sxs-lookup"><span data-stu-id="d8185-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="d8185-119">Este problema no es único para COM.</span><span class="sxs-lookup"><span data-stu-id="d8185-119">This problem is not unique to COM.</span></span> <span data-ttu-id="d8185-120">Cualquier programa que asigne memoria del montón debe resolver el mismo problema.</span><span class="sxs-lookup"><span data-stu-id="d8185-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="d8185-121">Por ejemplo, C++ usa destructores automáticos, mientras que C# y Java usan la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="d8185-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="d8185-122">COM utiliza un enfoque denominado *recuento de referencias*.</span><span class="sxs-lookup"><span data-stu-id="d8185-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="d8185-123">Cada objeto COM mantiene un recuento interno.</span><span class="sxs-lookup"><span data-stu-id="d8185-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="d8185-124">Esto se conoce como recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d8185-124">This is known as the reference count.</span></span> <span data-ttu-id="d8185-125">El recuento de referencias realiza un seguimiento del número de referencias al objeto que están activas actualmente.</span><span class="sxs-lookup"><span data-stu-id="d8185-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="d8185-126">Cuando el número de referencias cae a cero, el objeto se elimina a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d8185-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="d8185-127">Merece la pena repetir la última parte: el objeto se elimina a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d8185-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="d8185-128">El programa no elimina nunca explícitamente el objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="d8185-129">Estas son las reglas para el recuento de referencias:</span><span class="sxs-lookup"><span data-stu-id="d8185-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="d8185-130">Cuando el objeto se crea por primera vez, su recuento de referencias es 1.</span><span class="sxs-lookup"><span data-stu-id="d8185-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="d8185-131">En este punto, el programa tiene un único puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="d8185-132">El programa puede crear una nueva referencia duplicando (copiando) el puntero.</span><span class="sxs-lookup"><span data-stu-id="d8185-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="d8185-133">Al copiar el puntero, debe llamar al método [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="d8185-134">Este método incrementa el recuento de referencias en uno.</span><span class="sxs-lookup"><span data-stu-id="d8185-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="d8185-135">Cuando haya terminado de usar un puntero al objeto, debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d8185-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d8185-136">El método **Release** reduce el recuento de referencias en uno.</span><span class="sxs-lookup"><span data-stu-id="d8185-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="d8185-137">También invalida el puntero.</span><span class="sxs-lookup"><span data-stu-id="d8185-137">It also invalidates the pointer.</span></span> <span data-ttu-id="d8185-138">No vuelva a usar el puntero después de llamar a **Release**.</span><span class="sxs-lookup"><span data-stu-id="d8185-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="d8185-139">(Si tiene otros punteros al mismo objeto, puede seguir usando esos punteros).</span><span class="sxs-lookup"><span data-stu-id="d8185-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="d8185-140">Cuando se ha llamado a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) con cada puntero, el recuento de referencias de objeto del objeto alcanza el valor cero y el objeto se elimina a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d8185-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="d8185-141">En el diagrama siguiente se muestra un caso sencillo pero típico.</span><span class="sxs-lookup"><span data-stu-id="d8185-141">The following diagram shows a simple but typical case.</span></span>

![Diagrama que muestra un caso simple de recuento de referencias.](images/com04.png)

<span data-ttu-id="d8185-143">El programa crea un objeto y almacena un puntero (*p*) en el objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="d8185-144">En este punto, el recuento de referencias es 1.</span><span class="sxs-lookup"><span data-stu-id="d8185-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="d8185-145">Cuando el programa termina de usar el puntero, llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d8185-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d8185-146">El recuento de referencias se reduce a cero y el objeto se elimina a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d8185-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="d8185-147">Ahora *p* no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8185-147">Now *p* is invalid.</span></span> <span data-ttu-id="d8185-148">Es un error usar *p* para otras llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="d8185-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="d8185-149">En el diagrama siguiente se muestra un ejemplo más complejo.</span><span class="sxs-lookup"><span data-stu-id="d8185-149">The next diagram shows a more complex example.</span></span>

![Ilustración que muestra el recuento de referencias](images/com05.png)

<span data-ttu-id="d8185-151">En este caso, el programa crea un objeto y almacena el puntero *p*, como antes.</span><span class="sxs-lookup"><span data-stu-id="d8185-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="d8185-152">Después, el programa copia *p* en una nueva variable, *q*.</span><span class="sxs-lookup"><span data-stu-id="d8185-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="d8185-153">En este momento, el programa debe llamar a [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d8185-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="d8185-154">Ahora, el recuento de referencias es 2 y hay dos punteros válidos al objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="d8185-155">Ahora Supongamos que el programa ha terminado de usar *p*.</span><span class="sxs-lookup"><span data-stu-id="d8185-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="d8185-156">El programa llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), el recuento de referencias va a 1 y *p* ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8185-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="d8185-157">Sin embargo, *q* sigue siendo válido.</span><span class="sxs-lookup"><span data-stu-id="d8185-157">However, *q* is still valid.</span></span> <span data-ttu-id="d8185-158">Más adelante, el programa termina de usar *q*.</span><span class="sxs-lookup"><span data-stu-id="d8185-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="d8185-159">Por lo tanto, vuelve a llamar a **Release** .</span><span class="sxs-lookup"><span data-stu-id="d8185-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="d8185-160">El recuento de referencias llega a cero y el objeto se elimina a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d8185-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="d8185-161">Es posible que se pregunte por qué el programa copiará *p*.</span><span class="sxs-lookup"><span data-stu-id="d8185-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="d8185-162">Hay dos razones principales: en primer lugar, puede que desee almacenar el puntero en una estructura de datos, como una lista.</span><span class="sxs-lookup"><span data-stu-id="d8185-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="d8185-163">En segundo lugar, puede que desee mantener el puntero más allá del ámbito actual de la variable original.</span><span class="sxs-lookup"><span data-stu-id="d8185-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="d8185-164">Por lo tanto, se copiará en una nueva variable con un ámbito más amplio.</span><span class="sxs-lookup"><span data-stu-id="d8185-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="d8185-165">Una ventaja del recuento de referencias es que puede compartir punteros en diferentes secciones de código, sin las distintas rutas de acceso de código que se coordinan para eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="d8185-166">En su lugar, cada ruta de acceso de código simplemente llama a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando la ruta de acceso del código se realiza mediante el objeto.</span><span class="sxs-lookup"><span data-stu-id="d8185-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="d8185-167">El objeto controla la eliminación en el momento correcto.</span><span class="sxs-lookup"><span data-stu-id="d8185-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="d8185-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8185-168">Example</span></span>

<span data-ttu-id="d8185-169">Este es el código del [ejemplo de cuadro de diálogo Abrir](example--the-open-dialog-box.md) de nuevo.</span><span class="sxs-lookup"><span data-stu-id="d8185-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="d8185-170">El recuento de referencias se produce en dos lugares en este código.</span><span class="sxs-lookup"><span data-stu-id="d8185-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="d8185-171">En primer lugar, si el programa crea correctamente el objeto de cuadro de diálogo de elementos comunes, debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pFileOpen* .</span><span class="sxs-lookup"><span data-stu-id="d8185-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="d8185-172">En segundo lugar, cuando el método [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) devuelve un puntero a la interfaz [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) , el programa debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en el puntero *pItem* .</span><span class="sxs-lookup"><span data-stu-id="d8185-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="d8185-173">Observe que, en ambos casos, la llamada de [**versión**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) es lo último que ocurre antes de que el puntero salga del ámbito.</span><span class="sxs-lookup"><span data-stu-id="d8185-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="d8185-174">Observe también que solo se llama a **Release** después de probar el **valor de HRESULT** para ver si se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8185-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="d8185-175">Por ejemplo, si se produce un error en la llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , el puntero *pFileOpen* no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8185-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="d8185-176">Por lo tanto, sería un error llamar a **Release** en el puntero.</span><span class="sxs-lookup"><span data-stu-id="d8185-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="d8185-177">Siguientes</span><span class="sxs-lookup"><span data-stu-id="d8185-177">Next</span></span>

[<span data-ttu-id="d8185-178">Solicitar un objeto para una interfaz</span><span class="sxs-lookup"><span data-stu-id="d8185-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)