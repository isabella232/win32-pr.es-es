---
description: Contiene una lista de los protocolos que va a utilizar DCOM. Contiene un objeto para cada protocolo.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Colección DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496163"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="231ba-104">Colección DCOMProtocols</span><span class="sxs-lookup"><span data-stu-id="231ba-104">DCOMProtocols collection</span></span>

<span data-ttu-id="231ba-105">Contiene una lista de los protocolos que va a utilizar DCOM.</span><span class="sxs-lookup"><span data-stu-id="231ba-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="231ba-106">Contiene un objeto para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="231ba-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="231ba-107">Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="231ba-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="231ba-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="231ba-108">Members</span></span>

<span data-ttu-id="231ba-109">La colección **DCOMProtocols** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="231ba-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="231ba-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="231ba-110">Related Collections</span></span>

<span data-ttu-id="231ba-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="231ba-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="231ba-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="231ba-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="231ba-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="231ba-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="231ba-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="231ba-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="231ba-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="231ba-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="231ba-116">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="231ba-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="231ba-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="231ba-117">Properties</span></span>

<span data-ttu-id="231ba-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="231ba-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="231ba-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="231ba-119">Name</span></span>](#name)
-   [<span data-ttu-id="231ba-120">Pedido</span><span class="sxs-lookup"><span data-stu-id="231ba-120">Order</span></span>](#order)
-   [<span data-ttu-id="231ba-121">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="231ba-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="231ba-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="231ba-122">Name</span></span>



| <span data-ttu-id="231ba-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="231ba-123">Entry</span></span> | <span data-ttu-id="231ba-124">Value</span><span class="sxs-lookup"><span data-stu-id="231ba-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="231ba-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="231ba-125">Description</span></span>    | <span data-ttu-id="231ba-126">El nombre del protocolo</span><span class="sxs-lookup"><span data-stu-id="231ba-126">The name of the protocol.</span></span> <span data-ttu-id="231ba-127">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="231ba-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="231ba-128">Access</span><span class="sxs-lookup"><span data-stu-id="231ba-128">Access</span></span>         | <span data-ttu-id="231ba-129">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="231ba-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="231ba-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="231ba-130">Type</span></span>           | <span data-ttu-id="231ba-131">String</span><span class="sxs-lookup"><span data-stu-id="231ba-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="231ba-132">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="231ba-132">Default</span></span>        | <span data-ttu-id="231ba-133">"Nuevo protocolo"</span><span class="sxs-lookup"><span data-stu-id="231ba-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="231ba-134">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="231ba-134">Minimum system</span></span> | <span data-ttu-id="231ba-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="231ba-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="231ba-136">Pedido</span><span class="sxs-lookup"><span data-stu-id="231ba-136">Order</span></span>



| <span data-ttu-id="231ba-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="231ba-137">Entry</span></span> | <span data-ttu-id="231ba-138">Value</span><span class="sxs-lookup"><span data-stu-id="231ba-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="231ba-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="231ba-139">Description</span></span>    | <span data-ttu-id="231ba-140">El orden en el que se va a probar el protocolo.</span><span class="sxs-lookup"><span data-stu-id="231ba-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="231ba-141">Access</span><span class="sxs-lookup"><span data-stu-id="231ba-141">Access</span></span>         | <span data-ttu-id="231ba-142">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="231ba-142">ReadWrite</span></span>                               |
| <span data-ttu-id="231ba-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="231ba-143">Type</span></span>           | <span data-ttu-id="231ba-144">Long (0-65000)</span><span class="sxs-lookup"><span data-stu-id="231ba-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="231ba-145">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="231ba-145">Default</span></span>        | <span data-ttu-id="231ba-146">0</span><span class="sxs-lookup"><span data-stu-id="231ba-146">0</span></span>                                       |
| <span data-ttu-id="231ba-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="231ba-147">Minimum system</span></span> | <span data-ttu-id="231ba-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="231ba-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="231ba-149">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="231ba-149">ProtocolCode</span></span>



| <span data-ttu-id="231ba-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="231ba-150">Entry</span></span> | <span data-ttu-id="231ba-151">Value</span><span class="sxs-lookup"><span data-stu-id="231ba-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="231ba-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="231ba-152">Description</span></span>    | <span data-ttu-id="231ba-153">Código que especifica la secuencia de protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="231ba-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="231ba-154">Entre los códigos de protocolo admitidos se incluyen los siguientes: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX.</span><span class="sxs-lookup"><span data-stu-id="231ba-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="231ba-155">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="231ba-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="231ba-156">Access</span><span class="sxs-lookup"><span data-stu-id="231ba-156">Access</span></span>         | <span data-ttu-id="231ba-157">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="231ba-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="231ba-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="231ba-158">Type</span></span>           | <span data-ttu-id="231ba-159">String</span><span class="sxs-lookup"><span data-stu-id="231ba-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="231ba-160">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="231ba-160">Default</span></span>        | <span data-ttu-id="231ba-161">""</span><span class="sxs-lookup"><span data-stu-id="231ba-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="231ba-162">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="231ba-162">Minimum system</span></span> | <span data-ttu-id="231ba-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="231ba-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="231ba-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="231ba-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231ba-165">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="231ba-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
