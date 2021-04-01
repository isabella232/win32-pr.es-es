---
description: Las ACE específicas del objeto son compatibles con los objetos del servicio de directorio (DS). Una ACE específica del objeto contiene un par de GUID que amplían las formas en que la ACE puede proteger un objeto.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: ACE específicas del objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082997"
---
# <a name="object-specific-aces"></a><span data-ttu-id="ec524-104">ACE específicas del objeto</span><span class="sxs-lookup"><span data-stu-id="ec524-104">Object-specific ACEs</span></span>

<span data-ttu-id="ec524-105">Las [*ACE*](/windows/desktop/SecGloss/a-gly) específicas del objeto son compatibles con los objetos del servicio de directorio (DS).</span><span class="sxs-lookup"><span data-stu-id="ec524-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="ec524-106">Una ACE específica del objeto contiene un par de GUID que amplían las formas en que la ACE puede proteger un objeto.</span><span class="sxs-lookup"><span data-stu-id="ec524-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec524-107">GUID</span><span class="sxs-lookup"><span data-stu-id="ec524-107">GUID</span></span></th>
<th><span data-ttu-id="ec524-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec524-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec524-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="ec524-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="ec524-110">Identifica una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ec524-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="ec524-111">Tipo de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="ec524-111">A type of child object.</span></span> <span data-ttu-id="ec524-112">La ACE controla la derecha para crear un tipo especificado de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="ec524-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="ec524-113">Para obtener más información, vea <a href="controlling-child-object-creation-in-c--.md">controlar la creación de objetos secundarios en C++</a>.</span><span class="sxs-lookup"><span data-stu-id="ec524-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="ec524-114">Una propiedad o un conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ec524-114">A property set or property.</span></span> <span data-ttu-id="ec524-115">La ACE controla el derecho para leer o escribir la propiedad o el conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ec524-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="ec524-116">Para obtener más información, vea <a href="aces-to-control-access-to-an-object-s-properties.md">ACE para controlar el acceso a las propiedades de un objeto</a>.</span><span class="sxs-lookup"><span data-stu-id="ec524-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="ec524-117">Un derecho extendido.</span><span class="sxs-lookup"><span data-stu-id="ec524-117">An extended right.</span></span> <span data-ttu-id="ec524-118">La ACE controla el derecho para realizar la operación asociada con el derecho extendido.</span><span class="sxs-lookup"><span data-stu-id="ec524-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="ec524-119">Una escritura validada.</span><span class="sxs-lookup"><span data-stu-id="ec524-119">A validated write.</span></span> <span data-ttu-id="ec524-120">La ACE controla el derecho para realizar ciertas operaciones de escritura.</span><span class="sxs-lookup"><span data-stu-id="ec524-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="ec524-121">Estos permisos de escritura validados, que se definen y exponen en el editor ACL, proporcionan permisos para la escritura validada de propiedades en lugar de escrituras de bajo nivel no comprobadas de cualquier valor a una propiedad que se concede con un &quot; permiso de propiedad de escritura &quot; .</span><span class="sxs-lookup"><span data-stu-id="ec524-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec524-122"><strong>InheritedObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="ec524-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="ec524-123">Indica el tipo de objeto secundario que puede heredar la ACE.</span><span class="sxs-lookup"><span data-stu-id="ec524-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="ec524-124">La herencia también se controla mediante los marcadores de herencia en el <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, así como cualquier protección contra la herencia colocada en los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ec524-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="ec524-125">Para obtener más información, vea <a href="ace-inheritance.md">herencia de ACE</a>.</span><span class="sxs-lookup"><span data-stu-id="ec524-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ec524-126">Se admiten tres tipos de ACE específicas del objeto.</span><span class="sxs-lookup"><span data-stu-id="ec524-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="ec524-127">No se admiten las ACE de objetos de alarma del sistema actualmente.</span><span class="sxs-lookup"><span data-stu-id="ec524-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="ec524-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec524-128">Type</span></span>                      | <span data-ttu-id="ec524-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec524-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec524-130">ACE de objeto de acceso denegado</span><span class="sxs-lookup"><span data-stu-id="ec524-130">Access-denied object ACE</span></span>  | <span data-ttu-id="ec524-131">Se usa en una DACL para denegar el acceso de un administrador de confianza a una propiedad o un conjunto de propiedades en el objeto, o para limitar la herencia de ACE a un tipo especificado de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="ec524-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="ec524-132">Utiliza la estructura [**ACE de objeto de acceso \_ denegado \_ \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="ec524-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="ec524-133">ACE de objeto con permiso de acceso</span><span class="sxs-lookup"><span data-stu-id="ec524-133">Access-allowed object ACE</span></span> | <span data-ttu-id="ec524-134">Se usa en una DACL para permitir que un administrador de confianza tenga acceso a una propiedad o un conjunto de propiedades en el objeto, o para limitar la herencia de ACE a un tipo especificado de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="ec524-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="ec524-135">Utiliza la [**estructura \_ \_ \_ ACE del objeto de acceso permitido**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="ec524-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="ec524-136">ACE del objeto de auditoría del sistema</span><span class="sxs-lookup"><span data-stu-id="ec524-136">System-audit object ACE</span></span>   | <span data-ttu-id="ec524-137">Se usa en una SACL para registrar los intentos de un administrador de confianza de obtener acceso a una propiedad o un conjunto de propiedades en el objeto, o para limitar la herencia de ACE a un tipo especificado de objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="ec524-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="ec524-138">Utiliza la [**estructura \_ \_ \_ ACE del objeto de auditoría del sistema**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="ec524-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="ec524-139">Todas las ACL que contengan una ACE específica del objeto deben usar la revisión de la ACL de revisión \_ \_ DS.</span><span class="sxs-lookup"><span data-stu-id="ec524-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 
