---
title: Instrucciones COM y Unicode
description: Dado que Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), los desarrolladores necesitan un nivel moderado de comprensión acerca de los objetos e interfaces COM y deben saber cómo realizar tareas básicas (por ejemplo, cómo inicializar la biblioteca COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2312b6177891c31c0987b846f7adfc1aa08abc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714395"
---
# <a name="com-and-unicode-guidelines"></a><span data-ttu-id="93a56-103">Instrucciones COM y Unicode</span><span class="sxs-lookup"><span data-stu-id="93a56-103">COM and Unicode Guidelines</span></span>

<span data-ttu-id="93a56-104">Dado que Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), los desarrolladores necesitan un nivel moderado de comprensión acerca de los objetos e interfaces COM y deben saber cómo realizar tareas básicas (por ejemplo, cómo inicializar la biblioteca COM).</span><span class="sxs-lookup"><span data-stu-id="93a56-104">Because Microsoft Active Accessibility is based on Component Object Model (COM), developers need a moderate level of understanding about COM objects and interfaces and must know how to perform basic tasks (for example, how to initialize the COM library).</span></span> <span data-ttu-id="93a56-105">Los desarrolladores de servidores deben entender cómo diseñar las clases que implementan la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y cómo crear objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="93a56-105">Server developers need to understand how to design classes that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and how to create accessible objects.</span></span>

<span data-ttu-id="93a56-106">También necesita un nivel moderado de comprensión de Unicode para usar muchas de las funciones de Microsoft Active Accessibility que devuelven cadenas.</span><span class="sxs-lookup"><span data-stu-id="93a56-106">You also need a moderate level of understanding about Unicode to use many of the Microsoft Active Accessibility functions that return strings.</span></span>

<span data-ttu-id="93a56-107">Para usar Microsoft Active Accessibility de forma eficaz, debe comprender las siguientes funciones, estructuras, tipos de datos e interfaces COM y Unicode.</span><span class="sxs-lookup"><span data-stu-id="93a56-107">To use Microsoft Active Accessibility effectively, you should understand the following COM and Unicode functions, structures, data types, and interfaces.</span></span> <span data-ttu-id="93a56-108">En esta documentación se proporciona información limitada sobre algunos de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="93a56-108">Limited information about some of these items is provided in this documentation.</span></span>

### <a name="functions"></a><span data-ttu-id="93a56-109">Funciones:</span><span class="sxs-lookup"><span data-stu-id="93a56-109">Functions:</span></span>

-   [<span data-ttu-id="93a56-110">**OleInitialize**</span><span class="sxs-lookup"><span data-stu-id="93a56-110">**OleInitialize**</span></span>](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   <span data-ttu-id="93a56-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span><span class="sxs-lookup"><span data-stu-id="93a56-111">[**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)</span></span>
-   <span data-ttu-id="93a56-112">[**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) y [ **IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span><span class="sxs-lookup"><span data-stu-id="93a56-112">[**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)</span></span>
-   <span data-ttu-id="93a56-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) y [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span><span class="sxs-lookup"><span data-stu-id="93a56-113">[**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)</span></span>
-   <span data-ttu-id="93a56-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span><span class="sxs-lookup"><span data-stu-id="93a56-114">[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)</span></span>
-   <span data-ttu-id="93a56-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) y [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span><span class="sxs-lookup"><span data-stu-id="93a56-115">[**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) and [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)</span></span>

### <a name="structures-and-data-types"></a><span data-ttu-id="93a56-116">Estructuras y tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="93a56-116">Structures and data types:</span></span>

-   [<span data-ttu-id="93a56-117">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="93a56-117">**VARIANT**</span></span>](variant-structure.md)
-   [<span data-ttu-id="93a56-118">**VALOR**</span><span class="sxs-lookup"><span data-stu-id="93a56-118">**HRESULT**</span></span>](/windows/desktop/com/structure-of-com-error-codes)
-   [<span data-ttu-id="93a56-119">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="93a56-119">**BSTR**</span></span>](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a><span data-ttu-id="93a56-120">Interfaces COM:</span><span class="sxs-lookup"><span data-stu-id="93a56-120">COM Interfaces:</span></span>

-   [<span data-ttu-id="93a56-121">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="93a56-121">**IUnknown**</span></span>](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [<span data-ttu-id="93a56-122">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="93a56-122">**IDispatch**</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="93a56-123">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="93a56-123">**IEnumVARIANT**</span></span>](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a><span data-ttu-id="93a56-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="93a56-124">In this section</span></span>

-   [<span data-ttu-id="93a56-125">VARIANT (estructura)</span><span class="sxs-lookup"><span data-stu-id="93a56-125">VARIANT Structure</span></span>](variant-structure.md)
-   [<span data-ttu-id="93a56-126">Interfaz IDispatch</span><span class="sxs-lookup"><span data-stu-id="93a56-126">IDispatch Interface</span></span>](idispatch-interface.md)
-   [<span data-ttu-id="93a56-127">Convertir cadenas ANSI y Unicode</span><span class="sxs-lookup"><span data-stu-id="93a56-127">Converting Unicode and ANSI Strings</span></span>](converting-unicode-and-ansi-strings.md)

 

 