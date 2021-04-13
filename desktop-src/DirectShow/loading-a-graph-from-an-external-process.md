---
description: Cargar un grafo desde un proceso externo
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Cargar un grafo desde un proceso externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564421"
---
# <a name="loading-a-graph-from-an-external-process"></a><span data-ttu-id="e4d70-103">Cargar un grafo desde un proceso externo</span><span class="sxs-lookup"><span data-stu-id="e4d70-103">Loading a Graph From an External Process</span></span>

<span data-ttu-id="e4d70-104">GraphEdit puede cargar un gráfico de filtro creado por un proceso externo.</span><span class="sxs-lookup"><span data-stu-id="e4d70-104">GraphEdit can load a filter graph created by an external process.</span></span> <span data-ttu-id="e4d70-105">Con esta característica, puede ver exactamente qué gráfico de filtro se compila en la aplicación, con solo una cantidad mínima de código adicional en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4d70-105">With this feature, you can see exactly what filter graph your application builds, with only a minimal amount of additional code in your application.</span></span>

> [!Note]  
> <span data-ttu-id="e4d70-106">Esta característica requiere Windows 2000, Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="e4d70-106">This feature requires Windows 2000, Windows XP, or later.</span></span>

 

> [!Note]  
> <span data-ttu-id="e4d70-107">A partir de Windows Vista, debe registrar proppage.dll para habilitar esta característica.</span><span class="sxs-lookup"><span data-stu-id="e4d70-107">Starting in Windows Vista, you must register proppage.dll to enable this feature.</span></span> <span data-ttu-id="e4d70-108">Proppage.dll se incluye en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e4d70-108">Proppage.dll is included in the Windows SDK.</span></span>

 

<span data-ttu-id="e4d70-109">La aplicación debe registrar la instancia del gráfico de filtro en la tabla de objetos en ejecución (ROT).</span><span class="sxs-lookup"><span data-stu-id="e4d70-109">The application must register the filter graph instance in the Running Object Table (ROT).</span></span> <span data-ttu-id="e4d70-110">La ROT es una tabla de búsqueda global accesible que realiza un seguimiento de los objetos en ejecución.</span><span class="sxs-lookup"><span data-stu-id="e4d70-110">The ROT is a globally accessible look-up table that keeps track of running objects.</span></span> <span data-ttu-id="e4d70-111">Los objetos se registran en la tabla ROT por moniker.</span><span class="sxs-lookup"><span data-stu-id="e4d70-111">Objects are registered in the ROT by moniker.</span></span> <span data-ttu-id="e4d70-112">Para conectarse al gráfico, GraphEdit busca en la ROT los monikers cuyo nombre para mostrar coincida con un formato determinado:</span><span class="sxs-lookup"><span data-stu-id="e4d70-112">To connect to the graph, GraphEdit searches the ROT for monikers whose display name matches a particular format:</span></span>


```C++
!FilterGraph X pid Y
```



<span data-ttu-id="e4d70-113">donde *X* es la dirección hexadecimal del administrador de gráficos de filtro e *y es el* identificador de proceso, también en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="e4d70-113">where *X* is the hexadecimal address of the Filter Graph Manager, and *Y* is the process id, also in hexadecimal.</span></span>

<span data-ttu-id="e4d70-114">Cuando la aplicación crea primero el gráfico de filtro, llame a la siguiente función:</span><span class="sxs-lookup"><span data-stu-id="e4d70-114">When your application first creates the filter graph, call the following function:</span></span>


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



<span data-ttu-id="e4d70-115">Esta función crea un moniker y una nueva entrada de tabla de texto para el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e4d70-115">This function creates a moniker and a new ROT entry for the filter graph.</span></span> <span data-ttu-id="e4d70-116">El primer parámetro es un puntero al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e4d70-116">The first parameter is a pointer to the filter graph.</span></span> <span data-ttu-id="e4d70-117">El segundo parámetro recibe un valor que identifica la nueva entrada de la tabla ROT.</span><span class="sxs-lookup"><span data-stu-id="e4d70-117">The second parameter receives a value that identifies the new ROT entry.</span></span> <span data-ttu-id="e4d70-118">Antes de que la aplicación libere el gráfico de filtros, llame a la función siguiente para quitar la entrada de la tabla ROT.</span><span class="sxs-lookup"><span data-stu-id="e4d70-118">Before the application releases the filter graph, call the following function to remove the ROT entry.</span></span> <span data-ttu-id="e4d70-119">El parámetro *pdwRegister* es el identificador devuelto por la función AddToRot.</span><span class="sxs-lookup"><span data-stu-id="e4d70-119">The *pdwRegister* parameter is the identifier returned by the AddToRot function.</span></span>


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



