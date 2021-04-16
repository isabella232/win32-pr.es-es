---
description: Navegar por la jerarquía de la colección de COM+
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: Navegar por la jerarquía de la colección de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677218"
---
# <a name="navigating-the-com-collection-hierarchy"></a><span data-ttu-id="a3598-103">Navegar por la jerarquía de la colección de COM+</span><span class="sxs-lookup"><span data-stu-id="a3598-103">Navigating the COM+ Collection Hierarchy</span></span>

<span data-ttu-id="a3598-104">Algunas colecciones se pueden recuperar fácilmente mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="a3598-104">Some collections you can retrieve easily by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="a3598-105">Este método recupera una colección "de nivel superior"; es decir, una colección como [**aplicaciones**](applications.md), que se sitúa por sí misma y que es única y no se encuentra lógicamente en otra colección.</span><span class="sxs-lookup"><span data-stu-id="a3598-105">This method retrieves a "top-level" collection; that is, a collection such as [**Applications**](applications.md), which stands on its own and which is unique and not logically subsumed under another collection.</span></span>

<span data-ttu-id="a3598-106">Sin embargo, muchas colecciones se integran lógicamente en otra colección porque contienen elementos que forman parte de una estructura mayor.</span><span class="sxs-lookup"><span data-stu-id="a3598-106">Many collections, however, are logically subsumed under another collection because they contain elements that are part of some larger structure.</span></span> <span data-ttu-id="a3598-107">Por ejemplo, la colección de [**componentes**](components.md) se incluye o se relaciona en la colección de [**aplicaciones**](applications.md) porque contiene los componentes instalados en una aplicación com+ determinada, que se corresponde con un elemento de la colección de **aplicaciones** .</span><span class="sxs-lookup"><span data-stu-id="a3598-107">For example, the [**Components**](components.md) collection is subsumed, or related, to the [**Applications**](applications.md) collection because it contains the components installed in a particular COM+ application, which itself corresponds to an item in the **Applications** collection.</span></span> <span data-ttu-id="a3598-108">Las colecciones relacionadas como esta no son únicas; hay una colección de **componentes** para cada aplicación distinta.</span><span class="sxs-lookup"><span data-stu-id="a3598-108">Related collections such as this are not unique; there is a **Components** collection for each distinct application.</span></span>

