---
title: Cómo los servidores implementan identificadores secundarios
description: Los desarrolladores de servidores pueden asignar identificadores secundarios tanto a elementos simples como a objetos accesibles. Sin embargo, el enfoque recomendado es admitir la interfaz de modelo de objetos componentes (COM) estándar IEnumVARIANT en cada objeto accesible que tenga elementos secundarios.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995427"
---
# <a name="how-servers-implement-child-ids"></a><span data-ttu-id="cbd43-104">Cómo los servidores implementan identificadores secundarios</span><span class="sxs-lookup"><span data-stu-id="cbd43-104">How Servers Implement Child IDs</span></span>

<span data-ttu-id="cbd43-105">Los desarrolladores de servidores pueden asignar identificadores secundarios tanto a elementos simples como a objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="cbd43-105">Server developers can assign child IDs to both simple elements and accessible objects.</span></span> <span data-ttu-id="cbd43-106">Sin embargo, el enfoque recomendado es admitir la interfaz de modelo de objetos componentes (COM) estándar [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en cada objeto accesible que tenga elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="cbd43-106">However, the recommended approach is to support the standard Component Object Model (COM) interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in every accessible object that has children.</span></span>

<span data-ttu-id="cbd43-107">Si implementa [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), debe:</span><span class="sxs-lookup"><span data-stu-id="cbd43-107">If you implement [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must:</span></span>

-   <span data-ttu-id="cbd43-108">Enumera todos los elementos secundarios, tanto los elementos simples como los objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="cbd43-108">Enumerate all children, both simple elements and accessible objects.</span></span> <span data-ttu-id="cbd43-109">Proporcione los identificadores secundarios de todos los elementos simples y proporcione la [**IDispatch**](idispatch-interface.md) a cada objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="cbd43-109">Provide child IDs for all simple elements and provide the [**IDispatch**](idispatch-interface.md) to each accessible object.</span></span>
-   <span data-ttu-id="cbd43-110">Para objetos accesibles, establezca el miembro **VT** de la [**variante**](variant-structure.md) en el \_ envío de VT.</span><span class="sxs-lookup"><span data-stu-id="cbd43-110">For accessible objects, set the **vt** member of the [**VARIANT**](variant-structure.md) to VT\_DISPATCH.</span></span> <span data-ttu-id="cbd43-111">El miembro **pdispVal** debe contener un puntero a la interfaz [**IDispatch**](idispatch-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd43-111">The **pdispVal** member must contain a pointer to the [**IDispatch**](idispatch-interface.md) interface.</span></span> <span data-ttu-id="cbd43-112">Tenga en cuenta que el cliente asigna y libera la **variante** .</span><span class="sxs-lookup"><span data-stu-id="cbd43-112">Note that the **VARIANT** is allocated and freed by the client.</span></span>
-   <span data-ttu-id="cbd43-113">En el caso de los elementos simples, el identificador secundario es cualquier entero positivo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cbd43-113">For simple elements, the child ID is any 32-bit positive integer.</span></span> <span data-ttu-id="cbd43-114">Tenga en cuenta que los enteros negativos y cero están reservados por Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="cbd43-114">Note that zero and negative integers are reserved by Microsoft Active Accessibility.</span></span> <span data-ttu-id="cbd43-115">Establezca el miembro **VT** de la estructura [**Variant**](variant-structure.md) en VT \_ I4 y el miembro **lVal** en el identificador secundario.</span><span class="sxs-lookup"><span data-stu-id="cbd43-115">Set the [**VARIANT**](variant-structure.md) structure **vt** member to VT\_I4 and the **lVal** member to the child ID.</span></span>

<span data-ttu-id="cbd43-116">Si no admite [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), debe asignar los identificadores secundarios y el número de elementos secundarios de cada objeto secuencialmente a partir de uno.</span><span class="sxs-lookup"><span data-stu-id="cbd43-116">If you do not support [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must assign child IDs and number the children in each object sequentially starting with one.</span></span>

<span data-ttu-id="cbd43-117">Se recomienda que los clientes usen la función de Microsoft Active Accessibility [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) en lugar de llamar directamente a la interfaz de Server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="cbd43-117">It is recommended that clients use the Microsoft Active Accessibility function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) rather than call the server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface directly.</span></span>

 

 