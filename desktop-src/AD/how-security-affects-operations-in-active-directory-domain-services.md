---
title: Cómo afecta la seguridad a las operaciones en Active Directory Domain Services
description: Active Directory Domain Services usar el control de acceso para conceder o denegar el acceso a objetos, propiedades y operaciones en función de la identidad del usuario que realiza el intento de acceso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Efectos de seguridad en Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903113"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="9f54f-104">Cómo afecta la seguridad a las operaciones en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="9f54f-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="9f54f-105">Active Directory Domain Services usar el control de acceso para conceder o denegar el acceso a objetos, propiedades y operaciones en función de la identidad del usuario que realiza el intento de acceso.</span><span class="sxs-lookup"><span data-stu-id="9f54f-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="9f54f-106">Cuando la aplicación se enlaza al directorio, se enlaza con las credenciales de usuario específicas.</span><span class="sxs-lookup"><span data-stu-id="9f54f-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="9f54f-107">Cuando se autentica, estas credenciales determinan el contexto de seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9f54f-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="9f54f-108">Independientemente de si las credenciales son las del usuario que ha iniciado sesión, un usuario especificado, una cuenta de servicio, una cuenta de equipo o un usuario no autenticado (invitado/todos), el servidor de Active Directory comprueba el derecho del usuario para tener acceso a un objeto antes de que se realice cualquier operación en ese objeto.</span><span class="sxs-lookup"><span data-stu-id="9f54f-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="9f54f-109">El usuario puede o no tener acceso a un objeto determinado, a sus elementos secundarios, a sus propiedades u operaciones en ese objeto, lo que significa que la aplicación debe controlar los posibles errores causados por el acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="9f54f-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="9f54f-110">Para obtener más información sobre los contextos de seguridad y los efectos del control de acceso en varias operaciones, vea:</span><span class="sxs-lookup"><span data-stu-id="9f54f-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="9f54f-111">Operaciones de Access Control y de lectura</span><span class="sxs-lookup"><span data-stu-id="9f54f-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="9f54f-112">Operaciones de Access Control y escritura</span><span class="sxs-lookup"><span data-stu-id="9f54f-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="9f54f-113">Access Control y creación de objetos</span><span class="sxs-lookup"><span data-stu-id="9f54f-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="9f54f-114">Access Control y eliminación de objetos</span><span class="sxs-lookup"><span data-stu-id="9f54f-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 




