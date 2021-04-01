---
description: Una vez completados los modelos lógicos y conceptuales, puede tomar decisiones sobre la implementación física de la aplicación.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'El modelo físico: arquitectura de la aplicación'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153458"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="7cd9b-103">El modelo físico: arquitectura de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7cd9b-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="7cd9b-104">Una vez completados los modelos lógicos y conceptuales, puede tomar decisiones sobre la implementación física de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="7cd9b-105">Para crear el modelo físico, debe saber dónde se deben ubicar los distintos servicios de la aplicación y cómo deben implementarse.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="7cd9b-106">La determinación de dónde residan los distintos servicios debe ir antes de que se implementen los servicios.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="7cd9b-107">Una regla básica para determinar dónde residen los distintos servicios es: Coloque el componente en el que se está usando.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="7cd9b-108">Si, por ejemplo, un componente muestra información para el cliente base, debe ir en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="7cd9b-109">Si un componente valida la información del cliente base, también debe residir en el equipo del cliente base.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="7cd9b-110">Si un componente actualiza la información en una base de datos, debe residir en el servidor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="7cd9b-111">Por supuesto, existen consideraciones adicionales que realizan excepciones a esta regla.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="7cd9b-112">Los problemas de rendimiento y seguridad también pueden indicar dónde se encuentra un componente.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="7cd9b-113">Tenga en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-113">Consider the following:</span></span>

-   <span data-ttu-id="7cd9b-114">¿Un componente va a cambiar con frecuencia, lo que dificulta la distribución de las actualizaciones?</span><span class="sxs-lookup"><span data-stu-id="7cd9b-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="7cd9b-115">¿Usará el componente otras aplicaciones, como un componente de comprobación de seguridad común?</span><span class="sxs-lookup"><span data-stu-id="7cd9b-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="7cd9b-116">¿El componente realiza cálculos largos o realiza funciones, como la impresión, que se pueden descargar en un servidor?</span><span class="sxs-lookup"><span data-stu-id="7cd9b-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="7cd9b-117">¿Se puede mejorar la seguridad de un componente colocándolo en un servidor?</span><span class="sxs-lookup"><span data-stu-id="7cd9b-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="7cd9b-118">La ubicación correcta de los componentes de una aplicación también puede aislar al equipo de desarrollo de la recodificación costosa si el sistema o la ubicación de los datos cambian.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="7cd9b-119">Por ejemplo, si coloca las reglas de acceso a datos en una capa de datos en lugar de en procedimientos almacenados, la aplicación se aislará más fácilmente de la dependencia de un DBMS específico.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="7cd9b-120">No solo los cambios se limitan y prueban en compartimentos, pero los orígenes de datos se pueden cambiar y los datos se pueden distribuir sin cambiar fundamentalmente la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="7cd9b-121">Por último, la ubicación de los componentes debe aprovechar las eficiencias del sistema.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="7cd9b-122">Es tiempo y rentable colocar objetos de negocio en ubicaciones centralizadas en la red.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="7cd9b-123">Los objetos se pueden compartir entre aplicaciones y las pruebas unitarias se pueden realizar antes de que se implementen los componentes.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="7cd9b-124">También se pueden reducir los costos de mantenimiento, ya que los cambios de regla solo se producen en un único punto.</span><span class="sxs-lookup"><span data-stu-id="7cd9b-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cd9b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7cd9b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cd9b-126">El modelo conceptual: requisitos de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7cd9b-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="7cd9b-127">El modelo lógico: definición y planeación de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7cd9b-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



