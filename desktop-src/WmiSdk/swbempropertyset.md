---
description: Un objeto SWbemPropertySet es una colección de objetos SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Objeto SWbemPropertySet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717023"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="1c304-103">Objeto SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="1c304-103">SWbemPropertySet object</span></span>

<span data-ttu-id="1c304-104">Un objeto **SWbemPropertySet** es una colección de objetos [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1c304-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="1c304-105">Puede agregar elementos a la colección mediante el método [**Add**](swbempropertyset-add.md) , recuperar elementos de la colección mediante el método [**Item**](swbempropertyset-item.md) y quitar elementos de la colección mediante el método [**Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="1c304-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="1c304-106">Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1c304-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="1c304-107">Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="1c304-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="1c304-108">Los objetos [**SWbemProperty**](swbemproperty.md) que componen una colección **SWbemPropertySet** se usan para describir las propiedades de una única clase o instancia de WMI.</span><span class="sxs-lookup"><span data-stu-id="1c304-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="1c304-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c304-109">Members</span></span>

<span data-ttu-id="1c304-110">El objeto **SWbemPropertySet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1c304-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="1c304-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c304-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c304-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c304-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c304-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c304-113">Methods</span></span>

<span data-ttu-id="1c304-114">El objeto **SWbemPropertySet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1c304-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="1c304-115">Método</span><span class="sxs-lookup"><span data-stu-id="1c304-115">Method</span></span>                                    | <span data-ttu-id="1c304-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c304-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c304-117">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="1c304-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="1c304-118">Agrega un objeto [**SWbemProperty**](swbemproperty.md) a la colección **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="1c304-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="1c304-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1c304-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="1c304-120">Obtiene un denominado [**SWbemProperty**](swbemproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c304-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="1c304-121">Este es el método predeterminado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="1c304-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="1c304-122">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="1c304-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="1c304-123">Elimina un objeto [**SWbemProperty**](swbemproperty.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="1c304-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="1c304-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c304-124">Properties</span></span>

<span data-ttu-id="1c304-125">El objeto **SWbemPropertySet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1c304-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="1c304-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1c304-126">Property</span></span>                                           | <span data-ttu-id="1c304-127">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1c304-127">Access type</span></span>          | <span data-ttu-id="1c304-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c304-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="1c304-129">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="1c304-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="1c304-130">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1c304-130">Read-only</span></span><br/> | <span data-ttu-id="1c304-131">Número de elementos de la colección **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="1c304-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="1c304-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1c304-132">Examples</span></span>

<span data-ttu-id="1c304-133">El siguiente ejemplo de VBScript muestra cómo [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) puede devolver **wbemErrResetToDefault** si se invalida la propiedad.</span><span class="sxs-lookup"><span data-stu-id="1c304-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="1c304-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c304-134">Requirements</span></span>



| <span data-ttu-id="1c304-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c304-135">Requirement</span></span> | <span data-ttu-id="1c304-136">Value</span><span class="sxs-lookup"><span data-stu-id="1c304-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c304-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c304-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1c304-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c304-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c304-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c304-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1c304-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c304-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c304-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c304-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c304-142"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c304-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c304-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1c304-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c304-144"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c304-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c304-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c304-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c304-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c304-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c304-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="1c304-147">CLSID</span></span><br/>                    | <span data-ttu-id="1c304-148">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="1c304-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="1c304-149">IID</span><span class="sxs-lookup"><span data-stu-id="1c304-149">IID</span></span><br/>                      | <span data-ttu-id="1c304-150">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="1c304-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="1c304-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c304-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c304-152">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="1c304-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




