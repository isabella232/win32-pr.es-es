---
description: Registro de DMO
ms.assetid: 9f74fc1c-b903-4725-b667-3c56a2726dbc
title: Registro de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c5364304fd5f6a9557c84a4b27c86d29fa4e84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686322"
---
# <a name="registering-a-dmo"></a><span data-ttu-id="9b505-103">Registro de DMO</span><span class="sxs-lookup"><span data-stu-id="9b505-103">Registering a DMO</span></span>

<span data-ttu-id="9b505-104">Para que los clientes puedan usar DMO, el CLSID debe estar registrado en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="9b505-104">In order for clients to use your DMO, the CLSID must be registered on the user's system.</span></span> <span data-ttu-id="9b505-105">Esto se realiza a través de la función **DllRegisterServer** del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="9b505-105">This is done through the DLL's **DllRegisterServer** function.</span></span> <span data-ttu-id="9b505-106">Si utiliza el Active Template Library (ATL), el Asistente para ATL generará automáticamente esta función.</span><span class="sxs-lookup"><span data-stu-id="9b505-106">If you are using the Active Template Library (ATL), the ATL wizard automatically generates this function.</span></span>

<span data-ttu-id="9b505-107">También puede registrar su DMO en una o varias categorías estándar de DMO.</span><span class="sxs-lookup"><span data-stu-id="9b505-107">You can also register your DMO under one or more standard DMO categories.</span></span> <span data-ttu-id="9b505-108">Esto permite a los clientes detectar su DMO mediante la función [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) .</span><span class="sxs-lookup"><span data-stu-id="9b505-108">This enables clients to discover your DMO using the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function.</span></span> <span data-ttu-id="9b505-109">Las categorías se definen mediante GUID y se enumeran en la sección [identificadores GUID de DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="9b505-109">The categories are defined by GUID, and are listed in the section [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="9b505-110">El registro de un DMO en una categoría es opcional.</span><span class="sxs-lookup"><span data-stu-id="9b505-110">Registering a DMO under a category is optional.</span></span> <span data-ttu-id="9b505-111">Para ello, llame a la función [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) y especifique el nombre descriptivo de DMO, el CLSID y la categoría.</span><span class="sxs-lookup"><span data-stu-id="9b505-111">To do so, call the [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) function and specify the friendly name of the DMO, the CLSID, and the category.</span></span> <span data-ttu-id="9b505-112">Opcionalmente, también puede registrar un conjunto de tipos de medios que admita su DMOs.</span><span class="sxs-lookup"><span data-stu-id="9b505-112">Optionally, you can also register a set of media types that your DMOs supports.</span></span> <span data-ttu-id="9b505-113">Para obtener más información, consulte [tipos de medios de DMO](dmo-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="9b505-113">For more information, see [DMO Media Types](dmo-media-types.md).</span></span>

<span data-ttu-id="9b505-114">En el ejemplo siguiente se muestra cómo registrar un efecto de audio DMO que admite entrada y salida de audio PCM.</span><span class="sxs-lookup"><span data-stu-id="9b505-114">The following example shows how to register an audio effect DMO that supports PCM audio input and output.</span></span> <span data-ttu-id="9b505-115">En este caso, los tipos de entrada y de salida son los mismos.</span><span class="sxs-lookup"><span data-stu-id="9b505-115">In this case the input types and output types are the same.</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    // Register the DMO as a PCM audio effect DMO
    DMO_PARTIAL_MEDIATYPE mt;
    mt.type    = MEDIATYPE_Audio;
    mt.subtype = MEDIASUBTYPE_PCM;
    HRESULT hr = DMORegister(
        L"MyDMO",                  // Friendly name
        CLSID_MyDMO,               // CLSID
        DMOCATEGORY_AUDIO_EFFECT,  // Category
        0,                         // Flags 
        1,                         // Number of input types
        &mt,                       // Array of input types
        1,                         // Number of output types
        &mt);                      // Array of output types

    if (FAILED(hr)) return hr;

    // Registers the object, with no typelib.
    return _Module.RegisterServer(FALSE);
}
```



<span data-ttu-id="9b505-116">En este ejemplo se da por supuesto que ATL se ha usado para crear el proyecto; la última línea de la función llama al método ATL estándar para registrar el servidor COM.</span><span class="sxs-lookup"><span data-stu-id="9b505-116">This example assumes that ATL was used to create the project; the last line of the function calls the standard ATL method to register the COM server.</span></span> <span data-ttu-id="9b505-117">Si no usa ATL, la función tendrá un aspecto diferente.</span><span class="sxs-lookup"><span data-stu-id="9b505-117">If you are not using ATL, your function will look different.</span></span>

<span data-ttu-id="9b505-118">**Anulación del registro de DMO**</span><span class="sxs-lookup"><span data-stu-id="9b505-118">**Unregistering a DMO**</span></span>

<span data-ttu-id="9b505-119">La función **DllUnregisterServer** debe quitar las entradas del registro que crea la función **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="9b505-119">Your **DllUnregisterServer** function must remove any registry entries that the **DllRegisterServer** function creates.</span></span> <span data-ttu-id="9b505-120">Si llama a **DMORegister** al registrar DMO, debe [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) con la misma categoría al anular el registro de DMO.</span><span class="sxs-lookup"><span data-stu-id="9b505-120">If you call **DMORegister** when you register the DMO, you must [**DMOUnregister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister) with the same category when you unregister the DMO.</span></span>

<span data-ttu-id="9b505-121">En el ejemplo siguiente se quitan las entradas del registro creadas en el ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="9b505-121">The following example removes the registry entries created in the previous example:</span></span>


```C++
STDAPI DllUnregisterServer(void)
{
    DMOUnregister(CLSID_MyDMO, DMOCATEGORY_AUDIO_EFFECT);
    return _Module.UnregisterServer(TRUE);
}
```



<span data-ttu-id="9b505-122">**Valores de méritos de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="9b505-122">**DirectShow Merit Values**</span></span>

<span data-ttu-id="9b505-123">A efectos de la generación de gráficos de filtros, DirectShow asigna un valor de mérito predeterminado a DMOs.</span><span class="sxs-lookup"><span data-stu-id="9b505-123">For purposes of building filter graphs, DirectShow assigns a default merit value to DMOs.</span></span> <span data-ttu-id="9b505-124">Puede invalidar este valor agregando una entrada del registro a la clave del registro de DMO en el \_ CLSID raíz de las clases HKEY \_ \\ .</span><span class="sxs-lookup"><span data-stu-id="9b505-124">You can override this value by adding a registry entry to the DMO's registry key in HKEY\_CLASSES\_ROOT\\CLSID.</span></span> <span data-ttu-id="9b505-125">Incluya un valor **DWORD** denominado `Merit` cuyo valor especifique el mérito.</span><span class="sxs-lookup"><span data-stu-id="9b505-125">Include a **DWORD** value named `Merit` whose value specifies the merit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b505-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b505-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b505-127">Escritura de DMO</span><span class="sxs-lookup"><span data-stu-id="9b505-127">Writing a DMO</span></span>](writing-a-dmo.md)
</dt> </dl>

 

 



