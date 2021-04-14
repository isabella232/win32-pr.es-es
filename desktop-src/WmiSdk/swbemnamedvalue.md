---
description: El objeto SWbemNamedValue representa un único valor con nombre que pertenece al objeto de colección SWbemNamedValueSet. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 3f72afcd-6e10-4200-804d-918e3eb2862f
ms.tgt_platform: multiple
title: Objeto SWbemNamedValue (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue
- ISWbemNamedValue
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3668321256fea7ed8109e54f6b4df55bbd42867c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648425"
---
# <a name="swbemnamedvalue-object"></a><span data-ttu-id="a67b4-104">Objeto SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="a67b4-104">SWbemNamedValue object</span></span>

<span data-ttu-id="a67b4-105">El objeto **SWbemNamedValue** representa un único valor con nombre que pertenece al objeto de colección [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="a67b4-105">The **SWbemNamedValue** object represents a single named value that belongs to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection object.</span></span> <span data-ttu-id="a67b4-106">Este objeto no se puede crear mediante la llamada [**CreateObject**](creating-an-object-using-vbscript.md) de VBScript.</span><span class="sxs-lookup"><span data-stu-id="a67b4-106">This object cannot be created by the VBScript [**CreateObject**](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="a67b4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a67b4-107">Members</span></span>

<span data-ttu-id="a67b4-108">El objeto **SWbemNamedValue** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a67b4-108">The **SWbemNamedValue** object has these types of members:</span></span>

-   [<span data-ttu-id="a67b4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a67b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a67b4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a67b4-110">Properties</span></span>

<span data-ttu-id="a67b4-111">El objeto **SWbemNamedValue** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a67b4-111">The **SWbemNamedValue** object has these properties.</span></span>



| <span data-ttu-id="a67b4-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a67b4-112">Property</span></span>                                          | <span data-ttu-id="a67b4-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="a67b4-113">Access type</span></span>           | <span data-ttu-id="a67b4-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a67b4-114">Description</span></span>                                                                                    |
|:--------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a67b4-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="a67b4-115">**Name**</span></span>](swbemnamedvalue-name.md)<br/>   | <span data-ttu-id="a67b4-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a67b4-116">Read-only</span></span><br/>  | <span data-ttu-id="a67b4-117">Nombre del elemento **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="a67b4-117">Name of the **SWbemNamedValue** item.</span></span><br/>                                               |
| [<span data-ttu-id="a67b4-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="a67b4-118">**Value**</span></span>](swbemnamedvalue-value.md)<br/> | <span data-ttu-id="a67b4-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a67b4-119">Read/write</span></span><br/> | <span data-ttu-id="a67b4-120">Valor del elemento **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="a67b4-120">Value of the **SWbemNamedValue** item.</span></span> <span data-ttu-id="a67b4-121">Esta es la propiedad predeterminada de este objeto.</span><span class="sxs-lookup"><span data-stu-id="a67b4-121">This is the default property of this object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a67b4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a67b4-122">Requirements</span></span>



| <span data-ttu-id="a67b4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a67b4-123">Requirement</span></span> | <span data-ttu-id="a67b4-124">Value</span><span class="sxs-lookup"><span data-stu-id="a67b4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a67b4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a67b4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a67b4-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a67b4-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a67b4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a67b4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a67b4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a67b4-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a67b4-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a67b4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a67b4-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a67b4-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a67b4-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a67b4-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="a67b4-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a67b4-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a67b4-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a67b4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a67b4-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a67b4-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a67b4-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="a67b4-135">CLSID</span></span><br/>                    | <span data-ttu-id="a67b4-136">CLSID \_ SWbemNamedValue</span><span class="sxs-lookup"><span data-stu-id="a67b4-136">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="a67b4-137">IID</span><span class="sxs-lookup"><span data-stu-id="a67b4-137">IID</span></span><br/>                      | <span data-ttu-id="a67b4-138">\_ISWBEMNAMEDVALUE IID</span><span class="sxs-lookup"><span data-stu-id="a67b4-138">IID\_ISWbemNamedValue</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="a67b4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a67b4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a67b4-140">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="a67b4-140">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




