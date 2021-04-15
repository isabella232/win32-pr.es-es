---
description: La biblioteca COMAdmin (comadmin.dll) proporciona tres clases, cada una de las cuales implementa una interfaz dual COM.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Descripción resumida de las clases COMAdmin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666180"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="72ac2-103">Descripción resumida de las clases COMAdmin</span><span class="sxs-lookup"><span data-stu-id="72ac2-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="72ac2-104">La biblioteca COMAdmin (comadmin.dll) proporciona tres clases, cada una de las cuales implementa una interfaz dual COM.</span><span class="sxs-lookup"><span data-stu-id="72ac2-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="72ac2-105">Los objetos creados a partir de estas clases se utilizan para obtener acceso al catálogo, para representar colecciones en el catálogo y para representar los elementos contenidos dentro de las colecciones.</span><span class="sxs-lookup"><span data-stu-id="72ac2-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="72ac2-106">COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="72ac2-106">COMAdminCatalog</span></span>

<span data-ttu-id="72ac2-107">La clase [**COMAdminCatalog**](comadmincatalog.md) representa el propio catálogo.</span><span class="sxs-lookup"><span data-stu-id="72ac2-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="72ac2-108">Un objeto creado a partir de **COMAdminCatalog** es el objeto fundamental que se usa en la administración mediante programación.</span><span class="sxs-lookup"><span data-stu-id="72ac2-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="72ac2-109">Además de establecer la conexión básica con el servidor de catálogo al crear una instancia, **COMAdminCatalog** proporciona métodos que le permiten hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="72ac2-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="72ac2-110">Obtener recopilaciones en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="72ac2-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="72ac2-111">Conéctese al servidor de catálogo en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="72ac2-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="72ac2-112">Instalar, exportar, iniciar, apagar y obtener información relacionada con las aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="72ac2-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="72ac2-113">Instalar componentes en aplicaciones COM+ y obtener información sobre los componentes.</span><span class="sxs-lookup"><span data-stu-id="72ac2-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="72ac2-114">Iniciar, detener o actualizar los servicios que se ejecutan en la máquina.</span><span class="sxs-lookup"><span data-stu-id="72ac2-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="72ac2-115">Actualice, restaure o haga una copia de seguridad de la información del catálogo.</span><span class="sxs-lookup"><span data-stu-id="72ac2-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="72ac2-116">En COM+ 1,0, la clase [**COMAdminCatalog**](comadmincatalog.md) implementa la interfaz [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="72ac2-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="72ac2-117">En COM+ 1,5, la clase **COMAdminCatalog** implementa [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) como su interfaz predeterminada.</span><span class="sxs-lookup"><span data-stu-id="72ac2-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="72ac2-118">COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="72ac2-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="72ac2-119">La clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) representa cualquier colección del catálogo, proporcionando una cadena que asigna un nombre a la colección determinada en el momento de la creación de instancias de objeto.</span><span class="sxs-lookup"><span data-stu-id="72ac2-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="72ac2-120">(Las colecciones de catálogos disponibles se denominan en la tabla de [colecciones de administración de com+](com--administration-collections.md)). Los objetos se crean a partir de esta clase al recuperar una colección de nivel superior llamando al método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) del objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="72ac2-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="72ac2-121">Estos objetos también se crean al recuperar una colección secundaria llamando al método **GetCollection** de su objeto de colección primario.</span><span class="sxs-lookup"><span data-stu-id="72ac2-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="72ac2-122">Los objetos **COMAdminCatalogCollection** permiten hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="72ac2-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="72ac2-123">Enumerar los elementos incluidos en la colección.</span><span class="sxs-lookup"><span data-stu-id="72ac2-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="72ac2-124">Recupera un elemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="72ac2-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="72ac2-125">Agregar o quitar elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="72ac2-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="72ac2-126">Guardar o descartar los cambios pendientes realizados en la colección o en los elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="72ac2-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="72ac2-127">Obtener una colección diferente en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="72ac2-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="72ac2-128">La clase [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa la interfaz [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) .</span><span class="sxs-lookup"><span data-stu-id="72ac2-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="72ac2-129">COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="72ac2-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="72ac2-130">La clase [**COMAdminCatalogObject**](comadmincatalogobject.md) representa cualquier elemento incluido en una colección.</span><span class="sxs-lookup"><span data-stu-id="72ac2-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="72ac2-131">Los objetos se crean a partir de esta clase al obtener un elemento a través de la propiedad [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) de un objeto de colección de catálogos.</span><span class="sxs-lookup"><span data-stu-id="72ac2-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="72ac2-132">Los objetos creados a partir de la clase **COMAdminCatalogObject** permiten hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="72ac2-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="72ac2-133">Obtiene o establece las propiedades admitidas por el elemento que se va a utilizar para representar el objeto.</span><span class="sxs-lookup"><span data-stu-id="72ac2-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="72ac2-134">Obtenga información sobre el elemento y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="72ac2-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="72ac2-135">La clase [**COMAdminCatalogObject**](comadmincatalogobject.md) implementa la interfaz [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="72ac2-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72ac2-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="72ac2-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72ac2-137">Obtener acceso al catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="72ac2-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="72ac2-138">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="72ac2-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



