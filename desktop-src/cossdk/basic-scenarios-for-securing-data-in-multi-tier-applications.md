---
description: En este tema se presentan algunos escenarios de bloques de creación, que ilustran los criterios que se describen en decidir dónde aplicar la seguridad.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Escenarios básicos para la protección de datos en aplicaciones de niveles múltiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705335"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="10d5e-103">Escenarios básicos para la protección de datos en aplicaciones de niveles múltiples</span><span class="sxs-lookup"><span data-stu-id="10d5e-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="10d5e-104">En este tema se presentan algunos escenarios de bloques de creación, que ilustran los criterios [que se describen en decidir dónde aplicar la seguridad](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="10d5e-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="10d5e-105">Escenario de servidor de confianza</span><span class="sxs-lookup"><span data-stu-id="10d5e-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="10d5e-106">La base de datos confía totalmente en la aplicación COM+ para autenticar y autorizar a los usuarios finales para que tengan acceso a los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="10d5e-107">Preferiblemente, la base de datos está protegida contra cualquier acceso excepto a través de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10d5e-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="10d5e-108">La aplicación COM+ utiliza la seguridad basada en roles para autorizar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="10d5e-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="10d5e-109">Las conexiones se abren en la identidad de la aplicación COM+ y se pueden agrupar por completo.</span><span class="sxs-lookup"><span data-stu-id="10d5e-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="10d5e-110">La aplicación COM+ puede realizar la auditoría y el registro, o la aplicación puede pasar esta información a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="10d5e-111">Este escenario funciona mejor con los datos a los que se puede tener acceso mediante categorías de usuarios predecibles que se pueden encapsular en roles.</span><span class="sxs-lookup"><span data-stu-id="10d5e-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="10d5e-112">Por ejemplo, solo los "administradores", "cajeros" y "contables" tienen permiso para acceder a las cuentas.</span><span class="sxs-lookup"><span data-stu-id="10d5e-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="10d5e-113">La lógica de negocios de lo que se habilita para cada una de ellas se aplica en el nivel intermedio.</span><span class="sxs-lookup"><span data-stu-id="10d5e-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="10d5e-114">Escenario de suplantación</span><span class="sxs-lookup"><span data-stu-id="10d5e-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="10d5e-115">La base de datos realiza su propia autenticación y autorización de los usuarios finales para ayudar a limitar el acceso a los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="10d5e-116">La aplicación COM+ suplanta a los clientes cada vez que accede a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="10d5e-117">Las conexiones se realizan en cada llamada y no se pueden volver a usar.</span><span class="sxs-lookup"><span data-stu-id="10d5e-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="10d5e-118">Este escenario funciona mejor con los datos que están estrechamente enlazados a las clases de usuarios muy pequeñas.</span><span class="sxs-lookup"><span data-stu-id="10d5e-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="10d5e-119">Por ejemplo, cada empleado puede tener acceso únicamente a su propio archivo de personal, y cada administrador solo puede tener acceso a los archivos de personal de sus informes.</span><span class="sxs-lookup"><span data-stu-id="10d5e-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="10d5e-120">Escenario híbrido</span><span class="sxs-lookup"><span data-stu-id="10d5e-120">Hybrid Scenario</span></span>

<span data-ttu-id="10d5e-121">Una combinación de los dos escenarios anteriores, donde la suplantación solo se utiliza cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="10d5e-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="10d5e-122">Este escenario funciona mejor en situaciones en las que tiene relaciones de datos de usuario híbridos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="10d5e-123">Por ejemplo, tiene "administradores", "cajeros", "contables" y miles de clientes Web individuales que pueden tener acceso a solo sus propias cuentas.</span><span class="sxs-lookup"><span data-stu-id="10d5e-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="10d5e-124">Puede separar las rutas de acceso lógicas a través de la aplicación, potencialmente con componentes independientes, para administrar la última clase de usuarios, especialmente cuando las suposiciones de rendimiento para esos usuarios son diferentes.</span><span class="sxs-lookup"><span data-stu-id="10d5e-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="10d5e-125">Escenario de confianza con roles de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="10d5e-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="10d5e-126">Microsoft SQL Server 7,0 y versiones posteriores pueden autorizar el acceso a filas específicas mediante roles, pero confía en la aplicación COM+ para autenticar y autorizar a los usuarios y asignarlos a los roles correctos en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="10d5e-127">La aplicación COM+ autoriza a los usuarios mediante la seguridad basada en roles y los roles de aplicación se corresponden bien con los roles de base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="10d5e-128">Se pueden abrir conexiones que son específicas de un rol de base de datos determinado.</span><span class="sxs-lookup"><span data-stu-id="10d5e-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="10d5e-129">Estas conexiones se pueden reutilizar si están retenidas por objetos agrupados en las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="10d5e-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="10d5e-130">Para obtener más información sobre cómo hacerlo, consulte [agrupación de objetos com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="10d5e-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="10d5e-131">La aplicación COM+ puede realizar la auditoría y el registro, o la aplicación puede pasar esta información a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="10d5e-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="10d5e-132">Este escenario funciona mejor por lo general en los mismos tipos de usuarios y datos que en el primer escenario de servidor de confianza, ya que la aplicación COM+ sigue siendo de confianza para administrar correctamente la autorización.</span><span class="sxs-lookup"><span data-stu-id="10d5e-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="10d5e-133">Sin embargo, protege la base de datos frente al acceso no autorizado, a la vez que permite el acceso desde varios orígenes externos a la aplicación COM+, sin incurrir en las penalizaciones de escala y rendimiento presentes en el escenario de suplantación.</span><span class="sxs-lookup"><span data-stu-id="10d5e-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10d5e-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10d5e-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d5e-135">Decidir dónde aplicar la seguridad</span><span class="sxs-lookup"><span data-stu-id="10d5e-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="10d5e-136">Seguridad de aplicaciones de niveles múltiples</span><span class="sxs-lookup"><span data-stu-id="10d5e-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



