---
description: Implementación de DllRegisterServer
ms.assetid: aaa4069e-0b6a-4a76-b950-1a85a9ed969d
title: Implementación de DllRegisterServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b994e80a181b69efffbe6123382957e7a38f8278
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152508"
---
# <a name="implementing-dllregisterserver"></a><span data-ttu-id="5e023-103">Implementación de DllRegisterServer</span><span class="sxs-lookup"><span data-stu-id="5e023-103">Implementing DllRegisterServer</span></span>

<span data-ttu-id="5e023-104">El paso final consiste en implementar la función **DllRegisterServer** .</span><span class="sxs-lookup"><span data-stu-id="5e023-104">The final step is to implement the **DllRegisterServer** function.</span></span> <span data-ttu-id="5e023-105">El archivo DLL que contiene el componente debe exportar esta función.</span><span class="sxs-lookup"><span data-stu-id="5e023-105">The DLL that contains the component must export this function.</span></span> <span data-ttu-id="5e023-106">Una aplicación de instalación llamará a la función o cuando el usuario ejecute la herramienta Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="5e023-106">The function will be called by a set-up application, or when the user runs the Regsvr32.exe tool.</span></span>

<span data-ttu-id="5e023-107">En el ejemplo siguiente se muestra una implementación mínima de **DlLRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="5e023-107">The following example shows a minimal implementation of **DlLRegisterServer**:</span></span>


```C++
STDAPI DllRegisterServer(void)
{
    return AMovieDllRegisterServer2(TRUE);
}
```



<span data-ttu-id="5e023-108">La función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) crea entradas del registro para cada componente de la</span><span class="sxs-lookup"><span data-stu-id="5e023-108">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function creates registry entries for every component in the</span></span>


```
g_Templates
```



