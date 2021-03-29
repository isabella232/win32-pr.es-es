---
title: Interfaces de esquema
description: Interfaces de esquema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfaces de esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993845"
---
# <a name="schema-interfaces"></a><span data-ttu-id="41e8f-104">Interfaces de esquema</span><span class="sxs-lookup"><span data-stu-id="41e8f-104">Schema Interfaces</span></span>

<span data-ttu-id="41e8f-105">El contenedor de esquemas contiene un conjunto de definiciones de esquema que están adjuntas a parte del árbol de espacios de nombres del proveedor.</span><span class="sxs-lookup"><span data-stu-id="41e8f-105">The schema container contains a set of schema definitions that are attached to part of the namespace tree of the provider.</span></span> <span data-ttu-id="41e8f-106">Normalmente, cada instancia de un espacio de nombres tiene su propio esquema.</span><span class="sxs-lookup"><span data-stu-id="41e8f-106">Typically, each instance of a namespace has its own schema.</span></span> <span data-ttu-id="41e8f-107">Por ejemplo, en la siguiente ilustración, el proveedor de ejemplo ADSI define un contenedor de esquema en cada uno de los nodos raíz "Seattle" y "Toronto".</span><span class="sxs-lookup"><span data-stu-id="41e8f-107">For example, in the following figure, the ADSI example provider defines a schema container in each of the root nodes "Seattle" and "Toronto".</span></span>

![contención de esquemas](images/schemacont.png)

<span data-ttu-id="41e8f-109">Para crear una implementación de ADSI para un proveedor, debe proporcionar objetos de administración de esquema que reflejen el espacio de nombres subyacente del proveedor y que admitan las interfaces de esquema ADSI.</span><span class="sxs-lookup"><span data-stu-id="41e8f-109">To create an ADSI implementation for a provider, you need to supply schema management objects that reflect the underlying namespace of the provider and which support ADSI schema interfaces.</span></span> <span data-ttu-id="41e8f-110">A continuación se muestra una lista de las interfaces de esquema ADSI, que se encuentran en el contenedor de esquemas.</span><span class="sxs-lookup"><span data-stu-id="41e8f-110">The following is a list of the ADSI schema interfaces, which are contained in the schema container.</span></span>

-   <span data-ttu-id="41e8f-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) representa las clases de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="41e8f-111">[**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) represents directory service classes.</span></span>
-   <span data-ttu-id="41e8f-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) representa las propiedades del servicio de directorio que tienen uno o varios valores.</span><span class="sxs-lookup"><span data-stu-id="41e8f-112">[**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) represents directory service properties that have single or multiple values.</span></span>
-   <span data-ttu-id="41e8f-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) representa el tipo de variante única.</span><span class="sxs-lookup"><span data-stu-id="41e8f-113">[**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) represents the single VARIANT type.</span></span>

<span data-ttu-id="41e8f-114">Las interfaces definidas por ADSI pueden admitir propiedades específicas y sintaxis para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="41e8f-114">Interfaces defined by ADSI can support specific properties and syntaxes for your provider.</span></span> <span data-ttu-id="41e8f-115">Los proveedores pueden elegir ampliar una definición de ADSI mediante los métodos que crean y tienen acceso a las propiedades; por ejemplo, puede usar los métodos de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span><span class="sxs-lookup"><span data-stu-id="41e8f-115">Providers can choose to extend an ADSI definition by using the methods that create and access properties, for example, you can use the methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex).</span></span> <span data-ttu-id="41e8f-116">Los proveedores también pueden admitir propiedades adicionales mediante interfaces adicionales.</span><span class="sxs-lookup"><span data-stu-id="41e8f-116">Providers can also support additional properties through additional interfaces.</span></span> <span data-ttu-id="41e8f-117">Para obtener una lista completa de las interfaces ADSI, consulte [interfaces ADSI](adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="41e8f-117">For a complete list of ADSI interfaces, see [ADSI Interfaces](adsi-interfaces.md).</span></span>

<span data-ttu-id="41e8f-118">Un componente de proveedor ADSI con un espacio de nombres complejo podría permitir que existan varios esquemas en una instancia de espacio de nombres, cada uno en una parte diferente del árbol.</span><span class="sxs-lookup"><span data-stu-id="41e8f-118">An ADSI provider component with a complex namespace might allow multiple schemas to exist in a namespace instance, each at a different part of the tree.</span></span> <span data-ttu-id="41e8f-119">Sin embargo, la propiedad [**IADs:: Schema**](iads-property-methods.md) de un objeto siempre nombra su propia definición de esquema.</span><span class="sxs-lookup"><span data-stu-id="41e8f-119">The [**IADs::Schema**](iads-property-methods.md) property of an object, however, always names its own schema definition.</span></span>

 

 




