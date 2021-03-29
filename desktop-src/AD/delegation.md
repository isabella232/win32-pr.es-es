---
title: Delegación
description: La delegación es una de las características de seguridad más importantes de Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- AD de delegación
- seguridad AD, Delegación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993913"
---
# <a name="delegation"></a><span data-ttu-id="61cb3-105">Delegación</span><span class="sxs-lookup"><span data-stu-id="61cb3-105">Delegation</span></span>

<span data-ttu-id="61cb3-106">La *delegación* es una de las características de seguridad más importantes de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="61cb3-106">*Delegation* is one of the most important security features of Active Directory Domain Services.</span></span> <span data-ttu-id="61cb3-107">La delegación permite a una autoridad administrativa superior conceder derechos administrativos específicos para contenedores y subárboles a usuarios y grupos.</span><span class="sxs-lookup"><span data-stu-id="61cb3-107">Delegation enables a higher administrative authority to grant specific administrative rights for containers and subtrees to individuals and groups.</span></span> <span data-ttu-id="61cb3-108">Ya no se necesitan administradores de dominio, con una amplia autoridad sobre grandes segmentos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="61cb3-108">Domain administrators, with broad authority over large segments of users, are no longer required.</span></span>

<span data-ttu-id="61cb3-109">Una ACE puede conceder derechos administrativos específicos para los objetos de un contenedor a un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="61cb3-109">An ACE can grant specific administrative rights for the objects in a container to a user or group.</span></span> <span data-ttu-id="61cb3-110">Los derechos se conceden para operaciones específicas en clases de objeto específicas mediante ACE en la ACL del contenedor.</span><span class="sxs-lookup"><span data-stu-id="61cb3-110">Rights are granted for specific operations on specific object classes using ACEs in the container's ACL.</span></span> <span data-ttu-id="61cb3-111">Por ejemplo, para permitir que un usuario llamado "usuario 1" sea un administrador de la unidad organizativa "contabilidad corporativa", agregue ACE a la ACL en "contabilidad corporativa" como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="61cb3-111">For example, to enable a user named "user 1" to be an administrator of the "Corporate Accounting" organizational unit, add ACEs to the ACL on "Corporate Accounting" as follows:</span></span>

<span data-ttu-id="61cb3-112">"" usuario 1 "; Garantizar Crear, modificar, eliminar; usuario de clase de objeto "usuario 1"; Garantizar Crear, modificar, eliminar; grupo de clase de objeto "usuario 1"; Garantizar Escritura; usuario de clase de objeto; Contraseña de atributo "</span><span class="sxs-lookup"><span data-stu-id="61cb3-112">""user 1";Grant ;Create, Modify, Delete;Object-Class User"user 1";Grant ;Create, Modify, Delete;Object-Class Group"user 1";Grant ;Write;Object-Class User; Attribute Password"</span></span>

<span data-ttu-id="61cb3-113">Ahora, el usuario 1 puede crear nuevos usuarios y grupos en las cuentas corporativas y establecer las contraseñas de los usuarios existentes, pero el usuario 1 no puede crear ninguna otra clase de objeto y no puede afectar a los usuarios de ningún otro contenedor, a menos que, por supuesto, se conceda al usuario 1 acceso mediante ACE en los otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="61cb3-113">Now, user 1 can create new users and groups in Corporate Accounting and set the passwords on existing users, but user 1 cannot create any other object classes and cannot affect users in any other containers, unless, of course, user 1 is granted that access by ACEs on the other containers.</span></span>

 

 




