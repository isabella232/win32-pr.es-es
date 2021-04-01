---
title: Extensión de la interfaz de usuario para objetos de directorio
description: Con Microsoft Windows 2000 y versiones posteriores, están disponibles los complementos Microsoft Management Console (MMC), como Active Directory complemento usuarios y equipos, para la administración de Active Directory Domain Services.
ms.assetid: 758ec25d-42ab-46ba-aa58-416d7ac8fd68
ms.tgt_platform: multiple
keywords:
- Active Directory, uso, extensión de la interfaz de usuario
- objetos AD, extensión de la interfaz de usuario para objetos de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d635132a26e80a63fddb35f779211308779f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773158"
---
# <a name="extending-the-user-interface-for-directory-objects"></a><span data-ttu-id="5e91a-105">Extensión de la interfaz de usuario para objetos de directorio</span><span class="sxs-lookup"><span data-stu-id="5e91a-105">Extending the User Interface for Directory Objects</span></span>

<span data-ttu-id="5e91a-106">Con Microsoft Windows 2000 y versiones posteriores, están disponibles los complementos Microsoft Management Console (MMC), como Active Directory complemento usuarios y equipos, para la administración de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5e91a-106">With Microsoft Windows 2000 and later, Microsoft Management Console (MMC) snap-ins, such as the Active Directory Users and Computers snap-in, for administration of Active Directory Domain Services, are available.</span></span> <span data-ttu-id="5e91a-107">Además, el shell de Windows 2000 incluye interfaces de usuario (UI) para buscar objetos que residen en el directorio y leen y escriben propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e91a-107">In addition, the Windows 2000 shell includes user interfaces (UIs) for finding objects that reside in the directory and reading and writing properties.</span></span> <span data-ttu-id="5e91a-108">En esta sección se explica cómo ampliar la interfaz de usuario para ver y administrar Active Directory Domain Services objetos en el shell de Windows y Active Directory complementos administrativos. En esta sección también se describe lo que se necesita para implementar las extensiones de la interfaz de usuario en los equipos de escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="5e91a-108">This section explains how to extend the UI for viewing and managing Active Directory Domain Services objects in the Windows shell and Active Directory administrative snap-ins. This section also covers what is required to deploy the UI extensions to the user's desktops.</span></span>

<span data-ttu-id="5e91a-109">En concreto, en esta sección se trata lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e91a-109">Specifically, this section discusses the following:</span></span>

-   [<span data-ttu-id="5e91a-110">Acerca de las interfaces de usuario Active Directory</span><span class="sxs-lookup"><span data-stu-id="5e91a-110">About Active Directory User Interfaces</span></span>](about-the-user-interfaces-of-active-directory-domain-services.md)
-   [<span data-ttu-id="5e91a-111">Especificadores de presentación</span><span class="sxs-lookup"><span data-stu-id="5e91a-111">Display Specifiers</span></span>](display-specifiers.md)
-   [<span data-ttu-id="5e91a-112">Nombres para mostrar de clases y atributos</span><span class="sxs-lookup"><span data-stu-id="5e91a-112">Class and Attribute Display Names</span></span>](class-and-attribute-display-names.md)
-   [<span data-ttu-id="5e91a-113">Iconos de clase</span><span class="sxs-lookup"><span data-stu-id="5e91a-113">Class Icons</span></span>](class-icons.md)
-   [<span data-ttu-id="5e91a-114">Ver contenedores como nodos de hoja</span><span class="sxs-lookup"><span data-stu-id="5e91a-114">Viewing Containers as Leaf Nodes</span></span>](viewing-containers-as-leaf-nodes.md)
-   [<span data-ttu-id="5e91a-115">Modificación de las interfaces de usuario existentes</span><span class="sxs-lookup"><span data-stu-id="5e91a-115">Modifying Existing User Interfaces</span></span>](modifying-existing-user-interfaces.md)
-   [<span data-ttu-id="5e91a-116">Extensión de la interfaz de usuario para las nuevas clases de objeto</span><span class="sxs-lookup"><span data-stu-id="5e91a-116">User Interface Extension for New Object Classes</span></span>](user-interface-extension-for-new-object-classes.md)
-   [<span data-ttu-id="5e91a-117">Páginas de propiedades para su uso con especificadores de presentación</span><span class="sxs-lookup"><span data-stu-id="5e91a-117">Property Pages for Use with Display Specifiers</span></span>](property-pages-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="5e91a-118">Menús contextuales para su uso con especificadores de presentación</span><span class="sxs-lookup"><span data-stu-id="5e91a-118">Context Menus for Use with Display Specifiers</span></span>](context-menus-for-use-with-display-specifiers.md)
-   [<span data-ttu-id="5e91a-119">Asistentes para crear objetos</span><span class="sxs-lookup"><span data-stu-id="5e91a-119">Object Creation Wizards</span></span>](object-creation-wizards.md)
-   [<span data-ttu-id="5e91a-120">Usar cuadros de diálogo estándar para controlar objetos en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="5e91a-120">Using Standard Dialog Boxes for Handling Objects in Active Directory Domain Services</span></span>](using-standard-dialog-boxes-to-handle-objects-in-active-directory-domain-services.md)
-   [<span data-ttu-id="5e91a-121">Controladores de notificaciones administrativas</span><span class="sxs-lookup"><span data-stu-id="5e91a-121">Administrative Notification Handlers</span></span>](administrative-notification-handlers.md)
-   [<span data-ttu-id="5e91a-122">Distribución de componentes de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="5e91a-122">Distributing User Interface Components</span></span>](distributing-user-interface-components.md)
-   [<span data-ttu-id="5e91a-123">Cómo deben usar las aplicaciones los especificadores de presentación</span><span class="sxs-lookup"><span data-stu-id="5e91a-123">How Applications Should Use Display Specifiers</span></span>](how-applications-should-use-display-specifiers.md)
-   [<span data-ttu-id="5e91a-124">Depurar una extensión de Active Directory</span><span class="sxs-lookup"><span data-stu-id="5e91a-124">Debugging an Active Directory Extension</span></span>](debugging-an-active-directory-extension.md)

 

 




