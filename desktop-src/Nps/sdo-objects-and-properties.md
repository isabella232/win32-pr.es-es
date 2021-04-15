---
title: Objetos y propiedades
description: Las características de un objeto en SDO se determinan mediante las propiedades del objeto y los valores asociados a esas propiedades.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676429"
---
# <a name="objects-and-properties"></a><span data-ttu-id="66566-103">Objetos y propiedades</span><span class="sxs-lookup"><span data-stu-id="66566-103">Objects and Properties</span></span>

<span data-ttu-id="66566-104">Las características de un objeto en SDO se determinan mediante las propiedades del objeto y los valores asociados a esas propiedades.</span><span class="sxs-lookup"><span data-stu-id="66566-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="66566-105">A diferencia de otros modelos de objetos, los propios objetos SDO no tienen métodos.</span><span class="sxs-lookup"><span data-stu-id="66566-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="66566-106">Sin embargo, los objetos SDO exponen interfaces COM que proporcionan métodos.</span><span class="sxs-lookup"><span data-stu-id="66566-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="66566-107">Los objetos de SDO exponen la interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) que proporciona métodos para manipular las propiedades de los objetos.</span><span class="sxs-lookup"><span data-stu-id="66566-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="66566-108">Para obtener acceso a las propiedades del objeto, obtenga una interfaz **ISdo** para el objeto y use los métodos de la interfaz [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) y [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) para recuperar y establecer los valores de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="66566-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="66566-109">El tema [recuperar un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene código de ejemplo que muestra cómo obtener la interfaz **ISdo** para un objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="66566-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="66566-110">Después de realizar cambios en las propiedades de un objeto, use el método [**ISdo:: Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) para escribir los cambios en el almacenamiento persistente para el objeto.</span><span class="sxs-lookup"><span data-stu-id="66566-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="66566-111">Puede cancelar los cambios realizados en las propiedades de un objeto antes de llamar a **ISdo:: Apply** llamando al método [**ISdo:: restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) .</span><span class="sxs-lookup"><span data-stu-id="66566-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="66566-112">Este método restaura los valores de las propiedades de un objeto desde el almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="66566-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="66566-113">En la tabla siguiente se muestran los tipos de enumeración que enumeran las propiedades de algunos de los objetos de SDO.</span><span class="sxs-lookup"><span data-stu-id="66566-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="66566-114">Object</span><span class="sxs-lookup"><span data-stu-id="66566-114">Object</span></span>                                 | <span data-ttu-id="66566-115">Tipo de enumeración</span><span class="sxs-lookup"><span data-stu-id="66566-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="66566-116">Todos los objetos SDO</span><span class="sxs-lookup"><span data-stu-id="66566-116">All SDO objects</span></span>                        | [<span data-ttu-id="66566-117">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="66566-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="66566-118">Objeto de usuario</span><span class="sxs-lookup"><span data-stu-id="66566-118">User Object</span></span>                            | [<span data-ttu-id="66566-119">**USERPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="66566-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="66566-120">Objeto de servicio (servidor de directivas de redes)</span><span class="sxs-lookup"><span data-stu-id="66566-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="66566-121">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="66566-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="66566-122">Objeto de protocolo RADIUS de Microsoft</span><span class="sxs-lookup"><span data-stu-id="66566-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="66566-123">**RADIUSPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="66566-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="66566-124">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="66566-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="66566-125">Colecciones</span><span class="sxs-lookup"><span data-stu-id="66566-125">Collections</span></span>

<span data-ttu-id="66566-126">A menudo, los objetos se agrupan en colecciones.</span><span class="sxs-lookup"><span data-stu-id="66566-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="66566-127">La API SDO proporciona funcionalidad, a través de la interfaz de [**colección ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , para enumerar los objetos de una colección y para agregar y eliminar objetos de una colección.</span><span class="sxs-lookup"><span data-stu-id="66566-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="66566-128">El acceso a una colección se obtiene mediante la recuperación de una propiedad de colección en el objeto que contiene la colección.</span><span class="sxs-lookup"><span data-stu-id="66566-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="66566-129">Para obtener más información, vea la sección [jerarquía del modelo de objetos](/windows/desktop/Nps/sdo-object-model-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="66566-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="66566-130">El tipo de datos para todas las propiedades que se corresponden con las recopilaciones es VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="66566-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66566-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66566-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66566-132">Jerarquía del modelo de objetos SDO</span><span class="sxs-lookup"><span data-stu-id="66566-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="66566-133">Atributos compatibles con SDO</span><span class="sxs-lookup"><span data-stu-id="66566-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 