---
description: Matriz de plantillas de fábrica
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Matriz de plantillas de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152695"
---
# <a name="factory-template-array"></a><span data-ttu-id="687d9-103">Matriz de plantillas de fábrica</span><span class="sxs-lookup"><span data-stu-id="687d9-103">Factory Template Array</span></span>

<span data-ttu-id="687d9-104">La plantilla de generador contiene las siguientes variables de miembro público:</span><span class="sxs-lookup"><span data-stu-id="687d9-104">The factory template contains the following public member variables:</span></span>

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

<span data-ttu-id="687d9-105">Los dos punteros de función, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) y [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), usan las siguientes definiciones de tipo:</span><span class="sxs-lookup"><span data-stu-id="687d9-105">The two function pointers, [**m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) and [**m\_lpfnInit**](cfactorytemplate-m-lpfninit.md), use the following type definitions:</span></span>

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

<span data-ttu-id="687d9-106">La primera es la función de creación de instancias del componente.</span><span class="sxs-lookup"><span data-stu-id="687d9-106">The first is the instantiation function for the component.</span></span> <span data-ttu-id="687d9-107">La segunda es una función de inicialización opcional.</span><span class="sxs-lookup"><span data-stu-id="687d9-107">The second is an optional initialization function.</span></span> <span data-ttu-id="687d9-108">Si se proporciona una función de inicialización, se llama desde dentro de la función de punto de entrada del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="687d9-108">If you provide an initialization function, it is called from inside the DLL entry-point function.</span></span> <span data-ttu-id="687d9-109">(La función de punto de entrada de DLL se describe más adelante en este artículo).</span><span class="sxs-lookup"><span data-stu-id="687d9-109">(The DLL entry-point function is discussed later in this article.)</span></span>

<span data-ttu-id="687d9-110">Supongamos que está creando un archivo DLL que contiene un componente denominado CMyComponent, que hereda de [**CUnknown**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="687d9-110">Suppose you are creating a DLL that contains a component named CMyComponent, which inherits from [**CUnknown**](cunknown.md).</span></span> <span data-ttu-id="687d9-111">Debe proporcionar los elementos siguientes en el archivo DLL:</span><span class="sxs-lookup"><span data-stu-id="687d9-111">You must provide the following items in your DLL:</span></span>

-   <span data-ttu-id="687d9-112">La función de inicialización, un método público que devuelve una nueva instancia de CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="687d9-112">The initialization function, a public method that returns a new instance of CMyComponent.</span></span>
-   <span data-ttu-id="687d9-113">Una matriz global de plantillas de fábrica, denominada *g \_ templates.*</span><span class="sxs-lookup"><span data-stu-id="687d9-113">A global array of factory templates, named *g\_Templates.*</span></span> <span data-ttu-id="687d9-114">Esta matriz contiene la plantilla de generador para CMyComponent.</span><span class="sxs-lookup"><span data-stu-id="687d9-114">This array contains the factory template for CMyComponent.</span></span>
-   <span data-ttu-id="687d9-115">Una variable global denominada *g \_ cTemplates* que especifica el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="687d9-115">A global variable named *g\_cTemplates* that specifies the size of the array.</span></span>

<span data-ttu-id="687d9-116">En el ejemplo siguiente se muestra cómo declarar estos elementos:</span><span class="sxs-lookup"><span data-stu-id="687d9-116">The following example shows how to declare these items:</span></span>


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



<span data-ttu-id="687d9-117">El `CreateInstance` método llama al constructor de clase y devuelve un puntero a la nueva instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="687d9-117">The `CreateInstance` method calls the class constructor and returns a pointer to the new class instance.</span></span> <span data-ttu-id="687d9-118">El parámetro *pUnk* es un puntero al [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)de agregación.</span><span class="sxs-lookup"><span data-stu-id="687d9-118">The parameter *pUnk* is a pointer to the aggregating [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="687d9-119">Simplemente puede pasar este parámetro al constructor de clase.</span><span class="sxs-lookup"><span data-stu-id="687d9-119">You can simply pass this parameter to the class constructor.</span></span> <span data-ttu-id="687d9-120">El parámetro *pHr* es un puntero a un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="687d9-120">The parameter *pHr* is a pointer to an HRESULT value.</span></span> <span data-ttu-id="687d9-121">El constructor de clase establece este en un valor adecuado, pero si se produce un error en el constructor, establezca el valor en E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="687d9-121">The class constructor sets this to an appropriate value, but if the constructor fails, set the value to E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="687d9-122">La macro [**Name**](name.md) genera una cadena en las compilaciones de depuración, pero se resuelve como **null** en las compilaciones comerciales.</span><span class="sxs-lookup"><span data-stu-id="687d9-122">The [**NAME**](name.md) macro generates a string in debug builds but resolves to **NULL** in retail builds.</span></span> <span data-ttu-id="687d9-123">Se usa en este ejemplo para dar al componente un nombre que aparece en los registros de depuración, pero no ocupa la memoria en la versión final.</span><span class="sxs-lookup"><span data-stu-id="687d9-123">It is used in this example to give the component a name that appears in debug logs but does not occupy memory in the final version.</span></span>

<span data-ttu-id="687d9-124">El `CreateInstance` método puede tener cualquier nombre, ya que el generador de clases hace referencia al puntero de función en la plantilla de generador.</span><span class="sxs-lookup"><span data-stu-id="687d9-124">The `CreateInstance` method can have any name, because the class factory refers to the function pointer in the factory template.</span></span> <span data-ttu-id="687d9-125">Sin embargo, *g \_ templates* y *g \_ cTemplates* son variables globales que el generador de clases espera encontrar, por lo que deben tener exactamente esos nombres.</span><span class="sxs-lookup"><span data-stu-id="687d9-125">However, *g\_Templates* and *g\_cTemplates* are global variables that the class factory expects to find, so they must have exactly those names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="687d9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="687d9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="687d9-127">Cómo crear un archivo DLL de filtro de DirectShow</span><span class="sxs-lookup"><span data-stu-id="687d9-127">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 
