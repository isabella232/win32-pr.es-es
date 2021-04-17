---
description: Contiene una lista de los servidores en proceso registrados con el sistema. Contiene un objeto para cada componente que se registra como un servidor en proceso.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Colección InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714795"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="a5073-104">Colección InprocServers</span><span class="sxs-lookup"><span data-stu-id="a5073-104">InprocServers collection</span></span>

<span data-ttu-id="a5073-105">Contiene una lista de los servidores en proceso registrados con el sistema.</span><span class="sxs-lookup"><span data-stu-id="a5073-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="a5073-106">Contiene un objeto para cada componente que se registra como un servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="a5073-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="a5073-107">Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="a5073-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="a5073-108">Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="a5073-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a5073-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5073-109">Members</span></span>

<span data-ttu-id="a5073-110">La colección **InprocServers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="a5073-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a5073-111">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="a5073-111">Related Collections</span></span>

<span data-ttu-id="a5073-112">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="a5073-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a5073-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a5073-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a5073-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a5073-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a5073-115">Puede navegar a esta colección desde las colecciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a5073-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a5073-116">**Raíces**</span><span class="sxs-lookup"><span data-stu-id="a5073-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="a5073-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a5073-117">Properties</span></span>

<span data-ttu-id="a5073-118">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="a5073-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a5073-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="a5073-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="a5073-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="a5073-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="a5073-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="a5073-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="a5073-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="a5073-122">CLSID</span></span>



| <span data-ttu-id="a5073-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5073-123">Entry</span></span> | <span data-ttu-id="a5073-124">Value</span><span class="sxs-lookup"><span data-stu-id="a5073-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5073-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5073-125">Description</span></span>    | <span data-ttu-id="a5073-126">GUID del componente.</span><span class="sxs-lookup"><span data-stu-id="a5073-126">A GUID for the component.</span></span> <span data-ttu-id="a5073-127">Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="a5073-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a5073-128">Access</span><span class="sxs-lookup"><span data-stu-id="a5073-128">Access</span></span>         | <span data-ttu-id="a5073-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a5073-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="a5073-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5073-130">Type</span></span>           | <span data-ttu-id="a5073-131">String</span><span class="sxs-lookup"><span data-stu-id="a5073-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="a5073-132">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a5073-132">Default</span></span>        | <span data-ttu-id="a5073-133">N/D</span><span class="sxs-lookup"><span data-stu-id="a5073-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="a5073-134">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a5073-134">Minimum system</span></span> | <span data-ttu-id="a5073-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a5073-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="a5073-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="a5073-136">InprocServer32</span></span>



| <span data-ttu-id="a5073-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5073-137">Entry</span></span> | <span data-ttu-id="a5073-138">Value</span><span class="sxs-lookup"><span data-stu-id="a5073-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="a5073-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5073-139">Description</span></span>    | <span data-ttu-id="a5073-140">Ruta de acceso de archivo para el componente.</span><span class="sxs-lookup"><span data-stu-id="a5073-140">The file path for the component.</span></span> |
| <span data-ttu-id="a5073-141">Access</span><span class="sxs-lookup"><span data-stu-id="a5073-141">Access</span></span>         | <span data-ttu-id="a5073-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a5073-142">ReadOnly</span></span>                         |
| <span data-ttu-id="a5073-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5073-143">Type</span></span>           | <span data-ttu-id="a5073-144">String</span><span class="sxs-lookup"><span data-stu-id="a5073-144">String</span></span>                           |
| <span data-ttu-id="a5073-145">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a5073-145">Default</span></span>        | <span data-ttu-id="a5073-146">N/D</span><span class="sxs-lookup"><span data-stu-id="a5073-146">N/A</span></span>                              |
| <span data-ttu-id="a5073-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a5073-147">Minimum system</span></span> | <span data-ttu-id="a5073-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a5073-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="a5073-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="a5073-149">ProgID</span></span>



| <span data-ttu-id="a5073-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="a5073-150">Entry</span></span> | <span data-ttu-id="a5073-151">Value</span><span class="sxs-lookup"><span data-stu-id="a5073-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5073-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5073-152">Description</span></span>    | <span data-ttu-id="a5073-153">Nombre que identifica el componente.</span><span class="sxs-lookup"><span data-stu-id="a5073-153">A name identifying the component.</span></span> <span data-ttu-id="a5073-154">Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="a5073-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a5073-155">Access</span><span class="sxs-lookup"><span data-stu-id="a5073-155">Access</span></span>         | <span data-ttu-id="a5073-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a5073-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="a5073-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5073-157">Type</span></span>           | <span data-ttu-id="a5073-158">String</span><span class="sxs-lookup"><span data-stu-id="a5073-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="a5073-159">Predeterminado</span><span class="sxs-lookup"><span data-stu-id="a5073-159">Default</span></span>        | <span data-ttu-id="a5073-160">N/D</span><span class="sxs-lookup"><span data-stu-id="a5073-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="a5073-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a5073-161">Minimum system</span></span> | <span data-ttu-id="a5073-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a5073-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="a5073-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5073-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5073-164">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="a5073-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
