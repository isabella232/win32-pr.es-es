---
title: Crear la tabla de interfaz global
description: Crear la tabla de interfaz global
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421485"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="5ad9d-103">Crear la tabla de interfaz global</span><span class="sxs-lookup"><span data-stu-id="5ad9d-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="5ad9d-104">Use la siguiente llamada para crear el objeto de tabla de interfaz global y obtener un puntero a [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span><span class="sxs-lookup"><span data-stu-id="5ad9d-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="5ad9d-105">Al crear el objeto de tabla de interfaz global mediante la llamada anterior, es necesario vincularlo a la biblioteca UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="5ad9d-106">Esto resolverá los símbolos externos CLSID \_ StdGlobalInterfaceTable y IID \_ IGlobalInterfaceTable.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="5ad9d-107">Hay una única instancia de la tabla de interfaz global por proceso, por lo que todas las llamadas a esta función en un proceso devuelven la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="5ad9d-108">Después de la llamada a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , registre la interfaz desde el apartamento en el que reside con una llamada al método [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) .</span><span class="sxs-lookup"><span data-stu-id="5ad9d-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="5ad9d-109">Este método proporciona una cookie que identifica la interfaz y su ubicación.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="5ad9d-110">Un contenedor que busca un puntero a esta interfaz llama entonces al método [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) con esta cookie y, a continuación, la implementación proporciona un puntero de interfaz al apartamento que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="5ad9d-111">Para revocar el registro global de la interfaz, cualquier apartamento puede llamar al método [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .</span><span class="sxs-lookup"><span data-stu-id="5ad9d-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="5ad9d-112">Un ejemplo sencillo del uso de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) sería cuando desea pasar un puntero de interfaz a un objeto de un contenedor uniproceso (STA) a un subproceso de trabajo de otro apartamento.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="5ad9d-113">En lugar de tener que calcular las referencias en una secuencia y pasar la secuencia al subproceso de trabajo como un parámetro de subproceso, **IGlobalInterfaceTable** permite simplemente pasar una cookie.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="5ad9d-114">Al registrar la interfaz en la tabla de interfaz global, obtiene una cookie que puede usar en lugar de pasar el puntero real (siempre que necesite pasar el puntero), ya sea a un parámetro que no sea de método que vaya a otro apartamento (como parámetro a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) a través de [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) o a la memoria en proceso accesible fuera del apartamento.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="5ad9d-115">Se requiere cuidado porque el uso de interfaces globales impone la carga adicional en el programador de la administración de problemas, como condiciones de carrera y exclusión mutua, que están asociados a tener acceso al estado global desde varios subprocesos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="5ad9d-116">COM proporciona una implementación estándar de la interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="5ad9d-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="5ad9d-117">Se recomienda encarecidamente que use esta implementación estándar, ya que proporciona una funcionalidad completa de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5ad9d-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ad9d-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ad9d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad9d-119">Cuándo usar la tabla de interfaz global</span><span class="sxs-lookup"><span data-stu-id="5ad9d-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 