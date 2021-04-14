---
description: Recupera información de error extendida con respecto a métodos que se ocupan de varios objetos, como rellenar y SaveChanges en el objeto COMAdminCatalogCollection, y métodos para instalar, importar o exportar aplicaciones o componentes en el objeto COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Colección ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496457"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="43c2c-103">Colección ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="43c2c-103">ErrorInfo collection</span></span>

<span data-ttu-id="43c2c-104">Recupera información de error extendida con respecto a métodos que se ocupan de varios objetos, como [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , y métodos para instalar, importar o exportar aplicaciones o componentes en el objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="43c2c-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="43c2c-105">Use el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en un [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para tener acceso a la colección **errorInfo** asociada a la colección original que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="43c2c-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="43c2c-106">Debe llamar a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en **errorInfo** inmediatamente después de que se produzca un error. de lo contrario, se pierde la información de error.</span><span class="sxs-lookup"><span data-stu-id="43c2c-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="43c2c-107">Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="43c2c-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="43c2c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="43c2c-108">Members</span></span>

<span data-ttu-id="43c2c-109">La colección **errorInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.</span><span class="sxs-lookup"><span data-stu-id="43c2c-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="43c2c-110">Colecciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="43c2c-110">Related Collections</span></span>

<span data-ttu-id="43c2c-111">Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:</span><span class="sxs-lookup"><span data-stu-id="43c2c-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="43c2c-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="43c2c-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="43c2c-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="43c2c-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="43c2c-114">Puede navegar a esta colección desde cada colección, excepto por **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)y [**WOWInprocServers**](wowinprocservers.md).</span><span class="sxs-lookup"><span data-stu-id="43c2c-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="43c2c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43c2c-115">Properties</span></span>

<span data-ttu-id="43c2c-116">El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:</span><span class="sxs-lookup"><span data-stu-id="43c2c-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="43c2c-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="43c2c-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="43c2c-118">MajorRef</span><span class="sxs-lookup"><span data-stu-id="43c2c-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="43c2c-119">MinorRef</span><span class="sxs-lookup"><span data-stu-id="43c2c-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="43c2c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="43c2c-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="43c2c-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="43c2c-121">ErrorCode</span></span>



| <span data-ttu-id="43c2c-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="43c2c-122">Entry</span></span> | <span data-ttu-id="43c2c-123">Value</span><span class="sxs-lookup"><span data-stu-id="43c2c-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="43c2c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="43c2c-124">Description</span></span>    | <span data-ttu-id="43c2c-125">Código de error para el objeto o archivo.</span><span class="sxs-lookup"><span data-stu-id="43c2c-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="43c2c-126">Access</span><span class="sxs-lookup"><span data-stu-id="43c2c-126">Access</span></span>         | <span data-ttu-id="43c2c-127">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="43c2c-127">ReadOnly</span></span>                               |
| <span data-ttu-id="43c2c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="43c2c-128">Type</span></span>           | <span data-ttu-id="43c2c-129">String</span><span class="sxs-lookup"><span data-stu-id="43c2c-129">String</span></span>                                 |
| <span data-ttu-id="43c2c-130">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="43c2c-130">Default</span></span>        | <span data-ttu-id="43c2c-131">None</span><span class="sxs-lookup"><span data-stu-id="43c2c-131">None</span></span>                                   |
| <span data-ttu-id="43c2c-132">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="43c2c-132">Minimum system</span></span> | <span data-ttu-id="43c2c-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="43c2c-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="43c2c-134">MajorRef</span><span class="sxs-lookup"><span data-stu-id="43c2c-134">MajorRef</span></span>



| <span data-ttu-id="43c2c-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="43c2c-135">Entry</span></span> | <span data-ttu-id="43c2c-136">Value</span><span class="sxs-lookup"><span data-stu-id="43c2c-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c2c-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="43c2c-137">Description</span></span>    | <span data-ttu-id="43c2c-138">Valor de la propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) para el objeto que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="43c2c-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="43c2c-139">Por ejemplo, si se produce un error en una llamada a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para una colección en un objeto determinado de la colección, el valor de la propiedad **clave** para ese objeto se muestra como el valor de MajorRef.</span><span class="sxs-lookup"><span data-stu-id="43c2c-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="43c2c-140">Utilice esta propiedad para ver el elemento que no se puede actualizar o para buscar el componente o DLL que no se puede instalar.</span><span class="sxs-lookup"><span data-stu-id="43c2c-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="43c2c-141">Access</span><span class="sxs-lookup"><span data-stu-id="43c2c-141">Access</span></span>         | <span data-ttu-id="43c2c-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="43c2c-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="43c2c-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="43c2c-143">Type</span></span>           | <span data-ttu-id="43c2c-144">String</span><span class="sxs-lookup"><span data-stu-id="43c2c-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="43c2c-145">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="43c2c-145">Default</span></span>        | <span data-ttu-id="43c2c-146">None</span><span class="sxs-lookup"><span data-stu-id="43c2c-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="43c2c-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="43c2c-147">Minimum system</span></span> | <span data-ttu-id="43c2c-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="43c2c-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="43c2c-149">MinorRef</span><span class="sxs-lookup"><span data-stu-id="43c2c-149">MinorRef</span></span>



