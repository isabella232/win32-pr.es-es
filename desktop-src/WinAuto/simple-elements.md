---
title: Elementos simples
description: Un elemento simple es un elemento de la interfaz de usuario que comparte un objeto IAccessible con otros elementos y se basa en ese objeto IAccessible (normalmente su elemento primario) para exponer sus propiedades.
ms.assetid: 3f6bd992-4e0a-4dba-b6e9-e70dca77c880
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f8cb00b19719a4a8779a61f37b079633ada40c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695458"
---
# <a name="simple-elements"></a><span data-ttu-id="82155-103">Elementos simples</span><span class="sxs-lookup"><span data-stu-id="82155-103">Simple Elements</span></span>

<span data-ttu-id="82155-104">Un *elemento simple* es un elemento de la interfaz de usuario que comparte un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con otros elementos y se basa en ese objeto **IAccessible** (normalmente su elemento primario) para exponer sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="82155-104">A *simple element* is a UI element that shares an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object with other elements and relies on that **IAccessible** object (typically its parent) to expose its properties.</span></span> <span data-ttu-id="82155-105">Para diferenciar entre los elementos que comparten un objeto **IAccessible** , el servidor asigna un identificador secundario positivo único a cada elemento simple.</span><span class="sxs-lookup"><span data-stu-id="82155-105">To differentiate between the elements sharing an **IAccessible** object, the server assigns a unique, positive child identifier to each simple element.</span></span> <span data-ttu-id="82155-106">Esta asignación se realiza en cada instancia de la interfaz, por lo que los identificadores deben ser únicos dentro de ese contexto.</span><span class="sxs-lookup"><span data-stu-id="82155-106">This assignment is done on a per-instance-of-interface basis, so the IDs must be unique within that context.</span></span> <span data-ttu-id="82155-107">Muchas implementaciones asignan estos identificadores secuencialmente, empezando por 1.</span><span class="sxs-lookup"><span data-stu-id="82155-107">Many implementations assign these IDs sequentially, beginning with 1.</span></span> <span data-ttu-id="82155-108">Este esquema no permite que los elementos simples tengan elementos secundarios propios.</span><span class="sxs-lookup"><span data-stu-id="82155-108">This scheme does not allow simple elements to have children of their own.</span></span> <span data-ttu-id="82155-109">Los elementos simples también se conocen como *elementos secundarios*.</span><span class="sxs-lookup"><span data-stu-id="82155-109">Simple elements are also known as *children*.</span></span>

<span data-ttu-id="82155-110">Para que se pueda identificar y exponer de forma única, un elemento simple requiere un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y un identificador secundario.</span><span class="sxs-lookup"><span data-stu-id="82155-110">To be uniquely identified and exposed, a simple element requires an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object and child ID.</span></span> <span data-ttu-id="82155-111">Por lo tanto, al comunicarse con un objeto **IAccessible** , los clientes deben proporcionar el identificador secundario adecuado.</span><span class="sxs-lookup"><span data-stu-id="82155-111">Therefore, when communicating with an **IAccessible** object, the clients must supply the appropriate child ID.</span></span> <span data-ttu-id="82155-112">Se puede usar un identificador especial, **CHILDID \_ Self**, para hacer referencia al objeto accesible en sí, en lugar de a uno de sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="82155-112">A special identifier, **CHILDID\_SELF**, can be used to refer to the accessible object itself, instead of one of its children.</span></span>

<span data-ttu-id="82155-113">El objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) compartido entre los elementos simples suele corresponder a un objeto primario común en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="82155-113">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object shared among simple elements often corresponds to a common parent object in the user interface.</span></span> <span data-ttu-id="82155-114">Por ejemplo, los cuadros de lista del sistema exponen un objeto accesible para el cuadro de lista global y los elementos simples para cada elemento del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="82155-114">For example, system list boxes expose an accessible object for the overall list box and simple elements for each list box item.</span></span> <span data-ttu-id="82155-115">En este caso, el objeto **IAccessible** para el cuadro de lista también es el elemento primario o contenedor de los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="82155-115">In this case, the **IAccessible** object for the list box is also the parent or container of the list items.</span></span>

<span data-ttu-id="82155-116">Para obtener más información sobre los objetos accesibles, vea [objetos accesibles](accessible-objects.md).</span><span class="sxs-lookup"><span data-stu-id="82155-116">For more information about accessible objects, see [Accessible Objects](accessible-objects.md).</span></span>

 

 




