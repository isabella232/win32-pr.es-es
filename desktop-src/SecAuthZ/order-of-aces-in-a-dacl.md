---
description: Cuando un proceso intenta tener acceso a un objeto protegible, el sistema recorre las entradas de control de acceso (ACE) de la lista de control de acceso discrecional (DACL) de objetos hasta que encuentra ACE que permiten o deniegan el acceso solicitado.
ms.assetid: fccf043e-e769-4f3f-b18c-252be20190d8
title: Orden de ACE en una DACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc45d6fd286bb06bd4311a8a02010c68832735ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667921"
---
# <a name="order-of-aces-in-a-dacl"></a><span data-ttu-id="974d7-103">Orden de ACE en una DACL</span><span class="sxs-lookup"><span data-stu-id="974d7-103">Order of ACEs in a DACL</span></span>

<span data-ttu-id="974d7-104">Cuando un [*proceso*](/windows/desktop/SecGloss/p-gly) intenta tener acceso a un objeto protegible, el sistema recorre las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de la lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del objeto hasta que encuentra ACE que permiten o deniegan el acceso solicitado.</span><span class="sxs-lookup"><span data-stu-id="974d7-104">When a [*process*](/windows/desktop/SecGloss/p-gly) tries to access a securable object, the system steps through the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) until it finds ACEs that allow or deny the requested access.</span></span> <span data-ttu-id="974d7-105">Los derechos de acceso que una DACL permite a un usuario pueden variar en función del orden de las ACE en la DACL.</span><span class="sxs-lookup"><span data-stu-id="974d7-105">The access rights that a DACL allows a user could vary depending on the order of ACEs in the DACL.</span></span> <span data-ttu-id="974d7-106">Por lo tanto, el sistema operativo Windows XP define un orden preferido para las ACE en la DACL de un objeto protegible.</span><span class="sxs-lookup"><span data-stu-id="974d7-106">Consequently, the Windows XP operating system defines a preferred order for ACEs in the DACL of a securable object.</span></span> <span data-ttu-id="974d7-107">El orden preferido proporciona un marco de trabajo sencillo que garantiza que una ACE de acceso denegado realmente deniega el acceso.</span><span class="sxs-lookup"><span data-stu-id="974d7-107">The preferred order provides a simple framework that ensures that an access-denied ACE actually denies access.</span></span> <span data-ttu-id="974d7-108">Para obtener más información sobre el algoritmo del sistema para comprobar el acceso, vea [Cómo controlan el acceso a un objeto las DACL](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="974d7-108">For more information about the system's algorithm for checking access, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="974d7-109">En Windows Server 2003 y Windows XP, el orden adecuado de las ACE es complicado por la introducción de ACE específicas del objeto y la herencia automática.</span><span class="sxs-lookup"><span data-stu-id="974d7-109">For Windows Server 2003 and Windows XP, the proper order of ACEs is complicated by the introduction of object-specific ACEs and automatic inheritance.</span></span>

<span data-ttu-id="974d7-110">En los pasos siguientes se describe el orden preferido:</span><span class="sxs-lookup"><span data-stu-id="974d7-110">The following steps describe the preferred order:</span></span>

1.  <span data-ttu-id="974d7-111">Todas las ACE explícitas se colocan en un grupo antes de cualquier ACE heredada.</span><span class="sxs-lookup"><span data-stu-id="974d7-111">All explicit ACEs are placed in a group before any inherited ACEs.</span></span>
2.  <span data-ttu-id="974d7-112">Dentro del grupo de ACE explícitas, las ACE de acceso denegado se colocan antes que las ACE permitidas para acceso.</span><span class="sxs-lookup"><span data-stu-id="974d7-112">Within the group of explicit ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>
3.  <span data-ttu-id="974d7-113">Las ACE heredadas se colocan en el orden en el que se heredan.</span><span class="sxs-lookup"><span data-stu-id="974d7-113">Inherited ACEs are placed in the order in which they are inherited.</span></span> <span data-ttu-id="974d7-114">Las ACE heredadas del elemento primario del objeto secundario aparecen en primer lugar, a continuación, las ACE heredadas de la primaria y así sucesivamente en el árbol de objetos.</span><span class="sxs-lookup"><span data-stu-id="974d7-114">ACEs inherited from the child object's parent come first, then ACEs inherited from the grandparent, and so on up the tree of objects.</span></span>
4.  <span data-ttu-id="974d7-115">Para cada nivel de ACE heredadas, las ACE de acceso denegado se colocan antes que las ACE permitidas para acceso.</span><span class="sxs-lookup"><span data-stu-id="974d7-115">For each level of inherited ACEs, access-denied ACEs are placed before access-allowed ACEs.</span></span>

<span data-ttu-id="974d7-116">Por supuesto, no todos los tipos ACE son necesarios en una ACL.</span><span class="sxs-lookup"><span data-stu-id="974d7-116">Of course, not all ACE types are required in an ACL.</span></span>

<span data-ttu-id="974d7-117">Funciones como [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) y [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) agregan una ACE al final de una ACL.</span><span class="sxs-lookup"><span data-stu-id="974d7-117">Functions such as [**AddAccessAllowedAceEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedaceex) and [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) add an ACE to the end of an ACL.</span></span> <span data-ttu-id="974d7-118">Es responsabilidad del autor de la llamada asegurarse de que las ACE se agreguen en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="974d7-118">It is the caller's responsibility to ensure that the ACEs are added in the proper order.</span></span>

 

 