| <span data-ttu-id="43c2c-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="43c2c-150">Entry</span></span> | <span data-ttu-id="43c2c-151">Value</span><span class="sxs-lookup"><span data-stu-id="43c2c-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c2c-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="43c2c-152">Description</span></span>    | <span data-ttu-id="43c2c-153">Una especificación precisa del elemento que tiene un error, como un nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="43c2c-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="43c2c-154">Si se producen varios errores o en contextos en los que no se aplica, MinorRef es <Invalid> .</span><span class="sxs-lookup"><span data-stu-id="43c2c-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="43c2c-155">Access</span><span class="sxs-lookup"><span data-stu-id="43c2c-155">Access</span></span>         | <span data-ttu-id="43c2c-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="43c2c-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="43c2c-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="43c2c-157">Type</span></span>           | <span data-ttu-id="43c2c-158">String</span><span class="sxs-lookup"><span data-stu-id="43c2c-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="43c2c-159">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="43c2c-159">Default</span></span>        | <span data-ttu-id="43c2c-160">None</span><span class="sxs-lookup"><span data-stu-id="43c2c-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="43c2c-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="43c2c-161">Minimum system</span></span> | <span data-ttu-id="43c2c-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="43c2c-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="43c2c-163">Nombre</span><span class="sxs-lookup"><span data-stu-id="43c2c-163">Name</span></span>



| <span data-ttu-id="43c2c-164">Entrada</span><span class="sxs-lookup"><span data-stu-id="43c2c-164">Entry</span></span> | <span data-ttu-id="43c2c-165">Value</span><span class="sxs-lookup"><span data-stu-id="43c2c-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c2c-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="43c2c-166">Description</span></span>    | <span data-ttu-id="43c2c-167">Nombre del objeto o archivo que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="43c2c-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="43c2c-168">Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección.</span><span class="sxs-lookup"><span data-stu-id="43c2c-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="43c2c-169">Access</span><span class="sxs-lookup"><span data-stu-id="43c2c-169">Access</span></span>         | <span data-ttu-id="43c2c-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="43c2c-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="43c2c-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="43c2c-171">Type</span></span>           | <span data-ttu-id="43c2c-172">String</span><span class="sxs-lookup"><span data-stu-id="43c2c-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="43c2c-173">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="43c2c-173">Default</span></span>        | <span data-ttu-id="43c2c-174">None</span><span class="sxs-lookup"><span data-stu-id="43c2c-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="43c2c-175">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="43c2c-175">Minimum system</span></span> | <span data-ttu-id="43c2c-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="43c2c-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="43c2c-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="43c2c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c2c-178">Colecciones de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="43c2c-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
