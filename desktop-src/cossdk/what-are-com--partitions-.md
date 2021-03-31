---
description: Una partición COM+ es un contenedor lógico que permite a las aplicaciones ejecutarse independientemente de otras configuraciones de esas aplicaciones.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: ¿Qué son las particiones COM+?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104156972"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="1c790-103">¿Qué son las particiones COM+?</span><span class="sxs-lookup"><span data-stu-id="1c790-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="1c790-104">Una partición COM+ es un contenedor lógico que permite a las aplicaciones ejecutarse independientemente de otras configuraciones de esas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1c790-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="1c790-105">Cada configuración de una aplicación se instala en una partición independiente y se puede administrar por separado, de acuerdo con las necesidades específicas de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="1c790-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="1c790-106">Durante la activación de un componente COM+, el servicio particiones determina la configuración del componente que se va a activar, en función de la identidad del usuario que solicita la activación del componente.</span><span class="sxs-lookup"><span data-stu-id="1c790-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="1c790-107">Por ejemplo, una sola organización que tiene dos grupos independientes, producción y entrenamiento, podría implementar particiones COM+ como una manera de permitir que los dos grupos usen configuraciones diferentes de una aplicación COM+ en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="1c790-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="1c790-108">**Windows XP:** La capacidad de crear, configurar o delegar particiones COM+ no está disponible.</span><span class="sxs-lookup"><span data-stu-id="1c790-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="1c790-109">La partición global es la única partición de COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="1c790-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="1c790-110">**Windows 2000:** El servicio de particiones COM+ no está disponible en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1c790-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="1c790-111">Ventajas del uso de particiones COM+</span><span class="sxs-lookup"><span data-stu-id="1c790-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="1c790-112">El uso de particiones COM+ ofrece varias ventajas, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="1c790-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="1c790-113">Las organizaciones pueden reducir el costo total de propiedad (TCO) mediante el uso de menos servidores de aplicaciones físicos para admitir usuarios que necesitan varias configuraciones de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="1c790-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="1c790-114">Se reduce la sobrecarga administrativa.</span><span class="sxs-lookup"><span data-stu-id="1c790-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="1c790-115">En lugar de tener que configurar y administrar varios equipos, los administradores solo necesitan configurar y administrar varias particiones en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="1c790-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="1c790-116">Además, las particiones se pueden administrar mediante programación a través de la adición de una nueva interfaz de programación de COM+.</span><span class="sxs-lookup"><span data-stu-id="1c790-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="1c790-117">La seguridad se puede implementar y administrar partición a partición para usuarios locales, usuarios del dominio y unidades organizativas (OU).</span><span class="sxs-lookup"><span data-stu-id="1c790-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="1c790-118">Los programadores y administradores pueden utilizar las herramientas administrativas y de desarrollo de Microsoft, como el Windows SDK, Active Directory usuarios y equipos, y la herramienta administrativa Servicios de componentes, para administrar particiones COM+.</span><span class="sxs-lookup"><span data-stu-id="1c790-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="1c790-119">La característica de particiones está totalmente integrada en estas herramientas.</span><span class="sxs-lookup"><span data-stu-id="1c790-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="1c790-120">Escenario de uso principal</span><span class="sxs-lookup"><span data-stu-id="1c790-120">Primary Usage Scenario</span></span>

<span data-ttu-id="1c790-121">Una razón principal para que los clientes implementen la característica de particiones de COM+ es hospedar aplicaciones basadas en Web.</span><span class="sxs-lookup"><span data-stu-id="1c790-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="1c790-122">Por ejemplo, supongamos que una pequeña compañía de software desarrolla una aplicación COM+ para su uso por parte del personal del hospital.</span><span class="sxs-lookup"><span data-stu-id="1c790-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="1c790-123">La aplicación, que es una aplicación distribuida basada en Web, proporciona una manera para que los hospitales almacenen y recuperen registros médicos de pacientes mediante una base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c790-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="1c790-124">Supongamos que la compañía de software tiene tres clientes: Hospital A, hospital B y Hospital C. Aunque cada cliente ejecuta el lado cliente de la aplicación COM+ localmente en sus equipos de escritorio, el lado servidor de la aplicación COM+ reside en el servidor Web interno de la empresa de software y es accesible por sus clientes a través de la Web.</span><span class="sxs-lookup"><span data-stu-id="1c790-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="1c790-125">Dado que cada hospital tiene su propio conjunto de requisitos de almacenamiento y recuperación y su propio conjunto de datos de pacientes personalizados, la compañía de software debe proporcionar una manera de que varias configuraciones de la parte del servidor de la aplicación se ejecuten simultáneamente en el servidor Web.</span><span class="sxs-lookup"><span data-stu-id="1c790-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="1c790-126">Las particiones COM+ proporcionan una solución a este problema.</span><span class="sxs-lookup"><span data-stu-id="1c790-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="1c790-127">En la siguiente ilustración se muestra el escenario de particiones de la aplicación COM+ de la compañía de software.</span><span class="sxs-lookup"><span data-stu-id="1c790-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![Diagrama que muestra un escenario de particiones para una aplicación COM+, con una aplicación cliente para la aplicación de servidor en la base de datos de SQL Server.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="1c790-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c790-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c790-130">Restricciones de diseño de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="1c790-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="1c790-131">Particiones y componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="1c790-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="1c790-132">Implementación de particiones</span><span class="sxs-lookup"><span data-stu-id="1c790-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="1c790-133">Registro y activación de componentes en particiones</span><span class="sxs-lookup"><span data-stu-id="1c790-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



