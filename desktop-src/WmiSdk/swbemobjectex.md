---
description: Proporciona funcionalidad extendida para SWbemObject. Como SWbemObject, todos los objetos de WMI pueden usar los métodos de este objeto extendido.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: Objeto SWbemObjectEx (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: abed8c1d58687203aaeb32918cf15b2785b92622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715732"
---
# <a name="swbemobjectex-object"></a><span data-ttu-id="02b99-104">Objeto SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="02b99-104">SWbemObjectEx object</span></span>

<span data-ttu-id="02b99-105">El objeto **SWbemObjectEx** proporciona funcionalidad extendida para [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="02b99-105">The **SWbemObjectEx** object provides extended functionality for [**SWbemObject**](swbemobject.md).</span></span> <span data-ttu-id="02b99-106">Como **SWbemObject**, todos los objetos de WMI pueden usar los métodos de este objeto extendido.</span><span class="sxs-lookup"><span data-stu-id="02b99-106">Like **SWbemObject**, the methods of this extended object can be used by all WMI objects.</span></span> <span data-ttu-id="02b99-107">Este objeto no se puede crear mediante la llamada [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="02b99-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="02b99-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="02b99-108">Members</span></span>

<span data-ttu-id="02b99-109">El objeto **SWbemObjectEx** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="02b99-109">The **SWbemObjectEx** object has these types of members:</span></span>

-   [<span data-ttu-id="02b99-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="02b99-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="02b99-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02b99-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02b99-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="02b99-112">Methods</span></span>

<span data-ttu-id="02b99-113">El objeto **SWbemObjectEx** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="02b99-113">The **SWbemObjectEx** object has these methods.</span></span>



| <span data-ttu-id="02b99-114">Método</span><span class="sxs-lookup"><span data-stu-id="02b99-114">Method</span></span>                                      | <span data-ttu-id="02b99-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="02b99-115">Description</span></span>                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="02b99-116">**GetText\_**</span><span class="sxs-lookup"><span data-stu-id="02b99-116">**GetText\_**</span></span>](swbemobjectex-gettext-.md) | <span data-ttu-id="02b99-117">Devuelve un archivo de texto que muestra el contenido de un objeto en XML.</span><span class="sxs-lookup"><span data-stu-id="02b99-117">Returns a text file showing the contents of an object in XML.</span></span><br/> |
| [<span data-ttu-id="02b99-118">**Actualizaciones\_**</span><span class="sxs-lookup"><span data-stu-id="02b99-118">**Refresh\_**</span></span>](swbemobjectex-refresh-.md) | <span data-ttu-id="02b99-119">Actualiza los datos de un objeto.</span><span class="sxs-lookup"><span data-stu-id="02b99-119">Refreshes data in an object.</span></span><br/>                                  |
| <span data-ttu-id="02b99-120">**SetFromText\_**</span><span class="sxs-lookup"><span data-stu-id="02b99-120">**SetFromText\_**</span></span>                           | <span data-ttu-id="02b99-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="02b99-121">Reserved for future use.</span></span><br/>                                      |



 

### <a name="properties"></a><span data-ttu-id="02b99-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02b99-122">Properties</span></span>

<span data-ttu-id="02b99-123">El objeto **SWbemObjectEx** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="02b99-123">The **SWbemObjectEx** object has these properties.</span></span>



| <span data-ttu-id="02b99-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="02b99-124">Property</span></span>                                                                 | <span data-ttu-id="02b99-125">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="02b99-125">Access type</span></span>           | <span data-ttu-id="02b99-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="02b99-126">Description</span></span>                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02b99-127">**SystemProperties\_**</span><span class="sxs-lookup"><span data-stu-id="02b99-127">**SystemProperties\_**</span></span>](swbemobjectex-systemproperties-.md)<br/> | <span data-ttu-id="02b99-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="02b99-128">Read/write</span></span><br/> | <span data-ttu-id="02b99-129">Un objeto [**SWbemPropertySet**](swbempropertyset.md) que contiene la colección de propiedades del sistema que se aplican a **SWbemObjectEx**.</span><span class="sxs-lookup"><span data-stu-id="02b99-129">An [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of system properties that apply to the **SWbemObjectEx**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02b99-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02b99-130">Requirements</span></span>



| <span data-ttu-id="02b99-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="02b99-131">Requirement</span></span> | <span data-ttu-id="02b99-132">Value</span><span class="sxs-lookup"><span data-stu-id="02b99-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02b99-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02b99-133">Minimum supported client</span></span><br/> | <span data-ttu-id="02b99-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02b99-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02b99-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02b99-135">Minimum supported server</span></span><br/> | <span data-ttu-id="02b99-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02b99-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02b99-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02b99-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="02b99-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02b99-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="02b99-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="02b99-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="02b99-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02b99-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02b99-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02b99-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02b99-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02b99-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="02b99-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="02b99-143">CLSID</span></span><br/>                    | <span data-ttu-id="02b99-144">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="02b99-144">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="02b99-145">IID</span><span class="sxs-lookup"><span data-stu-id="02b99-145">IID</span></span><br/>                      | <span data-ttu-id="02b99-146">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="02b99-146">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="02b99-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="02b99-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02b99-148">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="02b99-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="02b99-149">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="02b99-149">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="02b99-150">WbemObjectTextFormatEnum</span><span class="sxs-lookup"><span data-stu-id="02b99-150">WbemObjectTextFormatEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

