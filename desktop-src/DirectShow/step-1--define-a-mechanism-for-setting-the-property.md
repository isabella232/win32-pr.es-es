---
description: Paso 1.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Paso 1. Definir un mecanismo para establecer la propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678088"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="75b88-104">Paso 1.</span><span class="sxs-lookup"><span data-stu-id="75b88-104">Step 1.</span></span> <span data-ttu-id="75b88-105">Definir un mecanismo para establecer la propiedad</span><span class="sxs-lookup"><span data-stu-id="75b88-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="75b88-106">El filtro debe admitir una forma para que la página de propiedades se comunique con él, de modo que la página de propiedades pueda establecer y recuperar propiedades en el filtro.</span><span class="sxs-lookup"><span data-stu-id="75b88-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="75b88-107">Entre los posibles mecanismos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="75b88-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="75b88-108">Exponga una interfaz COM personalizada.</span><span class="sxs-lookup"><span data-stu-id="75b88-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="75b88-109">Compatibilidad con las propiedades de automatización, a través de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="75b88-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="75b88-110">Exponga la interfaz **IPropertyBag** y defina un conjunto de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="75b88-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="75b88-111">En este ejemplo se usa una interfaz COM personalizada, denominada ISaturation.</span><span class="sxs-lookup"><span data-stu-id="75b88-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="75b88-112">No se trata de una interfaz de DirectShow real. solo se define para este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="75b88-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="75b88-113">Empiece por declarar la interfaz en un archivo de encabezado, junto con el identificador de interfaz (IID):</span><span class="sxs-lookup"><span data-stu-id="75b88-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



<span data-ttu-id="75b88-114">También puede definir la interfaz con IDL y usar el compilador MIDL para crear el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="75b88-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="75b88-115">A continuación, implemente la interfaz personalizada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="75b88-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="75b88-116">En este ejemplo se usan los métodos "Get" y "SET" para el valor de saturación del filtro.</span><span class="sxs-lookup"><span data-stu-id="75b88-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="75b88-117">Observe que ambos métodos protegen el \_ miembro m lSaturation con una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="75b88-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



<span data-ttu-id="75b88-118">Por supuesto, los detalles de su propia implementación variarán en el ejemplo que se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="75b88-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="75b88-119">Siguiente: [paso 2. Implemente ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="75b88-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="75b88-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75b88-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b88-121">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="75b88-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="75b88-122">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="75b88-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



