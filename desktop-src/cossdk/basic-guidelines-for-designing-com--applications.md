---
description: Directrices básicas para diseñar aplicaciones COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Directrices básicas para diseñar aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153268"
---
# <a name="basic-guidelines-for-designing-com-applications"></a><span data-ttu-id="1ca09-103">Directrices básicas para diseñar aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="1ca09-103">Basic Guidelines for Designing COM+ Applications</span></span>

<span data-ttu-id="1ca09-104">Para sacar el máximo partido de COM+, hay algunas directrices básicas que puede usar al crear una aplicación:</span><span class="sxs-lookup"><span data-stu-id="1ca09-104">To take full advantage of COM+, there are a few basic guidelines you can use when creating an application:</span></span>

-   <span data-ttu-id="1ca09-105">**Modele su estado duradero como un esquema de base de datos, mediante la herramienta de base de datos que prefiera.**</span><span class="sxs-lookup"><span data-stu-id="1ca09-105">**Model your durable state as a database schema, using your database tool of choice.**</span></span> <span data-ttu-id="1ca09-106">Casi todas las aplicaciones necesitan mantener el estado durable.</span><span class="sxs-lookup"><span data-stu-id="1ca09-106">Almost every application needs to maintain durable state.</span></span> <span data-ttu-id="1ca09-107">Las bases de datos proporcionan los servicios necesarios para crear almacenamiento duradero y escalable del estado.</span><span class="sxs-lookup"><span data-stu-id="1ca09-107">Databases provide the services needed to create durable and scalable storage of state.</span></span> <span data-ttu-id="1ca09-108">Por lo tanto, el primer paso en la creación de una aplicación COM+ es modelar el estado duradero de la aplicación como algún tipo de esquema de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1ca09-108">Therefore, the first step in creating a COM+ application is to model the durable state of your application as some sort of database schema.</span></span> <span data-ttu-id="1ca09-109">En realidad, no importa qué base de datos se usa; la mayoría de las bases de datos comerciales son compatibles con COM+.</span><span class="sxs-lookup"><span data-stu-id="1ca09-109">It doesn't really matter what database you use; most commercial databases are compatible with COM+.</span></span> <span data-ttu-id="1ca09-110">Microsoft SQL Server es un buen ejemplo de una solución que puede usar.</span><span class="sxs-lookup"><span data-stu-id="1ca09-110">Microsoft SQL Server is a good example of one solution you could use.</span></span>

-   <span data-ttu-id="1ca09-111">**Modelar la lógica de la aplicación COM+ como un conjunto de interfaces COM.**</span><span class="sxs-lookup"><span data-stu-id="1ca09-111">**Model the logic of your COM+ application as a set of COM interfaces.**</span></span> <span data-ttu-id="1ca09-112">Una vez que tenga un esquema que represente la información de estado de la aplicación, modele los intercambios que se producen en la aplicación como interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="1ca09-112">Once you have a schema that represents the state information of the application, model the interchanges that happen in the application as COM interfaces.</span></span> <span data-ttu-id="1ca09-113">Estas interfaces modelan el comportamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1ca09-113">These interfaces will model the behavior of the application.</span></span> <span data-ttu-id="1ca09-114">Esta es también la fase de desarrollo cuando debe determinar qué servicios COM+ funcionan mejor para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="1ca09-114">This is also the development stage when you should determine which COM+ services work best for your application.</span></span>

-   <span data-ttu-id="1ca09-115">**Cree archivos dll de componentes que contengan componentes que usen el esquema de datos físico y expongan una vista lógica de los datos a otros componentes (el primer elemento de esta lista), así como los componentes que se implementan en términos del modelo de datos lógicos (el segundo elemento de esta lista).**</span><span class="sxs-lookup"><span data-stu-id="1ca09-115">**Build component DLLs that contain components that use the physical data schema and expose a logical view of the data to other components (the first item in this list), as well as components that are implemented in terms of the logical data model (the second item in this list).**</span></span> <span data-ttu-id="1ca09-116">Una vez que tenga la estructura de la información de estado y la lógica, puede empezar a escribir código y ahora puede escribir componentes COM basados en DLL que implementen las interfaces en términos del esquema definido.</span><span class="sxs-lookup"><span data-stu-id="1ca09-116">Once you have the structure of the logic and the state information, you can begin to write code and can now write DLL-based COM components that implement the interfaces in terms of the defined schema.</span></span> <span data-ttu-id="1ca09-117">Los componentes simplemente actúan como manipuladores para trabajar con la información de la base de datos y los archivos dll de componentes permiten compilar una aplicación COM+ que funcione y que se escale correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ca09-117">Your components simply act as manipulators for working with your database information, and your component DLLs enable you build a COM+ application that works and that scales successfully.</span></span>

-   <span data-ttu-id="1ca09-118">**Implemente los componentes en el entorno COM+ mediante los servicios COM+ que ha seleccionado.**</span><span class="sxs-lookup"><span data-stu-id="1ca09-118">**Deploy the components in the COM+ environment using the COM+ services you've selected.**</span></span> <span data-ttu-id="1ca09-119">Después de compilar la aplicación, puede implementar la aplicación en un clúster de red o de servidor.</span><span class="sxs-lookup"><span data-stu-id="1ca09-119">Once you have built the application, you can then deploy the application across a network or server cluster.</span></span> <span data-ttu-id="1ca09-120">Ahora puede tomar decisiones basadas en recursos disponibles y puede adaptar cada componente para obtener el máximo rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1ca09-120">You can now make decisions based on resources available, and you can tailor each component for maximum performance.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ca09-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ca09-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ca09-122">Hipótesis y principios de diseño de COM+</span><span class="sxs-lookup"><span data-stu-id="1ca09-122">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="1ca09-123">Diseñar la aplicación COM+ mediante UML</span><span class="sxs-lookup"><span data-stu-id="1ca09-123">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="1ca09-124">Sugerencias de diseño generales para el uso de COM+</span><span class="sxs-lookup"><span data-stu-id="1ca09-124">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="1ca09-125">Optimizar interacciones con el nivel de lógica de negocios de COM+</span><span class="sxs-lookup"><span data-stu-id="1ca09-125">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="1ca09-126">Otras herramientas de Microsoft para compilar aplicaciones distribuidas</span><span class="sxs-lookup"><span data-stu-id="1ca09-126">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



