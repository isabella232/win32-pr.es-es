---
description: Defina un mecanismo para establecer la propiedad como parte de la creación de una página de propiedades de filtro para un filtro de DirectShow personalizado.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Paso 1. Definir un mecanismo para establecer la propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410078"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a><span data-ttu-id="d5b09-104">Paso 1.</span><span class="sxs-lookup"><span data-stu-id="d5b09-104">Step 1.</span></span> <span data-ttu-id="d5b09-105">Definir un mecanismo para establecer la propiedad</span><span class="sxs-lookup"><span data-stu-id="d5b09-105">Define a Mechanism for Setting the Property</span></span>

<span data-ttu-id="d5b09-106">El filtro debe admitir una manera de que la página de propiedades se comunique con ella, de modo que la página de propiedades pueda establecer y recuperar propiedades en el filtro.</span><span class="sxs-lookup"><span data-stu-id="d5b09-106">The filter must support a way for the property page to communicate with it, so that the property page can set and retrieve properties on the filter.</span></span> <span data-ttu-id="d5b09-107">Entre los posibles mecanismos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5b09-107">Possible mechanisms include the following:</span></span>

-   <span data-ttu-id="d5b09-108">Exponer una interfaz COM personalizada.</span><span class="sxs-lookup"><span data-stu-id="d5b09-108">Expose a custom COM interface.</span></span>
-   <span data-ttu-id="d5b09-109">Admite propiedades de Automation mediante **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="d5b09-109">Support Automation properties, through **IDispatch**.</span></span>
-   <span data-ttu-id="d5b09-110">Exponga **la interfaz IPropertyBag** y defina un conjunto de propiedades con nombre.</span><span class="sxs-lookup"><span data-stu-id="d5b09-110">Expose the **IPropertyBag** interface and define a set of named properties.</span></span>

<span data-ttu-id="d5b09-111">En este ejemplo se usa una interfaz COM personalizada, denominada ISaturation.</span><span class="sxs-lookup"><span data-stu-id="d5b09-111">This example uses a custom COM interface, named ISaturation.</span></span> <span data-ttu-id="d5b09-112">No se trata de una interfaz real de DirectShow; solo se define para este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d5b09-112">This is not an actual DirectShow interface; it is defined only for this example.</span></span> <span data-ttu-id="d5b09-113">Comience declarando la interfaz en un archivo de encabezado, junto con el identificador de interfaz (IID):</span><span class="sxs-lookup"><span data-stu-id="d5b09-113">Start by declaring the interface in a header file, along with the interface identifier (IID):</span></span>


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



<span data-ttu-id="d5b09-114">También puede definir la interfaz con IDL y usar el compilador MIDL para crear el archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d5b09-114">You can also define the interface with IDL and use the MIDL compiler to create the header file.</span></span> <span data-ttu-id="d5b09-115">A continuación, implemente la interfaz personalizada en el filtro.</span><span class="sxs-lookup"><span data-stu-id="d5b09-115">Next, implement the custom interface in the filter.</span></span> <span data-ttu-id="d5b09-116">En este ejemplo se usan los métodos "Get" y "Set" para el valor de saturación del filtro.</span><span class="sxs-lookup"><span data-stu-id="d5b09-116">This example uses "Get" and "Set" methods for the filter's saturation value.</span></span> <span data-ttu-id="d5b09-117">Observe que ambos métodos protegen el miembro \_ m lSaturation con una sección crítica.</span><span class="sxs-lookup"><span data-stu-id="d5b09-117">Notice that both methods protect the m\_lSaturation member with a critical section.</span></span>


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



<span data-ttu-id="d5b09-118">Por supuesto, los detalles de su propia implementación serán diferentes del ejemplo que se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="d5b09-118">Of course, the details of your own implementation will differ from the example shown here.</span></span>

<span data-ttu-id="d5b09-119">Siguiente: [Paso 2. Implemente ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span><span class="sxs-lookup"><span data-stu-id="d5b09-119">Next: [Step 2. Implement ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5b09-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5b09-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5b09-121">**CCritSec (clase)**</span><span class="sxs-lookup"><span data-stu-id="d5b09-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> <dt>

[<span data-ttu-id="d5b09-122">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="d5b09-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



