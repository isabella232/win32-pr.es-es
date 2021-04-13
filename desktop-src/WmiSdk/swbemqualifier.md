---
description: Puede utilizar las propiedades del objeto SWbemQualifier para representar un único calificador de una clase WMI, una instancia, una propiedad o un parámetro de método. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: b5dbe98a-e1d8-4679-a563-c88760d08b79
ms.tgt_platform: multiple
title: Objeto SWbemQualifier (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifier
- ISWbemQualifier
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5e9a49832ffa1e38fbe6ee0f71e1f6a39c1b0ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276118"
---
# <a name="swbemqualifier-object"></a><span data-ttu-id="e3f94-104">Objeto SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="e3f94-104">SWbemQualifier object</span></span>

<span data-ttu-id="e3f94-105">Puede utilizar las propiedades del objeto **SWbemQualifier** para representar un único calificador de una clase WMI, una instancia, una propiedad o un parámetro de método.</span><span class="sxs-lookup"><span data-stu-id="e3f94-105">You can use the properties of the **SWbemQualifier** object to represent a single qualifier of a WMI class, instance, property, or method parameter.</span></span> <span data-ttu-id="e3f94-106">Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="e3f94-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="e3f94-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3f94-107">Members</span></span>

<span data-ttu-id="e3f94-108">El objeto **SWbemQualifier** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e3f94-108">The **SWbemQualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="e3f94-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3f94-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3f94-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3f94-110">Properties</span></span>

<span data-ttu-id="e3f94-111">El objeto **SWbemQualifier** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e3f94-111">The **SWbemQualifier** object has these properties.</span></span>



| <span data-ttu-id="e3f94-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3f94-112">Property</span></span>                                                                       | <span data-ttu-id="e3f94-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="e3f94-113">Access type</span></span>           | <span data-ttu-id="e3f94-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3f94-114">Description</span></span>                                                                                           |
|:-------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3f94-115">**IsAmended**</span><span class="sxs-lookup"><span data-stu-id="e3f94-115">**IsAmended**</span></span>](swbemqualifier-isamended.md)<br/>                       | <span data-ttu-id="e3f94-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3f94-116">Read-only</span></span><br/>  | <span data-ttu-id="e3f94-117">Valor booleano que indica si se ha traducido este calificador mediante una operación de combinación.</span><span class="sxs-lookup"><span data-stu-id="e3f94-117">Boolean value that indicates if this qualifier has been localized using a merge operation.</span></span><br/> |
| [<span data-ttu-id="e3f94-118">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="e3f94-118">**IsLocal**</span></span>](swbemqualifier-islocal.md)<br/>                           | <span data-ttu-id="e3f94-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3f94-119">Read-only</span></span><br/>  | <span data-ttu-id="e3f94-120">Valor booleano que indica si este calificador es local.</span><span class="sxs-lookup"><span data-stu-id="e3f94-120">Boolean value that indicates if this qualifier is local.</span></span><br/>                                   |
| [<span data-ttu-id="e3f94-121">**IsOverridable**</span><span class="sxs-lookup"><span data-stu-id="e3f94-121">**IsOverridable**</span></span>](swbemqualifier-isoverridable.md)<br/>               | <span data-ttu-id="e3f94-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e3f94-122">Read/write</span></span><br/> | <span data-ttu-id="e3f94-123">Valor booleano que indica si se puede invalidar este calificador al propagarse.</span><span class="sxs-lookup"><span data-stu-id="e3f94-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span><br/>          |
| [<span data-ttu-id="e3f94-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="e3f94-124">**Name**</span></span>](swbemqualifier-name.md)<br/>                                 | <span data-ttu-id="e3f94-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3f94-125">Read-only</span></span><br/>  | <span data-ttu-id="e3f94-126">Nombre de este calificador.</span><span class="sxs-lookup"><span data-stu-id="e3f94-126">Name of this qualifier.</span></span><br/>                                                                    |
| [<span data-ttu-id="e3f94-127">**PropagatesToInstance**</span><span class="sxs-lookup"><span data-stu-id="e3f94-127">**PropagatesToInstance**</span></span>](swbemqualifier-propagatestoinstance.md)<br/> | <span data-ttu-id="e3f94-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e3f94-128">Read/write</span></span><br/> | <span data-ttu-id="e3f94-129">Valor booleano que indica si se puede propagar este calificador a una instancia de.</span><span class="sxs-lookup"><span data-stu-id="e3f94-129">Boolean value that indicates if this qualifier can be propagated to an instance.</span></span><br/>           |
| [<span data-ttu-id="e3f94-130">**PropagatesToSubClass**</span><span class="sxs-lookup"><span data-stu-id="e3f94-130">**PropagatesToSubClass**</span></span>](swbemqualifier-propagatestosubclass.md)<br/> | <span data-ttu-id="e3f94-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3f94-131">Read-only</span></span><br/>  | <span data-ttu-id="e3f94-132">Valor booleano que indica si este calificador se puede propagar a una subclase.</span><span class="sxs-lookup"><span data-stu-id="e3f94-132">Boolean value that indicates if this qualifier can be propagated to a subclass.</span></span><br/>            |
| [<span data-ttu-id="e3f94-133">**Value**</span><span class="sxs-lookup"><span data-stu-id="e3f94-133">**Value**</span></span>](swbemqualifier-value.md)<br/>                               | <span data-ttu-id="e3f94-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e3f94-134">Read/write</span></span><br/> | <span data-ttu-id="e3f94-135">Valor de variante de este calificador.</span><span class="sxs-lookup"><span data-stu-id="e3f94-135">Variant value of this qualifier.</span></span> <span data-ttu-id="e3f94-136">Esta es la propiedad predeterminada de este objeto.</span><span class="sxs-lookup"><span data-stu-id="e3f94-136">This is the default property of this object.</span></span><br/>              |



 

## <a name="requirements"></a><span data-ttu-id="e3f94-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3f94-137">Requirements</span></span>



| <span data-ttu-id="e3f94-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3f94-138">Requirement</span></span> | <span data-ttu-id="e3f94-139">Value</span><span class="sxs-lookup"><span data-stu-id="e3f94-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f94-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3f94-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f94-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3f94-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3f94-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3f94-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f94-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3f94-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3f94-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3f94-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f94-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f94-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3f94-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e3f94-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3f94-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e3f94-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e3f94-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3f94-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3f94-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3f94-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3f94-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="e3f94-150">CLSID</span></span><br/>                    | <span data-ttu-id="e3f94-151">CLSID \_ SWbemQualifier</span><span class="sxs-lookup"><span data-stu-id="e3f94-151">CLSID\_SWbemQualifier</span></span><br/>                                                        |
| <span data-ttu-id="e3f94-152">IID</span><span class="sxs-lookup"><span data-stu-id="e3f94-152">IID</span></span><br/>                      | <span data-ttu-id="e3f94-153">\_ISWBEMQUALIFIER IID</span><span class="sxs-lookup"><span data-stu-id="e3f94-153">IID\_ISWbemQualifier</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="e3f94-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3f94-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f94-155">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="e3f94-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