<span data-ttu-id="a3598-109">Por lo tanto, las colecciones se organizan en una estructura jerárquica que corresponde de forma natural a las relaciones lógicas entre los elementos que contienen.</span><span class="sxs-lookup"><span data-stu-id="a3598-109">Therefore, collections are arranged in a hierarchical structure that corresponds naturally to the logical relationships between the items they contain.</span></span> <span data-ttu-id="a3598-110">Puede encontrar un diagrama de la jerarquía de la colección en [colecciones de administración de com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="a3598-110">A diagram of the collection hierarchy can be found at [COM+ Administration Collections](com--administration-collections.md).</span></span> <span data-ttu-id="a3598-111">Para muchos de los elementos que desea configurar mediante los objetos COMAdmin, debe desplazarse por una parte de la jerarquía de la colección para recuperar el elemento adecuado.</span><span class="sxs-lookup"><span data-stu-id="a3598-111">For many of the elements that you want to configure using the COMAdmin objects, you need to navigate through some portion of the collection hierarchy to retrieve the appropriate item.</span></span>

<span data-ttu-id="a3598-112">Esto significa que, en la práctica, si desea obtener un elemento en una colección relacionada, debe repasar en primer lugar todas las colecciones de nivel superior necesarias, integrador indicado.</span><span class="sxs-lookup"><span data-stu-id="a3598-112">What this means in practice is that if you want to get an item in a related collection, you need to go through all the necessary higher level, subsuming collections first.</span></span> <span data-ttu-id="a3598-113">Y para recuperar una colección relacionada, debe recuperar el elemento específico en la colección primaria en la que está relacionada la colección secundaria.</span><span class="sxs-lookup"><span data-stu-id="a3598-113">And to retrieve a related collection, you need to retrieve the specific item in the parent collection to which the child collection is related.</span></span> <span data-ttu-id="a3598-114">Por ejemplo, si desea configurar un elemento correspondiente a un componente de una aplicación COM+ determinada, debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="a3598-114">For example, if you want to configure an item corresponding to a component in a particular COM+ application, you must perform the following steps:</span></span>

1.  <span data-ttu-id="a3598-115">Obtener la colección de [**aplicaciones**](applications.md) y rellenarla.</span><span class="sxs-lookup"><span data-stu-id="a3598-115">Get the [**Applications**](applications.md) collection and populate it.</span></span>
2.  <span data-ttu-id="a3598-116">Enumere el contenido de la colección de [**aplicaciones**](applications.md) hasta llegar al elemento correspondiente a la aplicación com+ correcta.</span><span class="sxs-lookup"><span data-stu-id="a3598-116">Enumerate through the contents of the [**Applications**](applications.md) collection until you get to the item corresponding to the correct COM+ application.</span></span>
3.  <span data-ttu-id="a3598-117">Obtener y rellenar la colección de [**componentes**](components.md) para esa aplicación com+ en particular.</span><span class="sxs-lookup"><span data-stu-id="a3598-117">Get and populate the [**Components**](components.md) collection for that particular COM+ application.</span></span>
4.  <span data-ttu-id="a3598-118">Enumere el contenido de la colección de [**componentes**](components.md) hasta llegar al elemento correspondiente al componente correcto.</span><span class="sxs-lookup"><span data-stu-id="a3598-118">Enumerate through the contents of the [**Components**](components.md) collection until you get to the item corresponding to the correct component.</span></span>

<span data-ttu-id="a3598-119">En el siguiente ejemplo de Microsoft Visual Basic se muestra cómo realizar los pasos anteriores:</span><span class="sxs-lookup"><span data-stu-id="a3598-119">The following Microsoft Visual Basic example shows how to perform the preceding steps:</span></span>


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



<span data-ttu-id="a3598-120">En el ejemplo anterior se usan dos métodos **GetCollection** distintos.</span><span class="sxs-lookup"><span data-stu-id="a3598-120">Two distinct **GetCollection** methods are used in the preceding example.</span></span> <span data-ttu-id="a3598-121">La primera se expone mediante [**COMAdminCatalog**](comadmincatalog.md) y se usa para obtener una colección de nivel superior (en este caso, "Applications").</span><span class="sxs-lookup"><span data-stu-id="a3598-121">The first is exposed by [**COMAdminCatalog**](comadmincatalog.md) and is used to get a top-level collection—in this case, "Applications".</span></span> <span data-ttu-id="a3598-122">La segunda se expone mediante [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y se usa para obtener una colección relacionada con la colección actual; para indicar exactamente qué colección desea, pase el nombre "Components" y el valor de la propiedad clave del objeto primario.</span><span class="sxs-lookup"><span data-stu-id="a3598-122">The second is exposed by [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and is used to get a collection related to the present collection; you indicate precisely which collection you want by passing in the name "Components" and the Key property value of the parent object.</span></span> <span data-ttu-id="a3598-123">El valor de la propiedad clave suele ser un nombre o un GUID que identifica de forma única el objeto. Este valor se identifica en la documentación de cada colección.</span><span class="sxs-lookup"><span data-stu-id="a3598-123">The Key property value is often a name or a GUID that uniquely identifies the object; this value is identified in the documentation for each collection.</span></span>

<span data-ttu-id="a3598-124">En el caso más general, debe obtener las colecciones relacionadas de forma iterativa hacia abajo en la jerarquía de la colección hasta que recupere la colección que desea.</span><span class="sxs-lookup"><span data-stu-id="a3598-124">In the most general case, you need to get related collections iteratively down the collection hierarchy until you retrieve the collection you want.</span></span> <span data-ttu-id="a3598-125">Los pasos que debería seguir el mismo modelo general, repetidamente.</span><span class="sxs-lookup"><span data-stu-id="a3598-125">The steps you would take follow the same general model, repetitively.</span></span> <span data-ttu-id="a3598-126">Para obtener una lista completa de las colecciones, consulte [colecciones de administración de com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="a3598-126">For a complete list of collections, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="a3598-127">En algunos casos, es posible que desee usar un método abreviado la segunda vez que siga una ruta de acceso a través de la jerarquía de la colección.</span><span class="sxs-lookup"><span data-stu-id="a3598-127">In some cases, you might want to use a shortcut method the second time you follow a path through the collection hierarchy.</span></span> <span data-ttu-id="a3598-128">Puede usar este método solo después de haber almacenado en caché todos los valores de clave que intervienen.</span><span class="sxs-lookup"><span data-stu-id="a3598-128">You can use this method only after you have already cached all the intervening Key values.</span></span> <span data-ttu-id="a3598-129">Para obtener más información, vea [**ICOMAdminCatalog:: GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span><span class="sxs-lookup"><span data-stu-id="a3598-129">For details, see [**ICOMAdminCatalog::GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3598-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3598-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3598-131">Rellenar colecciones de COM+</span><span class="sxs-lookup"><span data-stu-id="a3598-131">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="a3598-132">Consultar colecciones relacionadas disponibles</span><span class="sxs-lookup"><span data-stu-id="a3598-132">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="a3598-133">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="a3598-133">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