<span data-ttu-id="5e023-109">.</span><span class="sxs-lookup"><span data-stu-id="5e023-109">array.</span></span> <span data-ttu-id="5e023-110">Sin embargo, esta función tiene algunas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="5e023-110">However, this function has some limitations.</span></span> <span data-ttu-id="5e023-111">En primer lugar, asigna todos los filtros a la categoría "filtros de DirectShow" (CLSID \_ LegacyAmFilterCategory), pero no todos los filtros pertenecen a esta categoría.</span><span class="sxs-lookup"><span data-stu-id="5e023-111">First, it assigns every filter to the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory), but not every filter belongs in this category.</span></span> <span data-ttu-id="5e023-112">Los filtros de captura y los filtros de compresión, por ejemplo, tienen sus propias categorías.</span><span class="sxs-lookup"><span data-stu-id="5e023-112">Capture filters and compression filters, for example, have their own categories.</span></span> <span data-ttu-id="5e023-113">En segundo lugar, si el filtro es compatible con un dispositivo de hardware, es posible que deba registrar dos partes adicionales de la información que **AMovieDLLRegisterServer2** no controla: la categoría *medio* y *PIN*.</span><span class="sxs-lookup"><span data-stu-id="5e023-113">Second, if your filter supports a hardware device, you might need to register two additional pieces of information that **AMovieDLLRegisterServer2** does not handle: the *medium* and the *pin category*.</span></span> <span data-ttu-id="5e023-114">Un medio define un método de comunicación en un dispositivo de hardware, como un bus.</span><span class="sxs-lookup"><span data-stu-id="5e023-114">A medium defines a method of communication in a hardware device, such as a bus.</span></span> <span data-ttu-id="5e023-115">La categoría PIN define la función de un PIN.</span><span class="sxs-lookup"><span data-stu-id="5e023-115">The pin category defines the function of a pin.</span></span> <span data-ttu-id="5e023-116">Para obtener información sobre los medios, vea "KSPIN \_ Medium" en el kit de desarrollo de controladores (DDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5e023-116">For information on mediums, see "KSPIN\_MEDIUM" in the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="5e023-117">Para obtener una lista de las categorías de PIN, vea [conjunto de propiedades de PIN](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="5e023-117">For a list of pin categories, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="5e023-118">Si desea especificar una categoría de filtro, un medio o una categoría de PIN, llame al método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) desde el interior de **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="5e023-118">If you want to specify a filter category, a medium, or a pin category, call the [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method from within **DllRegisterServer**.</span></span> <span data-ttu-id="5e023-119">Este método toma un puntero a una estructura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) , que especifica información sobre el filtro.</span><span class="sxs-lookup"><span data-stu-id="5e023-119">This method takes a pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure, which specifies information about the filter.</span></span>

<span data-ttu-id="5e023-120">Para complicar las cosas en cierto modo, la estructura **REGFILTER2** admite dos formatos diferentes para registrar los pin.</span><span class="sxs-lookup"><span data-stu-id="5e023-120">To complicate matters somewhat, the **REGFILTER2** structure supports two different formats for registering pins.</span></span> <span data-ttu-id="5e023-121">El miembro **dwVersion** especifica el formato:</span><span class="sxs-lookup"><span data-stu-id="5e023-121">The **dwVersion** member specifies the format:</span></span>

-   <span data-ttu-id="5e023-122">Si **dwVersion** es 1, el formato del PIN es **AMOVIESETUP \_ PIN** (descrito anteriormente).</span><span class="sxs-lookup"><span data-stu-id="5e023-122">If **dwVersion** is 1, the pin format is **AMOVIESETUP\_PIN** (described previously).</span></span>
-   <span data-ttu-id="5e023-123">Si **dwVersion** es 2, el formato del PIN es [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span><span class="sxs-lookup"><span data-stu-id="5e023-123">If **dwVersion** is 2, the pin format is [**REGFILTERPINS2**](/windows/desktop/api/strmif/ns-strmif-regfilterpins2).</span></span>

<span data-ttu-id="5e023-124">La estructura **REGFILTERPINS2** incluye entradas para las categorías de anclaje medio y PIN.</span><span class="sxs-lookup"><span data-stu-id="5e023-124">The **REGFILTERPINS2** structure includes entries for pin mediums and pin categories.</span></span> <span data-ttu-id="5e023-125">Además, utiliza marcas de bits para algunos elementos que **AMOVIESETUP \_ PIN** declara como valores booleanos.</span><span class="sxs-lookup"><span data-stu-id="5e023-125">Also, it uses bit flags for some items that **AMOVIESETUP\_PIN** declares as Boolean values.</span></span>

<span data-ttu-id="5e023-126">En el ejemplo siguiente se muestra cómo llamar a **IFilterMapper2:: RegisterFilter** desde dentro de **DllRegisterServer**:</span><span class="sxs-lookup"><span data-stu-id="5e023-126">The following example shows how to call **IFilterMapper2::RegisterFilter** from inside **DllRegisterServer**:</span></span>


```C++
REGFILTER2 rf2FilterReg = {
    1,              // Version 1 (no pin mediums or pin category).
    MERIT_NORMAL,   // Merit.
    1,              // Number of pins.
    &sudPins        // Pointer to pin information.
};

STDAPI DllRegisterServer(void)
{
    HRESULT hr;
    IFilterMapper2 *pFM2 = NULL;

    hr = AMovieDllRegisterServer2(TRUE);
    if (FAILED(hr))
        return hr;

    hr = CoCreateInstance(CLSID_FilterMapper2, NULL, CLSCTX_INPROC_SERVER,
            IID_IFilterMapper2, (void **)&pFM2);

    if (FAILED(hr))
        return hr;

    hr = pFM2->RegisterFilter(
        CLSID_SomeFilter,                // Filter CLSID. 
        g_wszName,                       // Filter name.
        NULL,                            // Device moniker. 
        &CLSID_VideoCompressorCategory,  // Video compressor category.
        g_wszName,                       // Instance data.
        &rf2FilterReg                    // Pointer to filter information.
    );
    pFM2->Release();
    return hr;
}
```



 

 



