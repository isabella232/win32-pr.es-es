---
description: Declaración de la plantilla de fábrica
ms.assetid: 3060c167-ea23-4061-b32a-16e750f55e6f
title: Declaración de la plantilla de fábrica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3168f16b6281417846f13b7a17141282053c4705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152060"
---
# <a name="declaring-the-factory-template"></a><span data-ttu-id="acf40-103">Declaración de la plantilla de fábrica</span><span class="sxs-lookup"><span data-stu-id="acf40-103">Declaring the Factory Template</span></span>

<span data-ttu-id="acf40-104">El siguiente paso consiste en declarar la plantilla de generador para el filtro.</span><span class="sxs-lookup"><span data-stu-id="acf40-104">The next step is to declare the factory template for your filter.</span></span> <span data-ttu-id="acf40-105">Una plantilla de generador es una clase de C++ que contiene información para el generador de clases.</span><span class="sxs-lookup"><span data-stu-id="acf40-105">A factory template is a C++ class that contains information for the class factory.</span></span> <span data-ttu-id="acf40-106">En el archivo DLL, declare una matriz global de objetos [**CFactoryTemplate**](cfactorytemplate.md) , uno para cada filtro o componente com del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="acf40-106">In your DLL, declare a global array of [**CFactoryTemplate**](cfactorytemplate.md) objects, one for each filter or COM component in your DLL.</span></span> <span data-ttu-id="acf40-107">La matriz se debe denominar *g \_ templates*.</span><span class="sxs-lookup"><span data-stu-id="acf40-107">The array must be named *g\_Templates*.</span></span> <span data-ttu-id="acf40-108">Para obtener más información acerca de las plantillas de fábrica, consulte [How to Create a DirectShow Filter dll](how-to-create-a-dll.md).</span><span class="sxs-lookup"><span data-stu-id="acf40-108">For more information about factory templates, see [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).</span></span>

<span data-ttu-id="acf40-109">El miembro de **\_ \_ filtro m pAMovieSetup** de la plantilla de generador es un puntero a la estructura de [**\_ filtros AMOVIESETUP**](amoviesetup-filter.md) descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="acf40-109">The **m\_pAMovieSetup\_Filter** member of the factory template is a pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure described previously.</span></span> <span data-ttu-id="acf40-110">En el ejemplo siguiente se muestra una plantilla de generador, usando la estructura proporcionada en el ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="acf40-110">The following example shows a factory template, using the structure given in the previous example:</span></span>


```C++
CFactoryTemplate g_Templates[] = {
    {
        g_wszName,                      // Name.
        &CLSID_SomeFilter,              // CLSID.
        CSomeFilter::CreateInstance,    // Creation function.
        NULL,
        &sudFilterReg                   // Pointer to filter information.
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);
```



<span data-ttu-id="acf40-111">Si no declaras ninguna información de filtro, el **\_ \_ filtro m PAMoveSetup** puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="acf40-111">If you did not declare any filter information, **m\_pAMoveSetup\_Filter** can be **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acf40-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acf40-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acf40-113">Cómo registrar filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="acf40-113">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



