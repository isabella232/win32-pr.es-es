---
title: Cómo los clientes obtienen los identificadores secundarios
description: Cómo los clientes obtienen los identificadores secundarios
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791943"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="151e2-103">Cómo los clientes obtienen los identificadores secundarios</span><span class="sxs-lookup"><span data-stu-id="151e2-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="151e2-104">Los desarrolladores de cliente pueden obtener el identificador secundario de un objeto de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="151e2-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="151e2-105">Llame a [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span><span class="sxs-lookup"><span data-stu-id="151e2-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="151e2-106">Esta función recupera una matriz de estructuras [**variantes**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="151e2-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="151e2-107">Consulte el objeto para ver si es compatible con la interfaz [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="151e2-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="151e2-108">Si está presente, use [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) para obtener los identificadores secundarios.</span><span class="sxs-lookup"><span data-stu-id="151e2-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="151e2-109">Recopile los identificadores secundarios llamando al método [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="151e2-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="151e2-110">Es responsabilidad del cliente liberar la memoria que se usa para las estructuras de [**variantes**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="151e2-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="151e2-111">Los clientes también deben llamar a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en cualquier interfaz [**IDispatch**](idispatch-interface.md) que se devuelva.</span><span class="sxs-lookup"><span data-stu-id="151e2-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 