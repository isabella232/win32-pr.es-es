---
description: En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funciones DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105651439"
---
# <a name="dll-functions"></a><span data-ttu-id="44b19-103">Funciones DLL</span><span class="sxs-lookup"><span data-stu-id="44b19-103">DLL Functions</span></span>

<span data-ttu-id="44b19-104">En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="44b19-104">This topic describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span>

<span data-ttu-id="44b19-105">Un archivo DLL debe implementar las funciones siguientes para que se pueda registrar, anular el registro y cargar en la memoria.</span><span class="sxs-lookup"><span data-stu-id="44b19-105">A DLL must implement the following functions so that it can be registered, unregistered, and loaded into memory.</span></span>

-   <span data-ttu-id="44b19-106">[*DllMain*](/windows/desktop/Dlls/dllmain): el punto de entrada de dll.</span><span class="sxs-lookup"><span data-stu-id="44b19-106">[*DllMain*](/windows/desktop/Dlls/dllmain): The DLL entry point.</span></span> <span data-ttu-id="44b19-107">El nombre *DllMain* es un marcador de posición para el nombre de la función definida por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="44b19-107">The name *DllMain* is a placeholder for the library-defined function name.</span></span> <span data-ttu-id="44b19-108">La implementación de DirectShow usa el nombre **DllEntryPoint**.</span><span class="sxs-lookup"><span data-stu-id="44b19-108">The DirectShow implementation uses the name **DllEntryPoint**.</span></span> <span data-ttu-id="44b19-109">Para obtener más información, vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="44b19-109">For more information, see the Platform SDK.</span></span>
-   <span data-ttu-id="44b19-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): crea una instancia de generador de clases.</span><span class="sxs-lookup"><span data-stu-id="44b19-110">[**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): Creates a class factory instance.</span></span> <span data-ttu-id="44b19-111">Se describe en las secciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="44b19-111">Described in the previous sections.</span></span>
-   <span data-ttu-id="44b19-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): consulta si el archivo dll se puede descargar de forma segura.</span><span class="sxs-lookup"><span data-stu-id="44b19-112">[**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): Queries whether the DLL can safely be unloaded.</span></span>
-   <span data-ttu-id="44b19-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crea entradas del registro para el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="44b19-113">[**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): Creates registry entries for the DLL.</span></span>
-   <span data-ttu-id="44b19-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): quita las entradas del registro para el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="44b19-114">[**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): Removes registry entries for the DLL.</span></span>

<span data-ttu-id="44b19-115">De ellos, DirectShow implementa los tres primeros.</span><span class="sxs-lookup"><span data-stu-id="44b19-115">Of these, the first three are implemented by DirectShow.</span></span> <span data-ttu-id="44b19-116">Si la plantilla de fábrica proporciona una función de inicialización en la variable miembro [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) , se llama a esa función desde dentro de la función de punto de entrada del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="44b19-116">If your factory template provides an initialization function in the [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md) member variable, that function is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="44b19-117">Para obtener más información sobre cuándo el sistema llama a la función de punto de entrada de DLL, vea [*DllMain*](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="44b19-117">For more information on when the system calls the DLL entry-point function, see [*DllMain*](/windows/desktop/Dlls/dllmain).</span></span>

<span data-ttu-id="44b19-118">Debe implementar [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), pero DirectShow proporciona una función denominada [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) que realiza el trabajo necesario.</span><span class="sxs-lookup"><span data-stu-id="44b19-118">You must implement [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), but DirectShow provides a function named [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) that does the necessary work.</span></span> <span data-ttu-id="44b19-119">El componente puede ajustar simplemente esta función, tal y como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="44b19-119">Your component can simply wrap this function, as shown in the following example:</span></span>


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



<span data-ttu-id="44b19-120">Sin embargo, en [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) , puede personalizar el proceso de registro según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="44b19-120">However, within [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) you can customize the registration process as needed.</span></span> <span data-ttu-id="44b19-121">Si el archivo DLL contiene un filtro, puede que tenga que realizar algún trabajo adicional.</span><span class="sxs-lookup"><span data-stu-id="44b19-121">If your DLL contains a filter, you might need to do some additional work.</span></span> <span data-ttu-id="44b19-122">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="44b19-122">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

<span data-ttu-id="44b19-123">En el archivo de definición de módulo (. def), exporte todas las funciones DLL excepto la función de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="44b19-123">In your module-definition (.def) file, export all the DLL functions except for the entry-point function.</span></span> <span data-ttu-id="44b19-124">A continuación se encuentra un archivo. def de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="44b19-124">The following is an example .def file:</span></span>


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



<span data-ttu-id="44b19-125">Puede registrar el archivo DLL mediante la utilidad Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="44b19-125">You can register the DLL using the Regsvr32.exe utility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44b19-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44b19-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44b19-127">Cómo crear un archivo DLL de filtro de DirectShow</span><span class="sxs-lookup"><span data-stu-id="44b19-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
