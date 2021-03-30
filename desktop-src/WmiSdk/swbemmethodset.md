---
description: Un objeto SWbemMethodSet es una colección de objetos SWbemMethod. Los elementos se recuperan mediante el método Item. Para obtener más información, vea obtener acceso a una colección. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Objeto SWbemMethodSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910281"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="bb03c-106">Objeto SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="bb03c-106">SWbemMethodSet object</span></span>

<span data-ttu-id="bb03c-107">Un objeto **SWbemMethodSet** es una colección de objetos [**SWbemMethod**](swbemmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="bb03c-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="bb03c-108">Los elementos se recuperan mediante el método [**Item**](swbemmethodset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="bb03c-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="bb03c-109">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="bb03c-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="bb03c-110">Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="bb03c-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="bb03c-111">En esta versión de la API, no se admite el acceso de escritura a la información del método.</span><span class="sxs-lookup"><span data-stu-id="bb03c-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="bb03c-112">Si desea definir métodos o modificar las definiciones de método existentes, puede definir los cambios del método en un archivo MOF y enviar los cambios mediante el compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="bb03c-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="bb03c-113">También puede usar la API COM de WMI.</span><span class="sxs-lookup"><span data-stu-id="bb03c-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="bb03c-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb03c-114">Members</span></span>

<span data-ttu-id="bb03c-115">El objeto **SWbemMethodSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bb03c-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="bb03c-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb03c-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="bb03c-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb03c-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb03c-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb03c-118">Methods</span></span>

<span data-ttu-id="bb03c-119">El objeto **SWbemMethodSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bb03c-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="bb03c-120">Método</span><span class="sxs-lookup"><span data-stu-id="bb03c-120">Method</span></span>                              | <span data-ttu-id="bb03c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb03c-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb03c-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb03c-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="bb03c-123">Recupera un objeto [**SWbemMethod**](swbemmethod.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="bb03c-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="bb03c-124">Este es el método de automatización predeterminado de este objeto.</span><span class="sxs-lookup"><span data-stu-id="bb03c-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bb03c-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb03c-125">Properties</span></span>

<span data-ttu-id="bb03c-126">El objeto **SWbemMethodSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb03c-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="bb03c-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb03c-127">Property</span></span>                                         | <span data-ttu-id="bb03c-128">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="bb03c-128">Access type</span></span>          | <span data-ttu-id="bb03c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb03c-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="bb03c-130">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="bb03c-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="bb03c-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb03c-131">Read-only</span></span><br/> | <span data-ttu-id="bb03c-132">Número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="bb03c-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb03c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb03c-133">Requirements</span></span>



| <span data-ttu-id="bb03c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb03c-134">Requirement</span></span> | <span data-ttu-id="bb03c-135">Value</span><span class="sxs-lookup"><span data-stu-id="bb03c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb03c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb03c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bb03c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb03c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb03c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb03c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bb03c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb03c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb03c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb03c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb03c-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb03c-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb03c-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bb03c-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb03c-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb03c-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb03c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb03c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb03c-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb03c-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bb03c-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="bb03c-146">CLSID</span></span><br/>                    | <span data-ttu-id="bb03c-147">CLSID \_ SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="bb03c-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="bb03c-148">IID</span><span class="sxs-lookup"><span data-stu-id="bb03c-148">IID</span></span><br/>                      | <span data-ttu-id="bb03c-149">\_ISWBEMMETHODSET IID</span><span class="sxs-lookup"><span data-stu-id="bb03c-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="bb03c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb03c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb03c-151">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="bb03c-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




