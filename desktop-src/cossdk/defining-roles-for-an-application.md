---
description: Para determinar una directiva de seguridad para una aplicación, defina los privilegios de seguridad que requiere.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Definición de roles para una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705268"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="91312-103">Definición de roles para una aplicación</span><span class="sxs-lookup"><span data-stu-id="91312-103">Defining Roles for an Application</span></span>

<span data-ttu-id="91312-104">Para determinar una directiva de seguridad para una aplicación, defina los privilegios de seguridad que requiere.</span><span class="sxs-lookup"><span data-stu-id="91312-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="91312-105">Para ello, declare un nivel simbólico de privilegio como un rol (es decir, defina el rol para la aplicación) y, a continuación, [asigne el rol](assigning-roles-to-components--interfaces--or-methods.md) a recursos específicos dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91312-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="91312-106">Este diseño se cumple cuando se implementa la aplicación y los administradores del sistema rellenan el rol con usuarios y grupos de usuarios reales.</span><span class="sxs-lookup"><span data-stu-id="91312-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="91312-107">Para obtener más información, consulte [Administración de seguridad basada en roles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="91312-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="91312-108">**Para agregar un rol a una aplicación**</span><span class="sxs-lookup"><span data-stu-id="91312-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="91312-109">En el árbol de consola de la herramienta administrativa Servicios de componentes, busque la aplicación COM+ a la que desea agregar el rol.</span><span class="sxs-lookup"><span data-stu-id="91312-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="91312-110">Expanda el árbol para ver las carpetas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91312-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="91312-111">Haga clic con el botón secundario en la carpeta **roles** de la aplicación, seleccione **nuevo** y, a continuación, haga clic en **rol**.</span><span class="sxs-lookup"><span data-stu-id="91312-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="91312-112">En el cuadro de diálogo **rol**, escriba el nombre del nuevo rol en el cuadro proporcionado.</span><span class="sxs-lookup"><span data-stu-id="91312-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="91312-113">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="91312-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="91312-114">Después de agregar roles a la aplicación, debe asegurarse de asignar los roles a los componentes, interfaces y métodos adecuados.</span><span class="sxs-lookup"><span data-stu-id="91312-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="91312-115">De lo contrario, si se ha elegido y habilitado la seguridad basada en roles y si se han agregado roles pero no se han asignado, se producirá un error en todas las llamadas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91312-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="91312-116">Para obtener más información, vea [asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md).</span><span class="sxs-lookup"><span data-stu-id="91312-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="91312-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91312-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91312-118">Asignar roles a componentes, interfaces o métodos</span><span class="sxs-lookup"><span data-stu-id="91312-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="91312-119">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="91312-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="91312-120">Habilitación de las comprobaciones de acceso para una aplicación</span><span class="sxs-lookup"><span data-stu-id="91312-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="91312-121">Habilitar comprobaciones de acceso en el nivel de componente</span><span class="sxs-lookup"><span data-stu-id="91312-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="91312-122">Establecimiento de un nivel de seguridad para las comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="91312-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



