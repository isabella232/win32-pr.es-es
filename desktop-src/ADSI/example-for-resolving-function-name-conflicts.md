---
title: Ejemplo para resolver conflictos de nombres de función
description: En este tema se describe cómo resolver conflictos de nombres de función al crear una extensión para ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Visual Basic de código de ejemplo, resolver conflictos de nombres de función
- resolver conflictos de nombre de función ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359417"
---
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="150b9-105">Ejemplo para resolver conflictos de nombres de función</span><span class="sxs-lookup"><span data-stu-id="150b9-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="150b9-106">Tenga en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="150b9-106">Consider the following:</span></span>

-   <span data-ttu-id="150b9-107">IADs0 no admite Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="150b9-108">IADs1 admite Func1 y Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="150b9-109">IADs2 admite Func2 y Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="150b9-110">Las tres interfaces son interfaces duales.</span><span class="sxs-lookup"><span data-stu-id="150b9-110">All three interfaces are dual interfaces.</span></span>


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



<span data-ttu-id="150b9-111">Tenga en cuenta que, a pesar de que IADs1 no admite Func2, un cliente ADSI reconoce una [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que admite todas las interfaces dual y de distribución del modelo.</span><span class="sxs-lookup"><span data-stu-id="150b9-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="150b9-112">Por lo tanto, el cliente ADSI puede llamar directamente a Func2 mediante myInf1. Func2 sin resolver qué interfaz es compatible con Func2.</span><span class="sxs-lookup"><span data-stu-id="150b9-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="150b9-113">Tanto IADs1 como IADs2 tienen una función llamada Func0, pero IADs1:: Func0 se invoca directamente mediante el acceso vtable, porque las dos siguientes se aplican al cliente:</span><span class="sxs-lookup"><span data-stu-id="150b9-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="150b9-114">El cliente tiene un puntero a un objeto IADs1 de interfaz dual, que tiene una función denominada Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="150b9-115">Visual Basic admite el acceso de vtable directo, suponiendo que ese tipo de datos esté disponible a través de la biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="150b9-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="150b9-116">En el ejemplo de código siguiente, el cliente tiene un puntero de interfaz dual a IADs2 en lugar de IADs1.</span><span class="sxs-lookup"><span data-stu-id="150b9-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="150b9-117">Por lo tanto, IADs2:: Func0 se invoca mediante el acceso de vtable directo.</span><span class="sxs-lookup"><span data-stu-id="150b9-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="150b9-118">De nuevo, en el ejemplo de código siguiente, IADs1 y IADs2 tienen una función llamada Func0, pero, aquí, el cliente tiene un puntero a una interfaz dual, IADs0, que no tiene una función llamada Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="150b9-119">Por lo tanto, no se puede realizar ningún acceso de vtable directo.</span><span class="sxs-lookup"><span data-stu-id="150b9-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="150b9-120">En su lugar, se llama a [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) para invocar Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="150b9-121">Tenga en cuenta estos dos casos:</span><span class="sxs-lookup"><span data-stu-id="150b9-121">Consider these two cases:</span></span>

-   <span data-ttu-id="150b9-122">IADs1 y IADs2 se implementan mediante dos componentes COM, EXT1 y ext2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="150b9-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="150b9-123">Si EXT1 va antes de ext2 en el registro, se invoca IADs1:: Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="150b9-124">Sin embargo, si ext2 aparece primero en el registro, se invoca IADs2:: Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="150b9-125">Si IADs1 y ADs2 se implementan mediante el mismo objeto de extensión, los métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) de la extensión siempre invocan a Func0.</span><span class="sxs-lookup"><span data-stu-id="150b9-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="150b9-126">El desarrollador de la extensión debe determinar cómo resolver conflictos de funciones, o propiedades, de diferentes interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales que tienen el mismo nombre en una extensión.</span><span class="sxs-lookup"><span data-stu-id="150b9-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="150b9-127">La implementación de [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y los métodos [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deben resolver este conflicto.</span><span class="sxs-lookup"><span data-stu-id="150b9-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="150b9-128">Por ejemplo, si usa IMyInterface1:: Func1 y IMyInterface2:: Func1, donde IMyInterface1 y IMyInterface2 son interfaces **IDispatch** duales admitidas por el mismo objeto de extensión.</span><span class="sxs-lookup"><span data-stu-id="150b9-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="150b9-129">Los métodos **PrivateGetIDsOfNames** y **PrivateInvoke** deben determinar a qué Func1 se debe llamar siempre.</span><span class="sxs-lookup"><span data-stu-id="150b9-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="150b9-130">Lo mismo se aplica a los DISPID conflictivos en diferentes interfaces dobles o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="150b9-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="150b9-131">Por ejemplo, el DISPID de IMyInterface1:: Y es 2 en el archivo IMyInterface1. ODL o IMyInterface1. idl.</span><span class="sxs-lookup"><span data-stu-id="150b9-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="150b9-132">El DISPID de IMyInterface2:: X también es 2 en iMyInterface2. ODL.</span><span class="sxs-lookup"><span data-stu-id="150b9-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="150b9-133">[**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) debe devolver un DISPID único, dentro de la propia extensión, para cada, en lugar de devolver el mismo DISPID para ambos.</span><span class="sxs-lookup"><span data-stu-id="150b9-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="150b9-134">ADSI resuelve el primer problema al no admitir varias interfaces con nombres de función o propiedad en conflicto.</span><span class="sxs-lookup"><span data-stu-id="150b9-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="150b9-135">Resuelve el segundo problema agregando un único, que está en el mismo objeto de extensión, el número de la interfaz a los bits sin usar del DispId.</span><span class="sxs-lookup"><span data-stu-id="150b9-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 