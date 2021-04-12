---
description: El objeto SWbemProperty representa una única propiedad WMI de un objeto administrado. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Objeto SWbemProperty (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279288"
---
# <a name="swbemproperty-object"></a><span data-ttu-id="f40f7-104">Objeto SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="f40f7-104">SWbemProperty object</span></span>

<span data-ttu-id="f40f7-105">El objeto **SWbemProperty** representa una única propiedad WMI de un objeto administrado.</span><span class="sxs-lookup"><span data-stu-id="f40f7-105">The **SWbemProperty** object represents a single WMI property of a managed object.</span></span> <span data-ttu-id="f40f7-106">Este objeto no se puede crear mediante la llamada [CreateObject](creating-an-object-using-vbscript.md) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="f40f7-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="f40f7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f40f7-107">Members</span></span>

<span data-ttu-id="f40f7-108">El objeto **SWbemProperty** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f40f7-108">The **SWbemProperty** object has these types of members:</span></span>

-   [<span data-ttu-id="f40f7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f40f7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f40f7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f40f7-110">Properties</span></span>

<span data-ttu-id="f40f7-111">El objeto **SWbemProperty** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f40f7-111">The **SWbemProperty** object has these properties.</span></span>



| <span data-ttu-id="f40f7-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f40f7-112">Property</span></span>                                                     | <span data-ttu-id="f40f7-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f40f7-113">Access type</span></span>           | <span data-ttu-id="f40f7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f40f7-114">Description</span></span>                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f40f7-115">**CIMType**</span><span class="sxs-lookup"><span data-stu-id="f40f7-115">**CIMType**</span></span>](swbemproperty-cimtype.md)<br/>          | <span data-ttu-id="f40f7-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f40f7-116">Read-only</span></span><br/>  | <span data-ttu-id="f40f7-117">Tipo de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f40f7-117">Type of this property.</span></span><br/>                                                                                             |
| [<span data-ttu-id="f40f7-118">**IsArray (**</span><span class="sxs-lookup"><span data-stu-id="f40f7-118">**IsArray**</span></span>](swbemproperty-isarray.md)<br/>          | <span data-ttu-id="f40f7-119">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f40f7-119">Read-only</span></span><br/>  | <span data-ttu-id="f40f7-120">Valor booleano que indica si esta propiedad tiene un tipo de matriz.</span><span class="sxs-lookup"><span data-stu-id="f40f7-120">Boolean value that indicates if this property has an array type.</span></span><br/>                                                   |
| [<span data-ttu-id="f40f7-121">**IsLocal**</span><span class="sxs-lookup"><span data-stu-id="f40f7-121">**IsLocal**</span></span>](swbemproperty-islocal.md)<br/>          | <span data-ttu-id="f40f7-122">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f40f7-122">Read-only</span></span><br/>  | <span data-ttu-id="f40f7-123">Valor booleano que indica si esta propiedad es local.</span><span class="sxs-lookup"><span data-stu-id="f40f7-123">Boolean value that indicates if this property is local.</span></span><br/>                                                            |
| [<span data-ttu-id="f40f7-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="f40f7-124">**Name**</span></span>](swbemproperty-name.md)<br/>                | <span data-ttu-id="f40f7-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f40f7-125">Read-only</span></span><br/>  | <span data-ttu-id="f40f7-126">Nombre de esta propiedad WMI.</span><span class="sxs-lookup"><span data-stu-id="f40f7-126">Name of this WMI property.</span></span><br/>                                                                                         |
| [<span data-ttu-id="f40f7-127">**Origen**</span><span class="sxs-lookup"><span data-stu-id="f40f7-127">**Origin**</span></span>](swbemproperty-origin.md)<br/>            | <span data-ttu-id="f40f7-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f40f7-128">Read-only</span></span><br/>  | <span data-ttu-id="f40f7-129">Contiene la clase de origen de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f40f7-129">Contains the originating class of this property.</span></span><br/>                                                                   |
| [<span data-ttu-id="f40f7-130">**Calificadores\_**</span><span class="sxs-lookup"><span data-stu-id="f40f7-130">**Qualifiers\_**</span></span>](swbemproperty-qualifiers-.md)<br/> | <span data-ttu-id="f40f7-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="f40f7-131">Read-only</span></span><br/>  | <span data-ttu-id="f40f7-132">Un objeto [**SWbemQualifierSet**](swbemqualifierset.md) , que es la colección de calificadores para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f40f7-132">An [**SWbemQualifierSet**](swbemqualifierset.md) object, which is the collection of qualifiers for this property.</span></span><br/> |
| [<span data-ttu-id="f40f7-133">**Value**</span><span class="sxs-lookup"><span data-stu-id="f40f7-133">**Value**</span></span>](swbemproperty-value.md)<br/>              | <span data-ttu-id="f40f7-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f40f7-134">Read/write</span></span><br/> | <span data-ttu-id="f40f7-135">Valor real de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f40f7-135">Actual value of this property.</span></span> <span data-ttu-id="f40f7-136">Esta es la propiedad de automatización predeterminada de este objeto.</span><span class="sxs-lookup"><span data-stu-id="f40f7-136">This is the default automation property of this object.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="f40f7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f40f7-137">Requirements</span></span>



| <span data-ttu-id="f40f7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f40f7-138">Requirement</span></span> | <span data-ttu-id="f40f7-139">Value</span><span class="sxs-lookup"><span data-stu-id="f40f7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f40f7-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f40f7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="f40f7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f40f7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f40f7-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f40f7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="f40f7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f40f7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f40f7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f40f7-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="f40f7-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f40f7-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f40f7-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f40f7-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="f40f7-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f40f7-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f40f7-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f40f7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f40f7-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f40f7-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f40f7-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="f40f7-150">CLSID</span></span><br/>                    | <span data-ttu-id="f40f7-151">CLSID \_ SWbemProperty</span><span class="sxs-lookup"><span data-stu-id="f40f7-151">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="f40f7-152">IID</span><span class="sxs-lookup"><span data-stu-id="f40f7-152">IID</span></span><br/>                      | <span data-ttu-id="f40f7-153">\_ISWBEMPROPERTY IID</span><span class="sxs-lookup"><span data-stu-id="f40f7-153">IID\_ISWbemProperty</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f40f7-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="f40f7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f40f7-155">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="f40f7-155">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




