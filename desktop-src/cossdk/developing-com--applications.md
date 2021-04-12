---
description: Al desarrollar aplicaciones COM+, las tareas principales incluyen el diseño de componentes COM para encapsular la lógica de la aplicación y la integración de estos componentes en una aplicación COM+, la creación de la aplicación COM+ y la administración de la aplicación a través de la implementación y el mantenimiento.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Desarrollo de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538584"
---
# <a name="developing-com-applications"></a><span data-ttu-id="d23b0-103">Desarrollo de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="d23b0-103">Developing COM+ Applications</span></span>

<span data-ttu-id="d23b0-104">Al desarrollar aplicaciones COM+, las tareas principales incluyen el diseño de componentes COM para encapsular la lógica de la aplicación y la integración de estos componentes en una aplicación COM+, la creación de la aplicación COM+ y la administración de la aplicación a través de la implementación y el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="d23b0-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="d23b0-105">Diseñar componentes COM</span><span class="sxs-lookup"><span data-stu-id="d23b0-105">Designing COM Components</span></span>

<span data-ttu-id="d23b0-106">En los pasos siguientes se describe un procedimiento general para un buen diseño de componentes:</span><span class="sxs-lookup"><span data-stu-id="d23b0-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="d23b0-107">Defina las clases COM y las clases de implementación.</span><span class="sxs-lookup"><span data-stu-id="d23b0-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="d23b0-108">Agrupe las clases en componentes.</span><span class="sxs-lookup"><span data-stu-id="d23b0-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="d23b0-109">Seleccione el conjunto de servicios COM+ para el componente, aunque no se especifiquen todos al desarrollar el componente.</span><span class="sxs-lookup"><span data-stu-id="d23b0-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="d23b0-110">Estos servicios se pueden especificar posteriormente mediante la herramienta administrativa Servicios de componentes o el modelo de objetos de administración de COM+ (vea [automatizar la administración de com+](automating-com--administration.md) para obtener más información sobre el modelo de objetos de administración de com+).</span><span class="sxs-lookup"><span data-stu-id="d23b0-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="d23b0-111">Crear la aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="d23b0-111">Creating the COM+ Application</span></span>

<span data-ttu-id="d23b0-112">Después de diseñar los componentes COM, el desarrollador integra los componentes en una aplicación COM+ y configura la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d23b0-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="d23b0-113">Los siguientes pasos describen el proceso:</span><span class="sxs-lookup"><span data-stu-id="d23b0-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="d23b0-114">Integre los componentes en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="d23b0-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="d23b0-115">Puede integrar los componentes en una aplicación COM+ existente o crear una nueva aplicación (vacía) para los componentes.</span><span class="sxs-lookup"><span data-stu-id="d23b0-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="d23b0-116">(Consulte [creación de aplicaciones com+](creating-com--applications.md)).</span><span class="sxs-lookup"><span data-stu-id="d23b0-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="d23b0-117">Especifique el conjunto de atributos correcto para cada una de las clases (si hay alguna, y si no se especifica en la herramienta de desarrollo).</span><span class="sxs-lookup"><span data-stu-id="d23b0-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="d23b0-118">Estos atributos expresan las dependencias de los componentes en los servicios COM+ en los que puede depender su implementación (por ejemplo, transacciones, componentes en cola, seguridad, agrupación de objetos y activación Just-in-Time).</span><span class="sxs-lookup"><span data-stu-id="d23b0-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="d23b0-119">Configure el marco de seguridad (roles y asignación de roles para clases, interfaces y métodos).</span><span class="sxs-lookup"><span data-stu-id="d23b0-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="d23b0-120">Configure atributos específicos del entorno en clases y aplicaciones (por ejemplo, el tamaño predeterminado del grupo de objetos).</span><span class="sxs-lookup"><span data-stu-id="d23b0-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="d23b0-121">El administrador del sistema puede establecer (o modificar) más adelante estos atributos específicos del entorno.</span><span class="sxs-lookup"><span data-stu-id="d23b0-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="d23b0-122">Exporte la aplicación para su redistribución e implementación.</span><span class="sxs-lookup"><span data-stu-id="d23b0-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="d23b0-123">Para obtener información más detallada sobre los pasos para el diseño de aplicaciones distribuidas, consulte [diseño de aplicaciones com+](designing-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="d23b0-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="d23b0-124">Administrar aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="d23b0-124">Administering COM+ Applications</span></span>

<span data-ttu-id="d23b0-125">Normalmente, un programador entrega una aplicación COM+ parcialmente configurada al administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="d23b0-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="d23b0-126">A continuación, el administrador puede personalizar la aplicación para uno o más entornos específicos (por ejemplo, agregando cuentas de usuario en roles y nombres de servidor en un clúster de aplicaciones).</span><span class="sxs-lookup"><span data-stu-id="d23b0-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="d23b0-127">Entre las tareas del administrador se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="d23b0-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="d23b0-128">Instalación de la aplicación COM+ parcialmente configurada en un equipo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d23b0-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="d23b0-129">Proporcionar atributos específicos del entorno, como los miembros del rol y el tamaño del grupo de objetos.</span><span class="sxs-lookup"><span data-stu-id="d23b0-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="d23b0-130">Volver a exportar la aplicación COM+ completamente configurada.</span><span class="sxs-lookup"><span data-stu-id="d23b0-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="d23b0-131">Crear un proxy de aplicación (si se va a tener acceso a la aplicación de forma remota).</span><span class="sxs-lookup"><span data-stu-id="d23b0-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="d23b0-132">Una vez que una aplicación está totalmente configurada para un entorno específico, el administrador puede implementarla en máquinas de prueba o de producción.</span><span class="sxs-lookup"><span data-stu-id="d23b0-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="d23b0-133">Esto implica la instalación de la aplicación COM+ completamente configurada en uno o varios equipos.</span><span class="sxs-lookup"><span data-stu-id="d23b0-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="d23b0-134">Para obtener información detallada sobre los procedimientos de administración de COM+, vea la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="d23b0-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



