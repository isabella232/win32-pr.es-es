---
description: Declare una clase de C++ que herede la clase base que eligió como parte de la escritura de un filtro de transformación.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Paso 2. Declarar la clase Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410068"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="ce45f-104">Paso 2.</span><span class="sxs-lookup"><span data-stu-id="ce45f-104">Step 2.</span></span> <span data-ttu-id="ce45f-105">Declarar la clase Filter</span><span class="sxs-lookup"><span data-stu-id="ce45f-105">Declare the Filter Class</span></span>

<span data-ttu-id="ce45f-106">Este es el paso 2 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ce45f-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="ce45f-107">Comience declarando una clase de C++ que hereda la clase base:</span><span class="sxs-lookup"><span data-stu-id="ce45f-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="ce45f-108">Cada una de las clases de filtro tiene clases de pin asociadas.</span><span class="sxs-lookup"><span data-stu-id="ce45f-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="ce45f-109">En función de las necesidades específicas del filtro, es posible que tenga que invalidar las clases de pin.</span><span class="sxs-lookup"><span data-stu-id="ce45f-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="ce45f-110">En el caso de **CTransformFilter,** los pines delegan la mayor parte de su trabajo en el filtro, por lo que probablemente no necesite invalidar los pines.</span><span class="sxs-lookup"><span data-stu-id="ce45f-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="ce45f-111">Debe generar un CLSID único para el filtro.</span><span class="sxs-lookup"><span data-stu-id="ce45f-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="ce45f-112">Puede usar la utilidad Guidgen o Uuidgen; nunca copie un GUID existente.</span><span class="sxs-lookup"><span data-stu-id="ce45f-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="ce45f-113">Hay varias maneras de declarar un CLSID.</span><span class="sxs-lookup"><span data-stu-id="ce45f-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="ce45f-114">En el ejemplo siguiente se usa la **\_ macro DEFINE GUID:**</span><span class="sxs-lookup"><span data-stu-id="ce45f-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="ce45f-115">A continuación, escriba un método de constructor para el filtro:</span><span class="sxs-lookup"><span data-stu-id="ce45f-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="ce45f-116">Observe que uno de los parámetros del constructor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) es el CLSID definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ce45f-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="ce45f-117">Siguiente: [Paso 3. Admite la negociación de tipos de medios](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="ce45f-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce45f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce45f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce45f-119">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ce45f-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



