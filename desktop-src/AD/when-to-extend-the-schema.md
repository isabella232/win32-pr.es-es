---
title: Cuándo extender el esquema
description: Extienda el esquema solo si ninguna clase de objeto existente cumple los requisitos de la aplicación. La extensión del esquema es una operación compleja; los cambios de esquema se replican en todos los controladores de dominio del bosque de la empresa. Tenga en cuenta esto con cuidado.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Cuándo extender el esquema AD
- esquema AD, Cuándo se debe extender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656211"
---
# <a name="when-to-extend-the-schema"></a><span data-ttu-id="d351e-107">Cuándo extender el esquema</span><span class="sxs-lookup"><span data-stu-id="d351e-107">When to Extend the Schema</span></span>

<span data-ttu-id="d351e-108">Extienda el esquema solo si ninguna clase de objeto existente cumple los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d351e-108">Extend the schema only if no existing object class fulfills the requirements of your application.</span></span> <span data-ttu-id="d351e-109">La extensión del esquema es una operación compleja; los cambios de esquema se replican en todos los controladores de dominio del bosque de la empresa.</span><span class="sxs-lookup"><span data-stu-id="d351e-109">Extending the schema is a complex operation; schema changes are replicated to every domain controller in the enterprise forest.</span></span> <span data-ttu-id="d351e-110">Tenga en cuenta esto con cuidado.</span><span class="sxs-lookup"><span data-stu-id="d351e-110">Consider this carefully.</span></span>

<span data-ttu-id="d351e-111">El esquema puede extenderse de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="d351e-111">The schema can be extended in three ways:</span></span>

-   <span data-ttu-id="d351e-112">Derivar una nueva subclase de una clase existente: la subclase tiene todos los atributos de la superclase y cualquier atributo que especifique.</span><span class="sxs-lookup"><span data-stu-id="d351e-112">Derive a new subclass from an existing class - the subclass has all of the attributes of the superclass and any attributes you specify.</span></span> <span data-ttu-id="d351e-113">Derivar de una clase existente:</span><span class="sxs-lookup"><span data-stu-id="d351e-113">Derive from an existing class:</span></span>
    -   <span data-ttu-id="d351e-114">Cuando la clase existente requiere atributos adicionales, pero de lo contrario es aceptable.</span><span class="sxs-lookup"><span data-stu-id="d351e-114">When the existing class requires additional attributes, but otherwise is acceptable.</span></span>
    -   <span data-ttu-id="d351e-115">Cuando la capacidad de transformar objetos existentes de la clase en una nueva clase no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="d351e-115">When the ability to transform existing objects of the class into a new class is not required.</span></span> <span data-ttu-id="d351e-116">No es posible agregar una subclase a un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="d351e-116">It is not possible to add a subclass to an existing object.</span></span>
    -   <span data-ttu-id="d351e-117">Usar el complemento Administrador de directorios existente para administrar los atributos extendidos de los objetos.</span><span class="sxs-lookup"><span data-stu-id="d351e-117">To use the existing Directory Manager snap-in to manage the extended attributes of the objects.</span></span>
-   <span data-ttu-id="d351e-118">Agregue atributos a una clase existente y/o agregue objetos primarios para la clase.</span><span class="sxs-lookup"><span data-stu-id="d351e-118">Add attributes to an existing class and/or add parent objects for the class.</span></span> <span data-ttu-id="d351e-119">Al agregar varios atributos, realice esta operación de una manera estructurada definiendo una clase auxiliar y agregando esa clase auxiliar a la clase existente.</span><span class="sxs-lookup"><span data-stu-id="d351e-119">When adding multiple attributes, perform this operation in a structured manner by defining an auxiliary class and adding that auxiliary class to the existing class.</span></span>
-   <span data-ttu-id="d351e-120">La modificación de una clase existente es necesaria cuando una aplicación requiere la capacidad de extender objetos existentes de la clase.</span><span class="sxs-lookup"><span data-stu-id="d351e-120">Modification of an existing class is required when an application requires the ability to extend existing objects of the class.</span></span> <span data-ttu-id="d351e-121">Por ejemplo, para agregar datos específicos de la aplicación al objeto de usuario, extienda normalmente el usuario de clase, ya que debe administrar los usuarios existentes y no solo los usuarios especiales creados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d351e-121">For example, to add application-specific data to the User object, extend the class User normally, because you must handle existing Users and not just special Users created by your application.</span></span>
-   <span data-ttu-id="d351e-122">Cree una nueva clase con los atributos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d351e-122">Create a new class with the required attributes.</span></span> <span data-ttu-id="d351e-123">Cree una nueva clase; es decir, una clase derivada de "Top" cuando ninguna clase existente cumple los requisitos operativos.</span><span class="sxs-lookup"><span data-stu-id="d351e-123">Create a new class; that is, a class derived from "Top" when no existing class fulfills the operational requirements.</span></span>

<span data-ttu-id="d351e-124">Cuando se crea una subclase de una clase existente, la subclase no heredará los elementos de interfaz de usuario asociados a la clase original.</span><span class="sxs-lookup"><span data-stu-id="d351e-124">When you subclass an existing class, any user interface items associated to the original class will not be inherited by the subclass.</span></span> <span data-ttu-id="d351e-125">Por ejemplo, si se subclase de un objeto de usuario, las páginas de propiedades y los elementos de menú asociados al usuario no se heredan.</span><span class="sxs-lookup"><span data-stu-id="d351e-125">For example, if you subclass a user object, the property pages and menu items associated to user are not inherited.</span></span> <span data-ttu-id="d351e-126">Por esta razón, es preferible extender un objeto existente o crear una clase auxiliar en lugar de crear una subclase.</span><span class="sxs-lookup"><span data-stu-id="d351e-126">For this reason, it is preferable to extend an existing object or create an auxiliary class rather than create a subclass.</span></span>

<span data-ttu-id="d351e-127">Tanto si crea subclases de una clase existente como si modifica una clase existente, querrá extender herramientas como el complemento usuarios y equipos de Active Directory para administrar los atributos extendidos de los objetos.</span><span class="sxs-lookup"><span data-stu-id="d351e-127">Whether you subclass an existing class or modify an existing class, you will want to extend tools such as the Active Directory Users and Computers snap-in to manage the extended attributes of the objects.</span></span> <span data-ttu-id="d351e-128">Para obtener más información, consulte [extensión de la interfaz de usuario para objetos de directorio](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d351e-128">For more information, see [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

 

 




