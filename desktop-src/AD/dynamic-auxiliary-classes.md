---
title: Clases auxiliares dinámicas
description: De forma similar a las clases de objeto estructural y abstracto, las clases auxiliares se definen mediante un objeto classSchema en el esquema de Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Clases auxiliares dinámicas AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487451"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="22115-104">Clases auxiliares dinámicas</span><span class="sxs-lookup"><span data-stu-id="22115-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="22115-105">De forma similar a las clases de objeto estructural y abstracto, las clases auxiliares se definen mediante un objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) en el esquema de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="22115-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="22115-106">Para obtener más información, vea [clases estructurales, abstractas y auxiliares](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="22115-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="22115-107">Esta definición de esquema especifica varias características de la clase, incluidos los atributos asociados a la clase.</span><span class="sxs-lookup"><span data-stu-id="22115-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="22115-108">A diferencia de las clases estructurales, no se puede crear una instancia de una clase auxiliar como se haría con una clase estructural.</span><span class="sxs-lookup"><span data-stu-id="22115-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="22115-109">En su lugar, se usa una clase auxiliar para extender la lista de atributos que está asociada a otra clase de objeto estructural, abstract u auxiliar.</span><span class="sxs-lookup"><span data-stu-id="22115-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="22115-110">En la versión inicial de Windows 2000, Active Directory Domain Services proporcionaban compatibilidad con la vinculación estática de clases auxiliares con la definición de [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) de otra clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="22115-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="22115-111">Cuando se utiliza una clase auxiliar de esta manera, cada instancia de la clase de objeto admite los atributos de la clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="22115-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="22115-112">**Windows 2000 Server y versiones anteriores:** Active Directory Domain Services no proporciona compatibilidad con la vinculación dinámica de clases auxiliares a objetos individuales, y no solo a clases completas de objetos.</span><span class="sxs-lookup"><span data-stu-id="22115-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="22115-113">Además, las clases auxiliares que se han adjuntado a una instancia de objeto no se pueden quitar de la instancia posteriormente.</span><span class="sxs-lookup"><span data-stu-id="22115-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="22115-114">**Windows Server 2003:** Se admiten las clases auxiliares dinámicas cuando todos los controladores de dominio del bosque ejecutan Windows Server 2003 y el modo funcional del bosque es Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="22115-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="22115-115">Para obtener más información acerca de las clases auxiliares, consulte:</span><span class="sxs-lookup"><span data-stu-id="22115-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="22115-116">Clases auxiliares vinculadas dinámicamente</span><span class="sxs-lookup"><span data-stu-id="22115-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="22115-117">Clases auxiliares vinculadas estáticamente</span><span class="sxs-lookup"><span data-stu-id="22115-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="22115-118">Determinar las clases asociadas a una instancia de objeto</span><span class="sxs-lookup"><span data-stu-id="22115-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="22115-119">Agregar una clase auxiliar a una instancia de objeto</span><span class="sxs-lookup"><span data-stu-id="22115-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="22115-120">Para obtener más información acerca de los niveles funcionales del bosque, vea el tema sobre cómo Active Directory elevar los niveles funcionales de dominio y bosque en la base de conocimiento de ayuda y soporte técnico en [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .</span><span class="sxs-lookup"><span data-stu-id="22115-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 