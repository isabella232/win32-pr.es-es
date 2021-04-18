---
description: Enumerar efectos y transiciones
ms.assetid: 364b7bfb-5d6e-4ca6-b0c8-7a0180c3f61a
title: Enumerar efectos y transiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e533f36501ac8da6015cc31eea6c2c111bf6a208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677107"
---
# <a name="enumerating-effects-and-transitions"></a><span data-ttu-id="9198a-103">Enumerar efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="9198a-103">Enumerating Effects and Transitions</span></span>

<span data-ttu-id="9198a-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9198a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9198a-105">DirectShow proporciona un objeto de [enumerador de dispositivos del sistema](system-device-enumerator.md) para enumerar los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="9198a-105">DirectShow provides a [System Device Enumerator](system-device-enumerator.md) object for enumerating devices.</span></span> <span data-ttu-id="9198a-106">Puede usarlo para recuperar monikers para efectos o transiciones instalados en el sistema del usuario.</span><span class="sxs-lookup"><span data-stu-id="9198a-106">You can use it to retrieve monikers for effects or transitions installed on the user's system.</span></span>

<span data-ttu-id="9198a-107">El enumerador de dispositivos del sistema expone la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .</span><span class="sxs-lookup"><span data-stu-id="9198a-107">The system device enumerator exposes the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span> <span data-ttu-id="9198a-108">Devuelve los enumeradores de categoría para las categorías de dispositivos especificadas.</span><span class="sxs-lookup"><span data-stu-id="9198a-108">It returns category enumerators for specified device categories.</span></span> <span data-ttu-id="9198a-109">Un enumerador de categoría, a su vez, expone la interfaz [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) y devuelve monikers para cada dispositivo de la categoría.</span><span class="sxs-lookup"><span data-stu-id="9198a-109">A category enumerator, in turn, exposes the [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) interface and returns monikers for each device in the category.</span></span> <span data-ttu-id="9198a-110">Para obtener una explicación detallada del uso de **ICreateDevEnum**, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9198a-110">For a detailed discussion of using **ICreateDevEnum**, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span> <span data-ttu-id="9198a-111">A continuación se encuentra un breve resumen, específico de los servicios de edición de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9198a-111">The following is a brief summary, specific to DirectShow Editing Services.</span></span>

<span data-ttu-id="9198a-112">Para enumerar los efectos o las transiciones, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9198a-112">To enumerate effects or transitions, perform the following steps.</span></span>

1.  <span data-ttu-id="9198a-113">Cree una instancia del enumerador de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="9198a-113">Create an instance of the system device enumerator.</span></span>
2.  <span data-ttu-id="9198a-114">Llame al método [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) para recuperar un enumerador de categoría.</span><span class="sxs-lookup"><span data-stu-id="9198a-114">Call the [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) method to retrieve a category enumerator.</span></span> <span data-ttu-id="9198a-115">Las categorías se definen por los identificadores de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="9198a-115">Categories are defined by class identifiers (CLSIDs).</span></span> <span data-ttu-id="9198a-116">Use CLSID \_ VideoEffects1Category para los efectos o CLSID \_ VideoEffects2Category para las transiciones.</span><span class="sxs-lookup"><span data-stu-id="9198a-116">Use CLSID\_VideoEffects1Category for effects or CLSID\_VideoEffects2Category for transitions.</span></span>
3.  <span data-ttu-id="9198a-117">Llame a **IEnumMoniker:: Next** para recuperar cada moniker de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="9198a-117">Call **IEnumMoniker::Next** to retrieve each moniker in the enumeration.</span></span>
4.  <span data-ttu-id="9198a-118">Para cada moniker, llame a **IMoniker:: BindToStorage** para recuperar el contenedor de propiedades asociado.</span><span class="sxs-lookup"><span data-stu-id="9198a-118">For each moniker, call **IMoniker::BindToStorage** to retrieve its associated property bag.</span></span>

<span data-ttu-id="9198a-119">La bolsa de propiedades contiene el nombre descriptivo y el identificador único global (GUID) para el efecto o la transición.</span><span class="sxs-lookup"><span data-stu-id="9198a-119">The property bag contains the friendly name and the globally unique identifier (GUID) for the effect or transition.</span></span> <span data-ttu-id="9198a-120">Una aplicación puede mostrar una lista de nombres descriptivos y, a continuación, obtener el GUID correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9198a-120">An application can display a list of friendly names and then obtain the corresponding GUID.</span></span>

<span data-ttu-id="9198a-121">En el ejemplo de código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="9198a-121">The following code example illustrates these steps.</span></span>


```C++
ICreateDevEnum *pCreateDevEnum = NULL;
IEnumMoniker *pEnumMoniker = NULL;

// Create the System Device Enumerator.
HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
    CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, (void**)&pCreateDevEnum);
if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

// Create an enumerator for the video effects category.
hr = pCreateDevEnum->CreateClassEnumerator(
    CLSID_VideoEffects1Category,  // Video effects category. 
    &pEnumMoniker, 0);               

// Note: Use CLSID_VideoEffects2Category for video transitions.

if (hr == S_OK)  // S_FALSE means the category is empty.
{
    // Enumerate each video effect.
    IMoniker *pMoniker;
    while (S_OK == pEnumMoniker->Next(1, &pMoniker, NULL))
    {
        IPropertyBag *pBag;
        hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
            (void **)&pBag);
        if(FAILED(hr))
        {
            pMoniker->Release();
            continue; // Maybe the next one will work.
        }
        VARIANT var;
        VariantInit(&var);
        hr = pBag->Read(OLESTR("FriendlyName"), &var, NULL);
        if (SUCCEEDED(hr))
        {
            if ( ... )  // Check if var.bstrVal is the name you want.
            {
                VARIANT var2;
                GUID guid;
                var2.vt = VT_BSTR;
                pBag->Read(OLESTR("guid"), &var2, NULL);
                CLSIDFromString(var2.bstrVal, &guid);
                VariantClear(&var2);
                // GUID is now the CLSID for the effect.
            }
        }
        VariantClear(&var);
        pBag->Release();
        pMoniker->Release();
    }
    pEnumMoniker->Release();
}
pCreateDevEnum->Release();
```



## <a name="related-topics"></a><span data-ttu-id="9198a-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9198a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9198a-123">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="9198a-123">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
