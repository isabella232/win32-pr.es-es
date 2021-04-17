---
description: Paso 2.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Paso 2. Declarar la clase de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ddfe28b7f31238089c331b319621787aef49f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678219"
---
# <a name="step-2-declare-the-filter-class"></a><span data-ttu-id="30c7b-104">Paso 2.</span><span class="sxs-lookup"><span data-stu-id="30c7b-104">Step 2.</span></span> <span data-ttu-id="30c7b-105">Declarar la clase de filtro</span><span class="sxs-lookup"><span data-stu-id="30c7b-105">Declare the Filter Class</span></span>

<span data-ttu-id="30c7b-106">Este es el paso 2 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="30c7b-106">This is step 2 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="30c7b-107">Empiece por declarar una clase de C++ que herede la clase base:</span><span class="sxs-lookup"><span data-stu-id="30c7b-107">Start by declaring a C++ class that inherits the base class:</span></span>


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



<span data-ttu-id="30c7b-108">Cada una de las clases de filtro tiene asociadas clases de PIN.</span><span class="sxs-lookup"><span data-stu-id="30c7b-108">Each of the filter classes has associated pin classes.</span></span> <span data-ttu-id="30c7b-109">En función de las necesidades específicas del filtro, puede que tenga que invalidar las clases de PIN.</span><span class="sxs-lookup"><span data-stu-id="30c7b-109">Depending on the specific needs of your filter, you might need to override the pin classes.</span></span> <span data-ttu-id="30c7b-110">En el caso de **CTransformFilter**, los pin delegan la mayor parte del trabajo en el filtro, por lo que probablemente no sea necesario invalidar los pin.</span><span class="sxs-lookup"><span data-stu-id="30c7b-110">In the case of **CTransformFilter**, the pins delegate most of their work to the filter, so you probably don't need to override the pins.</span></span>

<span data-ttu-id="30c7b-111">Debe generar un CLSID único para el filtro.</span><span class="sxs-lookup"><span data-stu-id="30c7b-111">You must generate a unique CLSID for the filter.</span></span> <span data-ttu-id="30c7b-112">Puede usar la utilidad Guidgen o uuidgen; no copie nunca un GUID existente.</span><span class="sxs-lookup"><span data-stu-id="30c7b-112">You can use the Guidgen or Uuidgen utility; never copy an existing GUID.</span></span> <span data-ttu-id="30c7b-113">Hay varias maneras de declarar un CLSID.</span><span class="sxs-lookup"><span data-stu-id="30c7b-113">There are several ways to declare a CLSID.</span></span> <span data-ttu-id="30c7b-114">En el ejemplo siguiente se usa la macro **definir \_ GUID** :</span><span class="sxs-lookup"><span data-stu-id="30c7b-114">The following example uses the **DEFINE\_GUID** macro:</span></span>


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



<span data-ttu-id="30c7b-115">A continuación, escriba un método de constructor para el filtro:</span><span class="sxs-lookup"><span data-stu-id="30c7b-115">Next, write a constructor method for the filter:</span></span>


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



<span data-ttu-id="30c7b-116">Tenga en cuenta que uno de los parámetros para el constructor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) es el CLSID definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="30c7b-116">Notice that one of the parameters to the [**CTransformFilter**](ctransformfilter-ctransformfilter.md) constructor is the CLSID defined earlier.</span></span>

<span data-ttu-id="30c7b-117">Siguiente: [paso 3. Compatibilidad con la negociación de tipos de medios](step-3--support-media-type-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="30c7b-117">Next: [Step 3. Support Media Type Negotiation](step-3--support-media-type-negotiation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30c7b-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30c7b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30c7b-119">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="30c7b-119">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



