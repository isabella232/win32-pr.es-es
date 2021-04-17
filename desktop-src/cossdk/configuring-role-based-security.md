---
description: Si la aplicación COM+ utiliza la seguridad basada en roles, hay varias tareas que deben completarse.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configuración de la seguridad de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360027"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="8bcf0-103">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="8bcf0-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="8bcf0-104">Si la aplicación COM+ utiliza la seguridad basada en roles, hay varias tareas que deben completarse.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="8bcf0-105">Al diseñar los componentes en la aplicación, debe definir los roles necesarios para ayudar a proteger el acceso a esos componentes.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="8bcf0-106">También puede decidir qué roles asignar a los componentes, interfaces y métodos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="8bcf0-107">Durante la integración de la aplicación, se usa la herramienta administrativa Servicios de componentes para agregar los roles definidos a la aplicación y asignar cada rol a los componentes, interfaces y métodos adecuados.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="8bcf0-108">Al configurar la seguridad basada en roles, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8bcf0-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="8bcf0-109">Habilite las comprobaciones de acceso en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-109">Enable access checks at the application level.</span></span> <span data-ttu-id="8bcf0-110">Para activar la comprobación de seguridad para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-110">To turn on security checking for an application.</span></span> <span data-ttu-id="8bcf0-111">Consulte [habilitación de comprobaciones de acceso para una aplicación](enabling-access-checks-for-an-application.md) para obtener más información sobre cómo realizar este paso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="8bcf0-112">Establezca el nivel de seguridad para las comprobaciones de acceso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-112">Set security level for access checks.</span></span> <span data-ttu-id="8bcf0-113">Para establecer la seguridad en el proceso o en el nivel de componente y de proceso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="8bcf0-114">Consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md) para obtener más información sobre cómo realizar este paso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="8bcf0-115">Habilite las comprobaciones de acceso en el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-115">Enable access checks at the component level.</span></span> <span data-ttu-id="8bcf0-116">Para activar la comprobación de seguridad en los niveles de componente, interfaz y método.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="8bcf0-117">Consulte [habilitación de comprobaciones de acceso en el nivel de componente](enabling-access-checks-at-the-component-level.md) para obtener más información sobre cómo realizar este paso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="8bcf0-118">Definir roles para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-118">Define roles for an application.</span></span> <span data-ttu-id="8bcf0-119">Crear roles para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-119">To create roles for an application.</span></span> <span data-ttu-id="8bcf0-120">Consulte [definición de roles para una aplicación](defining-roles-for-an-application.md) para más información sobre cómo realizar este paso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="8bcf0-121">Asignar roles a componentes, interfaces o métodos.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="8bcf0-122">Para asignar roles a recursos específicos dentro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="8bcf0-123">Vea [asignar roles a componentes, interfaces o métodos](assigning-roles-to-components--interfaces--or-methods.md) para obtener más información sobre cómo realizar este paso.</span><span class="sxs-lookup"><span data-stu-id="8bcf0-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bcf0-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bcf0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bcf0-125">Configuración de la Directiva de restricción de software</span><span class="sxs-lookup"><span data-stu-id="8bcf0-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="8bcf0-126">Establecer un nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="8bcf0-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



