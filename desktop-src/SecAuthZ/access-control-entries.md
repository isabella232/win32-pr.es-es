---
description: Una entrada de control de acceso (ACE) es un elemento de una lista de control de acceso (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Access Control entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fe98cf1c1c4d5fb23091a6539564ff964202cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666987"
---
# <a name="access-control-entries"></a><span data-ttu-id="7143b-103">Access Control entradas</span><span class="sxs-lookup"><span data-stu-id="7143b-103">Access Control Entries</span></span>

<span data-ttu-id="7143b-104">Una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) es un elemento de una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="7143b-104">An [*access control entry*](/windows/desktop/SecGloss/a-gly) (ACE) is an element in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span> <span data-ttu-id="7143b-105">Una ACL puede tener cero o más ACE.</span><span class="sxs-lookup"><span data-stu-id="7143b-105">An ACL can have zero or more ACEs.</span></span> <span data-ttu-id="7143b-106">Cada ACE controla o supervisa el acceso a un objeto por parte de un administrador de confianza especificado.</span><span class="sxs-lookup"><span data-stu-id="7143b-106">Each ACE controls or monitors access to an object by a specified trustee.</span></span> <span data-ttu-id="7143b-107">Para obtener información sobre cómo agregar, quitar o cambiar las ACE en las ACL de un objeto, vea [modificar las ACL de un objeto en C++](modifying-the-acls-of-an-object-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7143b-107">For information about adding, removing, or changing the ACEs in an object's ACLs, see [Modifying the ACLs of an Object in C++](modifying-the-acls-of-an-object-in-c--.md).</span></span>

<span data-ttu-id="7143b-108">Hay seis tipos de ACE, tres de los cuales son compatibles con todos los objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="7143b-108">There are six types of ACEs, three of which are supported by all securable objects.</span></span> <span data-ttu-id="7143b-109">Los otros tres tipos son [ACE específicas del objeto](object-specific-aces.md) que admiten los objetos de servicio de directorio.</span><span class="sxs-lookup"><span data-stu-id="7143b-109">The other three types are [Object-specific ACEs](object-specific-aces.md) supported by directory service objects.</span></span>

<span data-ttu-id="7143b-110">Todos los tipos de ACE contienen la siguiente información de control de acceso:</span><span class="sxs-lookup"><span data-stu-id="7143b-110">All types of ACEs contain the following access control information:</span></span>

-   <span data-ttu-id="7143b-111">[Identificador de seguridad](security-identifiers.md) (SID) que identifica el [Administrador de confianza](trustees.md) al que se aplica la ACE.</span><span class="sxs-lookup"><span data-stu-id="7143b-111">A [security identifier](security-identifiers.md) (SID) that identifies the [trustee](trustees.md) to which the ACE applies.</span></span>
-   <span data-ttu-id="7143b-112">Una [*máscara de acceso*](/windows/desktop/SecGloss/a-gly) que especifica los [derechos de acceso](access-rights-and-access-masks.md) controlados por la ACE.</span><span class="sxs-lookup"><span data-stu-id="7143b-112">An [*access mask*](/windows/desktop/SecGloss/a-gly) that specifies the [access rights](access-rights-and-access-masks.md) controlled by the ACE.</span></span>
-   <span data-ttu-id="7143b-113">Marca que indica el tipo de ACE.</span><span class="sxs-lookup"><span data-stu-id="7143b-113">A flag that indicates the type of ACE.</span></span>
-   <span data-ttu-id="7143b-114">Un conjunto de marcas de bits que determinan si los contenedores u objetos secundarios pueden heredar la ACE del objeto principal al que está adjunta la ACL.</span><span class="sxs-lookup"><span data-stu-id="7143b-114">A set of bit flags that determine whether child containers or objects can inherit the ACE from the primary object to which the ACL is attached.</span></span>

<span data-ttu-id="7143b-115">En la tabla siguiente se enumeran los tres tipos de ACE admitidos por todos los objetos protegibles.</span><span class="sxs-lookup"><span data-stu-id="7143b-115">The following table lists the three ACE types supported by all securable objects.</span></span>



| <span data-ttu-id="7143b-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="7143b-116">Type</span></span>               | <span data-ttu-id="7143b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7143b-117">Description</span></span>                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7143b-118">ACE de acceso denegado</span><span class="sxs-lookup"><span data-stu-id="7143b-118">Access-denied ACE</span></span>  | <span data-ttu-id="7143b-119">Se usa en una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) para denegar los derechos de acceso a un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="7143b-119">Used in a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) to deny access rights to a trustee.</span></span>                                       |
| <span data-ttu-id="7143b-120">ACE de acceso permitido</span><span class="sxs-lookup"><span data-stu-id="7143b-120">Access-allowed ACE</span></span> | <span data-ttu-id="7143b-121">Se usa en una DACL para permitir derechos de acceso a un administrador de confianza.</span><span class="sxs-lookup"><span data-stu-id="7143b-121">Used in a DACL to allow access rights to a trustee.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="7143b-122">ACE de auditoría del sistema</span><span class="sxs-lookup"><span data-stu-id="7143b-122">System-audit ACE</span></span>   | <span data-ttu-id="7143b-123">Se utiliza en una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL) para generar un registro de auditoría cuando el administrador de confianza intenta ejercitar los derechos de acceso especificados.</span><span class="sxs-lookup"><span data-stu-id="7143b-123">Used in a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL) to generate an audit record when the trustee attempts to exercise the specified access rights.</span></span> |



 

<span data-ttu-id="7143b-124">Para obtener una tabla de ACE específicas del objeto, vea [ACE específicas del objeto](object-specific-aces.md).</span><span class="sxs-lookup"><span data-stu-id="7143b-124">For a table of object-specific ACEs, see [Object-specific ACEs](object-specific-aces.md).</span></span>

> [!Note]  
> <span data-ttu-id="7143b-125">No se admiten las ACE de objetos de alarma del sistema actualmente.</span><span class="sxs-lookup"><span data-stu-id="7143b-125">System-alarm object ACEs are not currently supported.</span></span>

 

 

 
