---
description: El control de acceso hace referencia a las características de seguridad que controlan quién puede tener acceso a los recursos del sistema operativo. Las aplicaciones llaman a las funciones de control de acceso para establecer quién puede tener acceso a recursos específicos o controlar el acceso a los recursos proporcionados por la aplicación.
ms.assetid: d9ce4ec5-5c09-4b33-93a1-39638a925986
title: Access Control (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31c0198f0ce0de77750e0587d9b54c1e20cee756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082528"
---
# <a name="access-control-authorization"></a><span data-ttu-id="5ee21-104">Access Control (autorización)</span><span class="sxs-lookup"><span data-stu-id="5ee21-104">Access Control (Authorization)</span></span>

<span data-ttu-id="5ee21-105">El control de acceso hace referencia a las características de seguridad que controlan quién puede tener acceso a los recursos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5ee21-105">Access control refers to security features that control who can access resources in the operating system.</span></span> <span data-ttu-id="5ee21-106">Las aplicaciones llaman a las funciones de control de acceso para establecer quién puede tener acceso a recursos específicos o controlar el acceso a los recursos proporcionados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5ee21-106">Applications call access control functions to set who can access specific resources or control access to resources provided by the application.</span></span>

<span data-ttu-id="5ee21-107">En esta información general se describe el modelo de seguridad para controlar el acceso a objetos de Windows, como archivos, y para controlar el acceso a las funciones administrativas, como la configuración de la hora del sistema o la auditoría de las acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="5ee21-107">This overview describes the security model for controlling access to Windows objects, such as files, and for controlling access to administrative functions, such as setting the system time or auditing user actions.</span></span> <span data-ttu-id="5ee21-108">En el tema del [modelo de Access Control](access-control-model.md) se proporciona una descripción de alto nivel de las partes del control de acceso y cómo interactúan entre sí.</span><span class="sxs-lookup"><span data-stu-id="5ee21-108">The [Access Control Model](access-control-model.md) topic provides a high-level description of the parts of access control and how they interact with each other.</span></span>

<span data-ttu-id="5ee21-109">En los temas siguientes se describe el control de acceso:</span><span class="sxs-lookup"><span data-stu-id="5ee21-109">The following topics describe access control:</span></span>

-   [<span data-ttu-id="5ee21-110">Seguridad de nivel C2</span><span class="sxs-lookup"><span data-stu-id="5ee21-110">C2-level Security</span></span>](c2-level-security.md)
-   [<span data-ttu-id="5ee21-111">Modelo de Access Control</span><span class="sxs-lookup"><span data-stu-id="5ee21-111">Access Control Model</span></span>](access-control-model.md)
-   [<span data-ttu-id="5ee21-112">Lenguaje de definición de descriptores de seguridad</span><span class="sxs-lookup"><span data-stu-id="5ee21-112">Security Descriptor Definition Language</span></span>](security-descriptor-definition-language.md)
-   [<span data-ttu-id="5ee21-113">Privilegios</span><span class="sxs-lookup"><span data-stu-id="5ee21-113">Privileges</span></span>](privileges.md)
-   [<span data-ttu-id="5ee21-114">Generación de auditoría</span><span class="sxs-lookup"><span data-stu-id="5ee21-114">Audit Generation</span></span>](audit-generation.md)
-   [<span data-ttu-id="5ee21-115">Objetos protegibles</span><span class="sxs-lookup"><span data-stu-id="5ee21-115">Securable Objects</span></span>](securable-objects.md)
-   [<span data-ttu-id="5ee21-116">Access Control de bajo nivel</span><span class="sxs-lookup"><span data-stu-id="5ee21-116">Low-level Access Control</span></span>](low-level-access-control.md)

<span data-ttu-id="5ee21-117">A continuación se indican las tareas comunes de control de acceso:</span><span class="sxs-lookup"><span data-stu-id="5ee21-117">The following are common access control tasks:</span></span>

-   [<span data-ttu-id="5ee21-118">Cómo controlan el acceso a un objeto las DACL</span><span class="sxs-lookup"><span data-stu-id="5ee21-118">How DACLs Control Access to an Object</span></span>](how-dacls-control-access-to-an-object.md)
-   [<span data-ttu-id="5ee21-119">Controlar la creación de objetos secundarios en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-119">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="5ee21-120">ACE para controlar el acceso a las propiedades de un objeto</span><span class="sxs-lookup"><span data-stu-id="5ee21-120">ACEs to Control Access to an Object's Properties</span></span>](aces-to-control-access-to-an-object-s-properties.md)
-   [<span data-ttu-id="5ee21-121">Solicitar derechos de acceso a un objeto</span><span class="sxs-lookup"><span data-stu-id="5ee21-121">Requesting Access Rights to an Object</span></span>](requesting-access-rights-to-an-object.md)

<span data-ttu-id="5ee21-122">En los temas siguientes se proporciona código de ejemplo para las tareas de control de acceso:</span><span class="sxs-lookup"><span data-stu-id="5ee21-122">The following topics provide example code for access control tasks:</span></span>

-   [<span data-ttu-id="5ee21-123">Modificar las ACL de un objeto en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-123">Modifying the ACLs of an Object in C++</span></span>](modifying-the-acls-of-an-object-in-c--.md)
-   [<span data-ttu-id="5ee21-124">Crear un descriptor de seguridad para un nuevo objeto en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-124">Creating a Security Descriptor for a New Object in C++</span></span>](creating-a-security-descriptor-for-a-new-object-in-c--.md)
-   [<span data-ttu-id="5ee21-125">Controlar la creación de objetos secundarios en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-125">Controlling Child Object Creation in C++</span></span>](controlling-child-object-creation-in-c--.md)
-   [<span data-ttu-id="5ee21-126">Habilitar y deshabilitar privilegios en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-126">Enabling and Disabling Privileges in C++</span></span>](enabling-and-disabling-privileges-in-c--.md)
-   [<span data-ttu-id="5ee21-127">Buscar un SID en un token de acceso en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-127">Searching for a SID in an Access Token in C++</span></span>](searching-for-a-sid-in-an-access-token-in-c--.md)
-   [<span data-ttu-id="5ee21-128">Buscar el propietario de un objeto de archivo en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-128">Finding the Owner of a File Object in C++</span></span>](finding-the-owner-of-a-file-object-in-c--.md)
-   [<span data-ttu-id="5ee21-129">Tomar posesión de objetos en C++</span><span class="sxs-lookup"><span data-stu-id="5ee21-129">Taking Object Ownership in C++</span></span>](taking-object-ownership-in-c--.md)
-   [<span data-ttu-id="5ee21-130">Crear una DACL</span><span class="sxs-lookup"><span data-stu-id="5ee21-130">Creating a DACL</span></span>](/windows/desktop/SecBP/creating-a-dacl)

 

 
