---
description: Del mismo modo que el sistema usa descriptores de seguridad para controlar el acceso a los objetos protegibles, un servidor puede usar descriptores de seguridad para controlar el acceso a sus objetos privados. Para obtener más información sobre el modelo de seguridad de Windows, vea modelo de Access Control.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Access Control basados en ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813286"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="aaa19-104">Access Control basados en ACL</span><span class="sxs-lookup"><span data-stu-id="aaa19-104">ACL-based Access Control</span></span>

<span data-ttu-id="aaa19-105">Del mismo modo que el sistema usa [descriptores de seguridad](security-descriptors.md) para controlar el acceso a los objetos protegibles, un servidor puede usar descriptores de seguridad para controlar el acceso a sus objetos privados.</span><span class="sxs-lookup"><span data-stu-id="aaa19-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="aaa19-106">Para obtener más información sobre el modelo de seguridad de Windows, vea [modelo de Access Control](access-control-model.md).</span><span class="sxs-lookup"><span data-stu-id="aaa19-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="aaa19-107">Un servidor protegido puede [crear un descriptor de seguridad](security-descriptors-for-private-objects.md) con una DACL que especifique los tipos de acceso permitidos para varios [confíantes](trustees.md).</span><span class="sxs-lookup"><span data-stu-id="aaa19-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="aaa19-108">En un caso sencillo, el servidor podría crear un único descriptor [de seguridad para controlar el acceso a todos los datos y la funcionalidad del servidor](checking-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="aaa19-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="aaa19-109">Para una granularidad más fina de protección, el servidor podría crear descriptores de seguridad para cada uno de sus objetos privados o para diferentes tipos de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="aaa19-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="aaa19-110">Por ejemplo, cuando un cliente solicita al servidor que cree un nuevo objeto en una base de datos, el servidor podría crear un descriptor de seguridad para el nuevo objeto privado.</span><span class="sxs-lookup"><span data-stu-id="aaa19-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="aaa19-111">Después, el servidor podría almacenar el descriptor de seguridad con el objeto privado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aaa19-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="aaa19-112">Cuando un cliente intenta obtener acceso al objeto, el servidor recupera el descriptor de seguridad para comprobar los derechos de acceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="aaa19-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="aaa19-113">Es importante tener en cuenta que no hay nada en un descriptor de seguridad que lo asocie con el objeto o la funcionalidad que protege.</span><span class="sxs-lookup"><span data-stu-id="aaa19-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="aaa19-114">En su lugar, es el servidor protegido el que mantiene la asociación.</span><span class="sxs-lookup"><span data-stu-id="aaa19-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="aaa19-115">También se puede auditar el acceso al objeto privado.</span><span class="sxs-lookup"><span data-stu-id="aaa19-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="aaa19-116">Consulte [Auditoría de acceso a objetos privados](auditing-access-to-private-objects.md) para obtener una descripción de este.</span><span class="sxs-lookup"><span data-stu-id="aaa19-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 



