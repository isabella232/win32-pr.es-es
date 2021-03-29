---
title: Protección de objetos y atributos
description: Una lista de control de acceso (ACL) protege todos los objetos de Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protección de objetos y atributos
- seguridad AD, protección de objetos y atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773129"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="a4baf-105">Protección de objetos y atributos</span><span class="sxs-lookup"><span data-stu-id="a4baf-105">Object and Attribute Protection</span></span>

<span data-ttu-id="a4baf-106">Una lista de control de acceso (ACL) protege todos los objetos de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a4baf-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="a4baf-107">Las ACL determinan quién puede ver el objeto, qué atributos pueden leer y las acciones que cada usuario puede realizar en el objeto.</span><span class="sxs-lookup"><span data-stu-id="a4baf-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="a4baf-108">La existencia de un objeto o un atributo no se revela nunca a un usuario no autorizado.</span><span class="sxs-lookup"><span data-stu-id="a4baf-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="a4baf-109">Una ACL es una lista de entradas de control de acceso (ACE) almacenadas con el objeto que protege.</span><span class="sxs-lookup"><span data-stu-id="a4baf-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="a4baf-110">En Windows NT y Windows 2000, las ACL se almacenan como valores binarios, denominados descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a4baf-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="a4baf-111">Cada ACE contiene un identificador de seguridad (SID), que identifica la entidad de seguridad (usuario o grupo) a la que se aplica la ACE y los datos sobre el tipo de acceso que la ACE concede o deniega.</span><span class="sxs-lookup"><span data-stu-id="a4baf-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="a4baf-112">Las ACL de los objetos de directorio contienen ACE que se aplican al objeto como un todo y las ACE que se aplican a los atributos individuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="a4baf-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="a4baf-113">Esto permite a un administrador controlar no solo qué usuarios pueden ver un objeto, sino también qué propiedades pueden ver los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a4baf-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="a4baf-114">Por ejemplo, a todos los usuarios se les puede conceder acceso de lectura a los atributos de número de teléfono y correo electrónico para todos los demás usuarios, pero las propiedades de seguridad de los usuarios pueden denegarse a todos los miembros de un grupo de administradores de seguridad especial.</span><span class="sxs-lookup"><span data-stu-id="a4baf-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="a4baf-115">A los usuarios individuales se les puede conceder acceso de escritura a los atributos personales, como las direcciones de teléfono y correo electrónico de sus propios objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="a4baf-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




