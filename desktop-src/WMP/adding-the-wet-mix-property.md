---
title: Agregar la propiedad de combinación húmeda
description: Agregar la propiedad de combinación húmeda
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
- Ejemplo de complemento de DSP de eco, propiedad de combinación húmeda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357127"
---
# <a name="adding-the-wet-mix-property"></a><span data-ttu-id="b35f2-109">Agregar la propiedad de combinación húmeda</span><span class="sxs-lookup"><span data-stu-id="b35f2-109">Adding the Wet Mix Property</span></span>

<span data-ttu-id="b35f2-110">Debe agregar el código para proporcionar la propiedad adicional para el nivel de efecto.</span><span class="sxs-lookup"><span data-stu-id="b35f2-110">You must add the code to provide the additional property for the effect level.</span></span>

<span data-ttu-id="b35f2-111">En la sección [Agregar propiedades al complemento DSP de audio de ejemplo se](adding-properties-to-the-sample-audio-dsp-plug-in.md) proporcionan detalles sobre cómo agregar una nueva propiedad mediante Visual C++.</span><span class="sxs-lookup"><span data-stu-id="b35f2-111">The section [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) provides details about how to add a new property using Visual C++.</span></span> <span data-ttu-id="b35f2-112">En esta sección se muestra cómo agregar el código manualmente.</span><span class="sxs-lookup"><span data-stu-id="b35f2-112">This section shows you how to add the code manually.</span></span> <span data-ttu-id="b35f2-113">Esto implica agregar código en los mismos tres lugares en los que se modificó el código para la propiedad tiempo de retraso.</span><span class="sxs-lookup"><span data-stu-id="b35f2-113">This entails adding code in the same three places where you modified the code for the delay time property.</span></span>

<span data-ttu-id="b35f2-114">Agregue los prototipos para los \_ métodos Get WETMIX y put \_ WETMIX inmediatamente después de los otros prototipos de método de propiedad en echo. h.</span><span class="sxs-lookup"><span data-stu-id="b35f2-114">Add the prototypes for the get\_wetmix and put\_wetmix methods immediately following the other property method prototypes in Echo.h.</span></span> <span data-ttu-id="b35f2-115">Use la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="b35f2-115">Use the following syntax:</span></span>


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



<span data-ttu-id="b35f2-116">Ahora, agregue la implementación de cada método inmediatamente después de las otras implementaciones de propiedades en echo. cpp.</span><span class="sxs-lookup"><span data-stu-id="b35f2-116">Now, add the implementation for each method immediately following the other property implementations in Echo.cpp.</span></span> <span data-ttu-id="b35f2-117">En el ejemplo siguiente se muestra el código de ambos métodos:</span><span class="sxs-lookup"><span data-stu-id="b35f2-117">The following example shows the code for both methods:</span></span>


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



<span data-ttu-id="b35f2-118">Observe que la implementación de put \_ WETMIX incluye el código para calcular el valor correcto para m \_ fDryMix.</span><span class="sxs-lookup"><span data-stu-id="b35f2-118">Notice that the implementation of put\_wetmix includes the code to calculate the correct value for m\_fDryMix.</span></span> <span data-ttu-id="b35f2-119">Cada vez que se especifica un nuevo valor para m \_ fWetMix, se requiere este cálculo.</span><span class="sxs-lookup"><span data-stu-id="b35f2-119">Each time a new value is specified for m\_fWetMix, this calculation is required.</span></span>

<span data-ttu-id="b35f2-120">Agregue el código siguiente en la definición de interfaz justo después del código para los métodos de retraso en echo. idl:</span><span class="sxs-lookup"><span data-stu-id="b35f2-120">Add the following code in the interface definition just after the code for the delay methods in Echo.idl:</span></span>


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a><span data-ttu-id="b35f2-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b35f2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b35f2-122">**Eco de propiedades de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="b35f2-122">**Echo Sample Properties**</span></span>](echo-sample-properties.md)
</dt> </dl>

 

 