<span data-ttu-id="e4d70-120">En el ejemplo de código siguiente se muestra cómo llamar a estas funciones.</span><span class="sxs-lookup"><span data-stu-id="e4d70-120">The following code example shows how to call these functions.</span></span> <span data-ttu-id="e4d70-121">En este ejemplo, el código que agrega y quita entradas de la tabla ROT se compila condicionalmente, de modo que solo se incluye en las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="e4d70-121">In this example, the code that adds and removes ROT entries is conditionally compiled, so that it is included only in debug builds.</span></span>


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



<span data-ttu-id="e4d70-122">Para ver el gráfico de filtro en GraphEdit, ejecute la aplicación y GraphEdit al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e4d70-122">To view the filter graph in GraphEdit, run your application and GraphEdit at the same time.</span></span> <span data-ttu-id="e4d70-123">En el menú **archivo** GraphEdit, haga clic en **conectar a gráfico remoto...** En el cuadro de diálogo **conectar con el gráfico** , seleccione el ID. de proceso (PID) de la aplicación y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e4d70-123">In the GraphEdit **File** menu, click **Connect to Remote Graph...** In the **Connect To Graph** dialog box, select the process id (pid) of your application and click **OK**.</span></span> <span data-ttu-id="e4d70-124">GraphEdit carga el gráfico de filtro y lo muestra.</span><span class="sxs-lookup"><span data-stu-id="e4d70-124">GraphEdit loads the filter graph and displays it.</span></span> <span data-ttu-id="e4d70-125">No use otras características de GraphEdit en este grafo; podría producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="e4d70-125">Don't use any other GraphEdit features on this graph—it might cause unexpected results.</span></span> <span data-ttu-id="e4d70-126">Por ejemplo, no agregue ni quite filtros, o detenga e inicie el gráfico.</span><span class="sxs-lookup"><span data-stu-id="e4d70-126">For example, don't add or remove filters, or stop and start the graph.</span></span> <span data-ttu-id="e4d70-127">Cierre GraphEdit antes de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e4d70-127">Close GraphEdit before exiting your application.</span></span>

> [!Note]  
> <span data-ttu-id="e4d70-128">La aplicación podría alcanzar varias aserciones al salir.</span><span class="sxs-lookup"><span data-stu-id="e4d70-128">Your application might hit various asserts when it exits.</span></span> <span data-ttu-id="e4d70-129">Puede pasarlos por alto.</span><span class="sxs-lookup"><span data-stu-id="e4d70-129">You can ignore these.</span></span>

 

<span data-ttu-id="e4d70-130">En la ilustración siguiente se muestra el cuadro de diálogo **conectar con el gráfico** .</span><span class="sxs-lookup"><span data-stu-id="e4d70-130">The following illustration shows the **Connect To Graph** dialog box.</span></span>

![conectar al grafo](images/gedit-spy.png)

<span data-ttu-id="e4d70-132">Cuando GraphEdit carga el gráfico, se ejecuta en el contexto de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="e4d70-132">When GraphEdit loads the graph, it executes in the context of the target application.</span></span> <span data-ttu-id="e4d70-133">Por lo tanto, GraphEdit podría bloquearse porque está esperando el subproceso.</span><span class="sxs-lookup"><span data-stu-id="e4d70-133">Therefore, GraphEdit might block because it is waiting for the thread.</span></span> <span data-ttu-id="e4d70-134">Por ejemplo, esto puede ocurrir si está recorriendo el código en el depurador.</span><span class="sxs-lookup"><span data-stu-id="e4d70-134">For example, this can occur if you are stepping through your code in the debugger.</span></span>

<span data-ttu-id="e4d70-135">Esta característica solo debe usarse en las compilaciones de depuración de la aplicación, no en las compilaciones comerciales, ya que permite que otras aplicaciones vean o controlen el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e4d70-135">This feature should be used only in debug builds of your application, not retail builds, because it enables other applications to view or control the filter graph.</span></span>

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a><span data-ttu-id="e4d70-136">Conexión a un grafo remoto desde la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="e4d70-136">Connecting to a Remote Graph from the Command Line</span></span>

<span data-ttu-id="e4d70-137">GraphEdit admite una opción de línea de comandos para cargar un grafo remoto automáticamente en el inicio.</span><span class="sxs-lookup"><span data-stu-id="e4d70-137">GraphEdit supports a command-line option to load a remote graph automatically on startup.</span></span> <span data-ttu-id="e4d70-138">La sintaxis es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4d70-138">The syntax is:</span></span>


```C++
GraphEdt -a moniker
```



<span data-ttu-id="e4d70-139">donde *moniker* es un moniker creado mediante la función AddToRot, descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e4d70-139">where *moniker* is a moniker created using the AddToRot function, described previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4d70-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4d70-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4d70-141">Simular la compilación de gráficos con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="e4d70-141">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



