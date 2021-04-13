---
description: Contiene una lista de los servidores en proceso registrados con el sistema para los componentes de 32 bits en equipos de 64 bits. Contiene un objeto para cada componente.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Colección WOWInprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 43fceababaf6ced44a1ba3aef020900ed1afe4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538578"
---
# <a name="wowinprocservers-collection"></a><span data-ttu-id="01c27-104">Colección WOWInprocServers</span><span class="sxs-lookup"><span data-stu-id="01c27-104">WOWInprocServers collection</span></span>

<span data-ttu-id="01c27-105">Contiene una lista de los servidores en proceso registrados con el sistema para los componentes de 32 bits en equipos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="01c27-105">Contains a list of the in-process servers registered with the system for 32-bit components on 64-bit computers.</span></span> <span data-ttu-id="01c27-106">Contiene un objeto para cada componente.</span><span class="sxs-lookup"><span data-stu-id="01c27-106">It contains an object for each component.</span></span>

<span data-ttu-id="01c27-107">Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="01c27-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="01c27-108">Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="01c27-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="01c27-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="01c27-109">Members</span></span>

<span data-ttu-id="01c27-110">La colección **WOWInprocServers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="01c27-110">The **WOWInprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="01c27-111">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="01c27-111">Related Collections</span></span>

<span data-ttu-id="01c27-112">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="01c27-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="01c27-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="01c27-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="01c27-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="01c27-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="01c27-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="01c27-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="01c27-116">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="01c27-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="01c27-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01c27-117">Properties</span></span>

<span data-ttu-id="01c27-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="01c27-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="01c27-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="01c27-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="01c27-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="01c27-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="01c27-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="01c27-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="01c27-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="01c27-122">CLSID</span></span>



| <span data-ttu-id="01c27-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="01c27-123">Entry</span></span> | <span data-ttu-id="01c27-124">Value</span><span class="sxs-lookup"><span data-stu-id="01c27-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c27-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c27-125">Description</span></span>    | <span data-ttu-id="01c27-126">GUID del componente.</span><span class="sxs-lookup"><span data-stu-id="01c27-126">A GUID for the component.</span></span> <span data-ttu-id="01c27-127">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="01c27-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="01c27-128">Access</span><span class="sxs-lookup"><span data-stu-id="01c27-128">Access</span></span>         | <span data-ttu-id="01c27-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="01c27-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="01c27-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="01c27-130">Type</span></span>           | <span data-ttu-id="01c27-131">String</span><span class="sxs-lookup"><span data-stu-id="01c27-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="01c27-132">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="01c27-132">Default</span></span>        | <span data-ttu-id="01c27-133">N/D</span><span class="sxs-lookup"><span data-stu-id="01c27-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="01c27-134">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="01c27-134">Minimum system</span></span> | <span data-ttu-id="01c27-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01c27-135">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="01c27-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="01c27-136">InprocServer32</span></span>



| <span data-ttu-id="01c27-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="01c27-137">Entry</span></span> | <span data-ttu-id="01c27-138">Value</span><span class="sxs-lookup"><span data-stu-id="01c27-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="01c27-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c27-139">Description</span></span>    | <span data-ttu-id="01c27-140">Ruta de acceso de archivo para el componente.</span><span class="sxs-lookup"><span data-stu-id="01c27-140">The file path for the component.</span></span> |
| <span data-ttu-id="01c27-141">Access</span><span class="sxs-lookup"><span data-stu-id="01c27-141">Access</span></span>         | <span data-ttu-id="01c27-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="01c27-142">ReadOnly</span></span>                         |
| <span data-ttu-id="01c27-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="01c27-143">Type</span></span>           | <span data-ttu-id="01c27-144">String</span><span class="sxs-lookup"><span data-stu-id="01c27-144">String</span></span>                           |
| <span data-ttu-id="01c27-145">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="01c27-145">Default</span></span>        | <span data-ttu-id="01c27-146">N/D</span><span class="sxs-lookup"><span data-stu-id="01c27-146">N/A</span></span>                              |
| <span data-ttu-id="01c27-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="01c27-147">Minimum system</span></span> | <span data-ttu-id="01c27-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01c27-148">Windows XP</span></span>                       |



 

### <a name="progid"></a><span data-ttu-id="01c27-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="01c27-149">ProgID</span></span>



| <span data-ttu-id="01c27-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="01c27-150">Entry</span></span> | <span data-ttu-id="01c27-151">Value</span><span class="sxs-lookup"><span data-stu-id="01c27-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c27-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c27-152">Description</span></span>    | <span data-ttu-id="01c27-153">Nombre que identifica el componente.</span><span class="sxs-lookup"><span data-stu-id="01c27-153">A name identifying the component.</span></span> <span data-ttu-id="01c27-154">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="01c27-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="01c27-155">Access</span><span class="sxs-lookup"><span data-stu-id="01c27-155">Access</span></span>         | <span data-ttu-id="01c27-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="01c27-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="01c27-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="01c27-157">Type</span></span>           | <span data-ttu-id="01c27-158">String</span><span class="sxs-lookup"><span data-stu-id="01c27-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="01c27-159">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="01c27-159">Default</span></span>        | <span data-ttu-id="01c27-160">N/D</span><span class="sxs-lookup"><span data-stu-id="01c27-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="01c27-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="01c27-161">Minimum system</span></span> | <span data-ttu-id="01c27-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01c27-162">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="01c27-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="01c27-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c27-164">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="01c27-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
