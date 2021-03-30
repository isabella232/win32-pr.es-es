---
title: Apéndice D Notas para desarrolladores de Visual Basic
description: En esta sección se proporciona información acerca de Microsoft Active Accessibility para desarrolladores de Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994172"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a><span data-ttu-id="9b27f-103">Apéndice D: notas para desarrolladores de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9b27f-103">Appendix D: Notes for Visual Basic Developers</span></span>

<span data-ttu-id="9b27f-104">En esta sección se proporciona información acerca de Microsoft Active Accessibility para desarrolladores de Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9b27f-104">This section provides information about Microsoft Active Accessibility for Microsoft Visual Basic developers.</span></span>

<span data-ttu-id="9b27f-105">Las aplicaciones escritas en Visual Basic son clientes de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="9b27f-105">Applications written in Visual Basic are Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="9b27f-106">No proporcionan información sobre los elementos de la interfaz de usuario personalizados porque no implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ni ninguna otra interfaz del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="9b27f-106">They do not provide information about their custom user interface elements because they do not implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or any other Component Object Model (COM) interface.</span></span>

<span data-ttu-id="9b27f-107">En esta documentación se usan los nombres de C/C++ para las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ; sin embargo, los nombres de Visual Basic son similares.</span><span class="sxs-lookup"><span data-stu-id="9b27f-107">This documentation uses the C/C++ names for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties; however, the Visual Basic names are similar.</span></span> <span data-ttu-id="9b27f-108">Por ejemplo, la propiedad [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) se llamaría **accName** en una aplicación Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9b27f-108">For example, the [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) property would be called **accName** in a Visual Basic application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b27f-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9b27f-109">In this section</span></span>

-   [<span data-ttu-id="9b27f-110">Notas del método Visual Basic: accName</span><span class="sxs-lookup"><span data-stu-id="9b27f-110">Visual Basic Method Notes: accName</span></span>](visual-basic-method-notes--accname.md)
-   [<span data-ttu-id="9b27f-111">Notas del método Visual Basic: accValue</span><span class="sxs-lookup"><span data-stu-id="9b27f-111">Visual Basic Method Notes: accValue</span></span>](visual-basic-method-notes--accvalue.md)
-   [<span data-ttu-id="9b27f-112">Visual Basic programas de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b27f-112">Visual Basic Sample Programs</span></span>](visual-basic-sample-programs.md)

 

 




