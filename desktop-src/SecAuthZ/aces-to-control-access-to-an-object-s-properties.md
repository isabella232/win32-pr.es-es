---
description: ACE para controlar el acceso a las propiedades de los objetos
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: ACE para controlar el acceso a las propiedades de los objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1068ceb994e72deedcb795586ddf712fe9c1893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276498"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a><span data-ttu-id="d37a3-103">ACE para controlar el acceso a las propiedades de un objeto</span><span class="sxs-lookup"><span data-stu-id="d37a3-103">ACEs to Control Access to an Object's Properties</span></span>

<span data-ttu-id="d37a3-104">La [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) de un objeto de servicio de directorio (DS) puede contener una jerarquía de [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE), como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="d37a3-104">The [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of a directory service (DS) object can contain a hierarchy of [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), as follows:</span></span>

1.  <span data-ttu-id="d37a3-105">ACE que protegen el propio objeto</span><span class="sxs-lookup"><span data-stu-id="d37a3-105">ACEs that protect the object itself</span></span>
2.  <span data-ttu-id="d37a3-106">[ACE específicas del objeto](object-specific-aces.md) que protegen un conjunto de propiedades especificado en el objeto.</span><span class="sxs-lookup"><span data-stu-id="d37a3-106">[Object-specific ACEs](object-specific-aces.md) that protect a specified property set on the object</span></span>
3.  <span data-ttu-id="d37a3-107">ACE específicas del objeto que protegen una propiedad especificada en el objeto.</span><span class="sxs-lookup"><span data-stu-id="d37a3-107">Object-specific ACEs that protect a specified property on the object</span></span>

<span data-ttu-id="d37a3-108">Dentro de esta jerarquía, los derechos concedidos o denegados en un nivel superior se aplican también a los niveles inferiores.</span><span class="sxs-lookup"><span data-stu-id="d37a3-108">Within this hierarchy, the rights granted or denied at a higher level apply also to the lower levels.</span></span> <span data-ttu-id="d37a3-109">Por ejemplo, si una ACE específica del objeto en un conjunto de propiedades permite que un administrador de confianza sea el derecho \_ \_ DS \_ Read \_ prop Right, el administrador de confianza tendrá acceso de lectura implícito a todas las propiedades de ese conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d37a3-109">For example, if an object-specific ACE on a property set allows a trustee the ADS\_RIGHT\_DS\_READ\_PROP right, the trustee has implicit read access to all of the properties of that property set.</span></span> <span data-ttu-id="d37a3-110">Del mismo modo, una ACE en el propio objeto que permite \_ a ADS tener el derecho de \_ \_ lectura de DS read \_ prop proporciona acceso de lectura a todas las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="d37a3-110">Similarly, an ACE on the object itself that allows ADS\_RIGHT\_DS\_READ\_PROP access gives the trustee read access to all of the object's properties.</span></span>

<span data-ttu-id="d37a3-111">En la ilustración siguiente se muestra el árbol de un objeto DS hipotético y sus propiedades y conjuntos de propiedades.</span><span class="sxs-lookup"><span data-stu-id="d37a3-111">The following illustration shows the tree of a hypothetical DS object and its property sets and properties.</span></span>

![jerarquía de objetos del servicio de directorio](images/accctrl2.png)

<span data-ttu-id="d37a3-113">Supongamos que desea permitir el siguiente acceso a las propiedades de este objeto DS:</span><span class="sxs-lookup"><span data-stu-id="d37a3-113">Suppose you want to allow the following access to the properties of this DS object:</span></span>

-   <span data-ttu-id="d37a3-114">Permitir al grupo un permiso de lectura y escritura para todas las propiedades del objeto</span><span class="sxs-lookup"><span data-stu-id="d37a3-114">Allow Group A read/write permission to all of the object's properties</span></span>
-   <span data-ttu-id="d37a3-115">Permitir a todos los demás permisos de lectura y escritura para todas las propiedades excepto la propiedad D</span><span class="sxs-lookup"><span data-stu-id="d37a3-115">Allow everyone else read/write permission to all properties except Property D</span></span>

<span data-ttu-id="d37a3-116">Para ello, establezca las ACE en la DACL del objeto como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d37a3-116">To do this, set the ACEs in the object's DACL as shown in the following table.</span></span>



| <span data-ttu-id="d37a3-117">Confianza</span><span class="sxs-lookup"><span data-stu-id="d37a3-117">Trustee</span></span>  | <span data-ttu-id="d37a3-118">GUID del objeto</span><span class="sxs-lookup"><span data-stu-id="d37a3-118">Object GUID</span></span>    | <span data-ttu-id="d37a3-119">Tipo de ACE</span><span class="sxs-lookup"><span data-stu-id="d37a3-119">ACE type</span></span>                  | <span data-ttu-id="d37a3-120">Derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="d37a3-120">Access rights</span></span>                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| <span data-ttu-id="d37a3-121">Grupo A</span><span class="sxs-lookup"><span data-stu-id="d37a3-121">Group A</span></span>  | <span data-ttu-id="d37a3-122">None</span><span class="sxs-lookup"><span data-stu-id="d37a3-122">None</span></span>           | <span data-ttu-id="d37a3-123">ACE de acceso permitido</span><span class="sxs-lookup"><span data-stu-id="d37a3-123">Access-allowed ACE</span></span>        | <span data-ttu-id="d37a3-124">ADS \_ right \_ DS \_ leer \_ prop \| ADS \_ right \_ DS \_ Write \_ prop</span><span class="sxs-lookup"><span data-stu-id="d37a3-124">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="d37a3-125">Todos</span><span class="sxs-lookup"><span data-stu-id="d37a3-125">Everyone</span></span> | <span data-ttu-id="d37a3-126">Conjunto de propiedades 1</span><span class="sxs-lookup"><span data-stu-id="d37a3-126">Property Set 1</span></span> | <span data-ttu-id="d37a3-127">ACE de objeto con permiso de acceso</span><span class="sxs-lookup"><span data-stu-id="d37a3-127">Access-allowed object ACE</span></span> | <span data-ttu-id="d37a3-128">ADS \_ right \_ DS \_ leer \_ prop \| ADS \_ right \_ DS \_ Write \_ prop</span><span class="sxs-lookup"><span data-stu-id="d37a3-128">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |
| <span data-ttu-id="d37a3-129">Todos</span><span class="sxs-lookup"><span data-stu-id="d37a3-129">Everyone</span></span> | <span data-ttu-id="d37a3-130">Propiedad C</span><span class="sxs-lookup"><span data-stu-id="d37a3-130">Property C</span></span>     | <span data-ttu-id="d37a3-131">ACE de objeto con permiso de acceso</span><span class="sxs-lookup"><span data-stu-id="d37a3-131">Access-allowed object ACE</span></span> | <span data-ttu-id="d37a3-132">ADS \_ right \_ DS \_ leer \_ prop \| ADS \_ right \_ DS \_ Write \_ prop</span><span class="sxs-lookup"><span data-stu-id="d37a3-132">ADS\_RIGHT\_DS\_READ\_PROP \| ADS\_RIGHT\_DS\_WRITE\_PROP</span></span> |



 

<span data-ttu-id="d37a3-133">La ACE del grupo A no tiene un GUID de objeto, lo que significa que permite el acceso a todas las propiedades del objeto.</span><span class="sxs-lookup"><span data-stu-id="d37a3-133">The ACE for Group A does not have an object GUID, which means that it allows access to all the object's properties.</span></span> <span data-ttu-id="d37a3-134">La ACE específica del objeto para el conjunto de propiedades 1 permite que todos los usuarios tengan acceso a las propiedades a y B. La otra ACE específica del objeto permite que todos los usuarios tengan acceso a la propiedad C. tenga en cuenta que aunque esta DACL no tiene ninguna ACE de acceso denegado, deniega implícitamente el acceso de la propiedad D a todos los usuarios excepto el grupo A.</span><span class="sxs-lookup"><span data-stu-id="d37a3-134">The object-specific ACE for Property Set 1 allows everyone access to Properties A and B. The other object-specific ACE allows everyone access to Property C. Note that although this DACL does not have any access-denied ACEs, it implicitly denies Property D access to everyone except Group A.</span></span>

<span data-ttu-id="d37a3-135">Cuando un usuario intenta tener acceso a la propiedad de un objeto, el sistema comprueba las ACE, en orden, hasta que el acceso solicitado se concede, se deniega explícitamente o no hay más ACE, en cuyo caso se deniega implícitamente el acceso.</span><span class="sxs-lookup"><span data-stu-id="d37a3-135">When a user tries to access an object's property, the system checks the ACEs, in order, until the requested access is explicitly granted, denied, or there are no more ACEs, in which case, access is implicitly denied.</span></span>

<span data-ttu-id="d37a3-136">El sistema evalúa:</span><span class="sxs-lookup"><span data-stu-id="d37a3-136">The system evaluates:</span></span>

-   <span data-ttu-id="d37a3-137">ACE que se aplican al propio objeto</span><span class="sxs-lookup"><span data-stu-id="d37a3-137">ACEs that apply to the object itself</span></span>
-   <span data-ttu-id="d37a3-138">ACE específicas del objeto que se aplican al conjunto de propiedades que contiene la propiedad a la que se obtiene acceso.</span><span class="sxs-lookup"><span data-stu-id="d37a3-138">Object-specific ACEs that apply to the property set that contains the property being accessed</span></span>
-   <span data-ttu-id="d37a3-139">ACE específicas del objeto que se aplican a la propiedad a la que se obtiene acceso.</span><span class="sxs-lookup"><span data-stu-id="d37a3-139">Object-specific ACEs that apply to the property being accessed</span></span>

<span data-ttu-id="d37a3-140">El sistema omite las ACE específicas del objeto que se aplican a otros conjuntos de propiedades o propiedades.</span><span class="sxs-lookup"><span data-stu-id="d37a3-140">The system ignores object-specific ACEs that apply to other property sets or properties.</span></span>

 

 
