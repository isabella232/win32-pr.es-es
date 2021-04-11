---
description: Paso 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Paso 4. Crear la página de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279669"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="0496f-104">Paso 4.</span><span class="sxs-lookup"><span data-stu-id="0496f-104">Step 4.</span></span> <span data-ttu-id="0496f-105">Crear la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="0496f-105">Create the Property Page</span></span>

<span data-ttu-id="0496f-106">En este momento, el filtro admite todo lo que necesita para una página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0496f-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="0496f-107">El paso siguiente es implementar la propia página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0496f-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="0496f-108">Empiece por derivar una nueva clase de **CBasePropertyPage**.</span><span class="sxs-lookup"><span data-stu-id="0496f-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="0496f-109">En el ejemplo siguiente se muestra parte de la declaración, incluidas algunas variables miembro privadas que se utilizarán más adelante en el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0496f-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="0496f-110">A continuación, cree un recurso de cuadro de diálogo en el editor de recursos, junto con un recurso de cadena para el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0496f-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="0496f-111">La cadena aparecerá en la pestaña de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0496f-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="0496f-112">Los dos identificadores de recursos son argumentos del constructor **CBasePropertyPage** :</span><span class="sxs-lookup"><span data-stu-id="0496f-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="0496f-113">En la ilustración siguiente se muestra el recurso de cuadro de diálogo de la página de propiedades de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0496f-113">The following illustration shows the dialog resource for the example property page.</span></span>

![cuadro de diálogo Página de propiedades](images/proppage.png)

<span data-ttu-id="0496f-115">Ahora está listo para implementar la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0496f-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="0496f-116">Estos son los métodos de **CBasePropertyPage** para invalidar:</span><span class="sxs-lookup"><span data-stu-id="0496f-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="0496f-117">Se llama a **alconnect** cuando el cliente crea la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0496f-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="0496f-118">Establece el puntero **IUnknown** en el filtro.</span><span class="sxs-lookup"><span data-stu-id="0496f-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="0496f-119">Se llama a **OnActivate** cuando se crea el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0496f-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="0496f-120">Se llama a **OnReceiveMessage** cuando el cuadro de diálogo recibe un mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="0496f-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="0496f-121">Se llama a **OnApplyChanges** cuando el usuario confirma los cambios de propiedad haciendo clic en el botón **Aceptar** o **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="0496f-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="0496f-122">Se llama a **OnDisconnect** cuando el usuario descarta la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0496f-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="0496f-123">En el resto de este tutorial se describe cada uno de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0496f-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="0496f-124">Siguiente: [paso 5. Almacene un puntero al filtro](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="0496f-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0496f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0496f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0496f-126">Crear una página de propiedades de filtro</span><span class="sxs-lookup"><span data-stu-id="0496f-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



