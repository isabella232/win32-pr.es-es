---
description: Un objeto SWbemQualifierSet es una colección de objetos SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objeto SWbemQualifierSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083380"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="f9745-103">Objeto SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="f9745-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="f9745-104">Un objeto **SWbemQualifierSet** es una colección de objetos [**SWbemQualifier**](swbemqualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="f9745-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="f9745-105">Los elementos se agregan a la colección mediante el método [**Add**](swbemqualifierset-add.md) , se recuperan de la colección mediante el método [**Item**](swbemqualifierset-item.md) y se quitan de la colección mediante el método [**Remove**](swbemqualifierset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="f9745-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="f9745-106">Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="f9745-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="f9745-107">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="f9745-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="f9745-108">Los objetos [**SWbemQualifier**](swbemqualifier.md) que componen una colección **SWbemQualifierSet** describen los calificadores adjuntos a una clase WMI, una instancia, un método o un parámetro de método.</span><span class="sxs-lookup"><span data-stu-id="f9745-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="f9745-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9745-109">Members</span></span>

<span data-ttu-id="f9745-110">El objeto **SWbemQualifierSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f9745-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="f9745-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9745-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9745-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9745-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9745-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f9745-113">Methods</span></span>

<span data-ttu-id="f9745-114">El objeto **SWbemQualifierSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f9745-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="f9745-115">Método</span><span class="sxs-lookup"><span data-stu-id="f9745-115">Method</span></span>                                     | <span data-ttu-id="f9745-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9745-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f9745-117">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="f9745-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="f9745-118">Agrega un objeto [**SWbemQualifier**](swbemqualifier.md) a la colección **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="f9745-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="f9745-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9745-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="f9745-120">Devuelve un objeto [**SWbemQualifier**](swbemqualifier.md) con nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="f9745-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="f9745-121">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="f9745-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="f9745-122">Elimina un calificador con nombre de la colección.</span><span class="sxs-lookup"><span data-stu-id="f9745-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="f9745-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9745-123">Properties</span></span>

<span data-ttu-id="f9745-124">El objeto **SWbemQualifierSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f9745-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="f9745-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9745-125">Property</span></span>                                            | <span data-ttu-id="f9745-126">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f9745-126">Access type</span></span>          | <span data-ttu-id="f9745-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9745-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="f9745-128">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="f9745-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="f9745-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f9745-129">Read-only</span></span><br/> | <span data-ttu-id="f9745-130">Contiene el número de elementos de una colección **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="f9745-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9745-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9745-131">Requirements</span></span>



| <span data-ttu-id="f9745-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9745-132">Requirement</span></span> | <span data-ttu-id="f9745-133">Value</span><span class="sxs-lookup"><span data-stu-id="f9745-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9745-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9745-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9745-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9745-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9745-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9745-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9745-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9745-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9745-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9745-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9745-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9745-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9745-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9745-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9745-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9745-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9745-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9745-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9745-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9745-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9745-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="f9745-144">CLSID</span></span><br/>                    | <span data-ttu-id="f9745-145">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="f9745-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="f9745-146">IID</span><span class="sxs-lookup"><span data-stu-id="f9745-146">IID</span></span><br/>                      | <span data-ttu-id="f9745-147">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="f9745-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="f9745-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9745-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9745-149">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="f9745-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




