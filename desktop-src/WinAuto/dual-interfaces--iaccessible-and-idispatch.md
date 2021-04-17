---
title: Interfaces duals IAccessible y IDispatch
description: Los desarrolladores de servidores deben proporcionar la interfaz de modelo de objetos componentes (COM) estándar IDispatch para sus objetos accesibles.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704967"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a><span data-ttu-id="f9dae-103">Interfaces duales: IAccessible y IDispatch</span><span class="sxs-lookup"><span data-stu-id="f9dae-103">Dual Interfaces: IAccessible and IDispatch</span></span>

<span data-ttu-id="f9dae-104">Los desarrolladores de servidores deben proporcionar la interfaz de modelo de objetos componentes (COM) estándar [**IDispatch**](idispatch-interface.md) para sus objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="f9dae-104">Server developers must provide the standard Component Object Model (COM) interface [**IDispatch**](idispatch-interface.md) for their accessible objects.</span></span> <span data-ttu-id="f9dae-105">La interfaz IDispatch permite a las aplicaciones cliente escritas en Microsoft Visual Basic y varios lenguajes de scripting usar los métodos y las propiedades expuestas por [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="f9dae-105">The IDispatch interface allows client applications written in Microsoft Visual Basic and various scripting languages to use the methods and properties exposed by [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="f9dae-106">Dado que un objeto accesible proporciona acceso a un objeto de forma indirecta a través de [IDispatch:: Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) o directamente con **IAccessible**, se dice que tiene una interfaz dual.</span><span class="sxs-lookup"><span data-stu-id="f9dae-106">Because an accessible object provides access to an object either indirectly through [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) or directly with **IAccessible**, it is said to have a dual interface.</span></span>

<span data-ttu-id="f9dae-107">Cuando los clientes de C/C++ obtienen un puntero de interfaz IDispatch, los clientes pueden llamar a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para intentar convertir el puntero de interfaz IDispatch en un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="f9dae-107">When C/C++ clients get back an IDispatch interface pointer, clients can call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to try converting the IDispatch interface pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="f9dae-108">Para llamar a los métodos **IAccessible** indirectamente, los clientes de C/C++ llaman a IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="f9dae-108">To call the **IAccessible** methods indirectly, C/C++ clients call IDispatch::Invoke.</span></span> <span data-ttu-id="f9dae-109">Para mejorar el rendimiento, llame a los métodos **IAccessible** para usar el objeto directamente.</span><span class="sxs-lookup"><span data-stu-id="f9dae-109">For improved performance, call the **IAccessible** methods to use the object directly.</span></span>

<span data-ttu-id="f9dae-110">Para obtener una lista de los identificadores de envío (DISPID) que **IDispatch** usa para identificar los métodos y propiedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , vea [Apéndice C: IAccessible DISPID](appendix-c--iaccessible-dispids.md).</span><span class="sxs-lookup"><span data-stu-id="f9dae-110">For a list of the dispatch IDs (DISPIDs) that **IDispatch** uses to identify the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties, see [Appendix C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md).</span></span>

> [!Note]  
> <span data-ttu-id="f9dae-111">En la versión 2,0 y posteriores de Microsoft Active Accessibility, los servidores no tienen que implementar completamente los métodos de [**IDispatch**](idispatch-interface.md) , pero simplemente pueden devolver E \_ NOTIMPL después de inicializar los parámetros out, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f9dae-111">Under version 2.0 and later of Microsoft Active Accessibility, servers do not have to fully implement the methods of [**IDispatch**](idispatch-interface.md) but can simply return E\_NOTIMPL after initializing any out parameters, as shown in the following example.</span></span>

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 