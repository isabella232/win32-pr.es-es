---
title: Controlar el acceso a los objetos y sus propiedades
description: Para controlar el acceso a los objetos de la aplicación, trabaje con el descriptor de seguridad del objeto y, en concreto, con la lista de control de acceso discrecional (DACL) y su lista de entradas de control de acceso (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- objeto AD, controlar el acceso a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268229"
---
# <a name="controlling-access-to-objects-and-their-properties"></a><span data-ttu-id="9cef5-104">Controlar el acceso a los objetos y sus propiedades</span><span class="sxs-lookup"><span data-stu-id="9cef5-104">Controlling Access to Objects and Their Properties</span></span>

<span data-ttu-id="9cef5-105">Para controlar el acceso a los objetos de la aplicación, trabaje con el descriptor de seguridad del objeto y, en concreto, con la lista de control de acceso discrecional (DACL) y su lista de entradas de control de acceso (ACE).</span><span class="sxs-lookup"><span data-stu-id="9cef5-105">To control access to application objects, work with the object security descriptor, and specifically, with the discretionary access-control list (DACL) and its list of access-control entries (ACEs).</span></span>

<span data-ttu-id="9cef5-106">Cuando se crea un objeto, recibe un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9cef5-106">When an object is created, it receives a security descriptor.</span></span> <span data-ttu-id="9cef5-107">Para obtener más información y una descripción de las reglas que utiliza el sistema para crear la DACL para un nuevo objeto, consulte [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9cef5-107">For more information, and a description of the rules that the system uses to create the DACL for a new object, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span> <span data-ttu-id="9cef5-108">Estas reglas muestran que puede:</span><span class="sxs-lookup"><span data-stu-id="9cef5-108">These rules reveal that you can:</span></span>

-   <span data-ttu-id="9cef5-109">Cree un nuevo descriptor de seguridad y asócielo al objeto en el momento de su creación.</span><span class="sxs-lookup"><span data-stu-id="9cef5-109">Create a new security descriptor and attach it to the object at creation time.</span></span> <span data-ttu-id="9cef5-110">Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto de directorio](creating-a-security-descriptor-for-a-new-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="9cef5-110">For more information, see [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).</span></span>
-   <span data-ttu-id="9cef5-111">Aplique una ACE heredable, en cualquier punto de la jerarquía de directorios, de modo que los objetos de una ACE hereden el árbol.</span><span class="sxs-lookup"><span data-stu-id="9cef5-111">Apply an inheritable ACE, at any point in the directory hierarchy, such that an ACE is inherited by objects down the tree.</span></span> <span data-ttu-id="9cef5-112">Un objeto puede heredar una ACE de su contenedor primario.</span><span class="sxs-lookup"><span data-stu-id="9cef5-112">An object can inherit an ACE from its parent container.</span></span> <span data-ttu-id="9cef5-113">Para obtener más información, vea [herencia y delegación de la administración](inheritance-and-delegation-of-administration.md).</span><span class="sxs-lookup"><span data-stu-id="9cef5-113">For more information, see [Inheritance and Delegation of Administration](inheritance-and-delegation-of-administration.md).</span></span>
-   <span data-ttu-id="9cef5-114">Especifique una ACE en la DACL predeterminada en el esquema, si tiene los derechos de acceso necesarios.</span><span class="sxs-lookup"><span data-stu-id="9cef5-114">Specify an ACE in the default DACL in the schema, if you have the necessary access rights.</span></span> <span data-ttu-id="9cef5-115">Cada definición de clase de objeto del esquema incluye un descriptor de seguridad predeterminado que puede tener una DACL predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9cef5-115">Every object class definition in the schema includes a default security descriptor that can have a default DACL.</span></span> <span data-ttu-id="9cef5-116">Para obtener más información, vea [descriptor de seguridad predeterminado](default-security-descriptor.md).</span><span class="sxs-lookup"><span data-stu-id="9cef5-116">For more information, see [Default Security Descriptor](default-security-descriptor.md).</span></span>

<span data-ttu-id="9cef5-117">Además, se puede modificar la DACL de un objeto existente.</span><span class="sxs-lookup"><span data-stu-id="9cef5-117">In addition the DACL of an existing object can be modified.</span></span> <span data-ttu-id="9cef5-118">Puede:</span><span class="sxs-lookup"><span data-stu-id="9cef5-118">You can:</span></span>

-   <span data-ttu-id="9cef5-119">Reemplace la DACL por otra nueva.</span><span class="sxs-lookup"><span data-stu-id="9cef5-119">Replace the DACL with a new one.</span></span>
-   <span data-ttu-id="9cef5-120">Leer la DACL existente, modificarla y aplicar la DACL modificada.</span><span class="sxs-lookup"><span data-stu-id="9cef5-120">Read the existing DACL, modify it, and apply the modified DACL.</span></span> <span data-ttu-id="9cef5-121">Para obtener más información, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="9cef5-121">For more information, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="9cef5-122">En la lista siguiente se describe la función más importante de una ACE en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9cef5-122">The following list describes the most important function of an ACE in Active Directory Domain Services.</span></span> <span data-ttu-id="9cef5-123">Con una ACE, puede:</span><span class="sxs-lookup"><span data-stu-id="9cef5-123">With an ACE, you can:</span></span>

-   <span data-ttu-id="9cef5-124">Controlar quién puede realizar operaciones concretas en un objeto.</span><span class="sxs-lookup"><span data-stu-id="9cef5-124">Control who can perform specific operations on an object.</span></span>
-   <span data-ttu-id="9cef5-125">Controla quién tiene acceso a una propiedad concreta o a un conjunto de propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="9cef5-125">Control who has access to a specific property, or set of properties, of an object.</span></span>
-   <span data-ttu-id="9cef5-126">Controlar quién puede crear objetos secundarios en un contenedor, incluido quién puede crear un tipo específico de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="9cef5-126">Control who can create child objects in a container, including who can create a specific type of child object.</span></span>
-   <span data-ttu-id="9cef5-127">Definir derechos de acceso de control privado para un tipo de objeto y controlar quién puede realizar las operaciones protegidas por los derechos privados.</span><span class="sxs-lookup"><span data-stu-id="9cef5-127">Define private control-access rights for an object type and control who can perform the operations protected by the private rights.</span></span>
-   <span data-ttu-id="9cef5-128">Aplique una ACE a un objeto contenedor en la raíz de un subárbol de directorio, de modo que todos los objetos secundarios del árbol puedan heredar automáticamente las protecciones.</span><span class="sxs-lookup"><span data-stu-id="9cef5-128">Apply an ACE to a container object at the root of a directory subtree, such that the protections can be inherited automatically by all child objects down the tree.</span></span>
-   <span data-ttu-id="9cef5-129">Aplicar una ACE heredada automáticamente por un tipo específico de objeto secundario en un subárbol.</span><span class="sxs-lookup"><span data-stu-id="9cef5-129">Apply an ACE that is inherited automatically by a specific type of child object in a subtree.</span></span>
-   <span data-ttu-id="9cef5-130">Cree una ACE que conceda derechos a un grupo de seguridad, en lugar de a un solo usuario.</span><span class="sxs-lookup"><span data-stu-id="9cef5-130">Create an ACE that grants rights to a security group, rather than to a single user.</span></span>
-   <span data-ttu-id="9cef5-131">Aplique una ACE a directiva de grupo objetos para controlar las cuentas y los equipos afectados por la Directiva.</span><span class="sxs-lookup"><span data-stu-id="9cef5-131">Apply an ACE to Group Policy Objects to control the accounts and computers affected by the policy.</span></span>

 

 




