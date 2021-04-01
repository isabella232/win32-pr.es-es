---
title: Interfaces duales (ADSI)
description: Use las interfaces COM para tener acceso a las propiedades y los métodos en cualquier objeto ADSI de proveedor.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793791"
---
# <a name="dual-interfaces-adsi"></a><span data-ttu-id="c3d53-103">Interfaces duales (ADSI)</span><span class="sxs-lookup"><span data-stu-id="c3d53-103">Dual Interfaces (ADSI)</span></span>

<span data-ttu-id="c3d53-104">Use las interfaces COM para tener acceso a las propiedades y los métodos en cualquier objeto ADSI de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c3d53-104">Use COM interfaces to access the properties and methods on any provider ADSI objects.</span></span> <span data-ttu-id="c3d53-105">Una propiedad de solo lectura se asigna a una entrada de interfaz del **formulario \_ <PropertyName> Get**.</span><span class="sxs-lookup"><span data-stu-id="c3d53-105">A read-only property maps to an interface entry of the form **get\_<PropertyName>**.</span></span> <span data-ttu-id="c3d53-106">Una propiedad de lectura y escritura se asigna a dos entradas de interfaz del formulario **Get \_ <PropertyName>** y **Put \_ <PropertyName>**.</span><span class="sxs-lookup"><span data-stu-id="c3d53-106">A read/write property maps to two interface entries of the form **get\_<PropertyName>** and **put\_<PropertyName>**.</span></span>

<span data-ttu-id="c3d53-107">Todos los métodos de una interfaz COM deben:</span><span class="sxs-lookup"><span data-stu-id="c3d53-107">All methods on a COM interface must:</span></span>

-   <span data-ttu-id="c3d53-108">Devuelve un valor HRESULT para indicar si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="c3d53-108">Return an HRESULT value to indicate success or failure.</span></span> <span data-ttu-id="c3d53-109">El tipo **HRESULT** se describe en la especificación com.</span><span class="sxs-lookup"><span data-stu-id="c3d53-109">The **HRESULT** type is discussed in the COM specification.</span></span>
-   <span data-ttu-id="c3d53-110">En las llamadas a **QueryInterface**, se devuelve **E \_ nointerface** para interfaces no implementadas.</span><span class="sxs-lookup"><span data-stu-id="c3d53-110">On calls to **QueryInterface**, return **E\_NOINTERFACE** for unimplemented interfaces.</span></span>
-   <span data-ttu-id="c3d53-111">Devuelve **E \_ NOTIMPL** para los métodos no implementados en interfaces que, de otro modo, se implementan.</span><span class="sxs-lookup"><span data-stu-id="c3d53-111">Return **E\_NOTIMPL** for unimplemented methods on interfaces that are otherwise implemented.</span></span>
-   <span data-ttu-id="c3d53-112">**No se \_ \_ \_ \_ admite la propiedad** Return de E ADS para las propiedades de interfaz que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="c3d53-112">Return **E\_ADS\_PROPERTY\_NOT\_SUPPORTED** for interface properties that are not supported.</span></span>

<span data-ttu-id="c3d53-113">Para conservar la compatibilidad con los controladores de automatización, todos los parámetros y tipos devueltos deben estar dentro del subconjunto definido por el tipo de datos de la variante de automatización.</span><span class="sxs-lookup"><span data-stu-id="c3d53-113">To retain compatibility with Automation controllers, all parameters and return types should be within the subset defined by the Automation VARIANT data type.</span></span> <span data-ttu-id="c3d53-114">Para obtener más información, consulte **Variant** y **VARIANTARG** en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="c3d53-114">For more information, see **VARIANT** and **VARIANTARG** in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="c3d53-115">Un objeto de Active Directory de proveedor puede exponer interfaces que usan tipos de datos distintos de los del subconjunto **Variant** .</span><span class="sxs-lookup"><span data-stu-id="c3d53-115">A provider Active Directory object can expose interfaces that use data types other than those in the **VARIANT** subset.</span></span> <span data-ttu-id="c3d53-116">Sin embargo, los controladores de automatización como Visual Basic no pueden llamar a esas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c3d53-116">However, Automation controllers such as Visual Basic are not able to call those interfaces.</span></span> <span data-ttu-id="c3d53-117">La mayoría de las interfaces del proveedor ADSI derivan de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y se pueden usar como punteros de interfaz **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="c3d53-117">Most ADSI provider interfaces are derived from [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) and can be used as **IDispatch** interface pointers.</span></span> <span data-ttu-id="c3d53-118">Sin embargo, las interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)y [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) no se derivan de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="c3d53-118">However, the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), and [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ADSI interfaces are not derived from **IDispatch**.</span></span>

 

 