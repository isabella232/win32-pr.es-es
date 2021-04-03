---
description: El objeto SWbemPrivilege representa un solo privilegio. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Objeto SWbemPrivilege (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083382"
---
# <a name="swbemprivilege-object"></a><span data-ttu-id="2fb16-104">Objeto SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="2fb16-104">SWbemPrivilege object</span></span>

<span data-ttu-id="2fb16-105">El objeto **SWbemPrivilege** representa un solo privilegio.</span><span class="sxs-lookup"><span data-stu-id="2fb16-105">The **SWbemPrivilege** object represents a single privilege.</span></span> <span data-ttu-id="2fb16-106">Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.</span><span class="sxs-lookup"><span data-stu-id="2fb16-106">This object cannot be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="2fb16-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2fb16-107">Members</span></span>

<span data-ttu-id="2fb16-108">El objeto **SWbemPrivilege** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2fb16-108">The **SWbemPrivilege** object has these types of members:</span></span>

-   [<span data-ttu-id="2fb16-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fb16-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fb16-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fb16-110">Properties</span></span>

<span data-ttu-id="2fb16-111">El objeto **SWbemPrivilege** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2fb16-111">The **SWbemPrivilege** object has these properties.</span></span>



| <span data-ttu-id="2fb16-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2fb16-112">Property</span></span>                                                     | <span data-ttu-id="2fb16-113">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="2fb16-113">Access type</span></span>           | <span data-ttu-id="2fb16-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fb16-114">Description</span></span>                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="2fb16-115">**Mostrar**</span><span class="sxs-lookup"><span data-stu-id="2fb16-115">**Displayname**</span></span>](swbemprivilege-displayname.md)<br/> | <span data-ttu-id="2fb16-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fb16-116">Read-only</span></span><br/>  | <span data-ttu-id="2fb16-117">Nombre para mostrar de este privilegio.</span><span class="sxs-lookup"><span data-stu-id="2fb16-117">Display name of this privilege.</span></span><br/>                                       |
| [<span data-ttu-id="2fb16-118">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="2fb16-118">**Identifier**</span></span>](swbemprivilege-identifier.md)<br/>   | <span data-ttu-id="2fb16-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fb16-119">Read/write</span></span><br/> | <span data-ttu-id="2fb16-120">Entero que representa el privilegio que se va a establecer o recuperar.</span><span class="sxs-lookup"><span data-stu-id="2fb16-120">Integer that represents the privilege that is being set or retrieved.</span></span><br/> |
| [<span data-ttu-id="2fb16-121">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2fb16-121">**IsEnabled**</span></span>](swbemprivilege-isenabled.md)<br/>     | <span data-ttu-id="2fb16-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fb16-122">Read/write</span></span><br/> | <span data-ttu-id="2fb16-123">Valor booleano que indica si este privilegio está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2fb16-123">Boolean value that indicates if this privilege is enabled.</span></span><br/>            |
| [<span data-ttu-id="2fb16-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="2fb16-124">**Name**</span></span>](swbemprivilege-name.md)<br/>               | <span data-ttu-id="2fb16-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fb16-125">Read-only</span></span><br/>  | <span data-ttu-id="2fb16-126">Nombre de este privilegio.</span><span class="sxs-lookup"><span data-stu-id="2fb16-126">Name of this privilege.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="2fb16-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fb16-127">Requirements</span></span>



| <span data-ttu-id="2fb16-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb16-128">Requirement</span></span> | <span data-ttu-id="2fb16-129">Value</span><span class="sxs-lookup"><span data-stu-id="2fb16-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb16-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fb16-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb16-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fb16-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fb16-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fb16-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb16-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fb16-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fb16-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fb16-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb16-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb16-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fb16-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2fb16-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="2fb16-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2fb16-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2fb16-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fb16-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb16-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fb16-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2fb16-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="2fb16-140">CLSID</span></span><br/>                    | <span data-ttu-id="2fb16-141">CLSID \_ SWbemPrivilege</span><span class="sxs-lookup"><span data-stu-id="2fb16-141">CLSID\_SWbemPrivilege</span></span><br/>                                                        |
| <span data-ttu-id="2fb16-142">IID</span><span class="sxs-lookup"><span data-stu-id="2fb16-142">IID</span></span><br/>                      | <span data-ttu-id="2fb16-143">\_ISWBEMPRIVILEGE IID</span><span class="sxs-lookup"><span data-stu-id="2fb16-143">IID\_ISWbemPrivilege</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="2fb16-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fb16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb16-145">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="2fb16-145">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="2fb16-146">Scripting de objetos de API</span><span class="sxs-lookup"><span data-stu-id="2fb16-146">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




