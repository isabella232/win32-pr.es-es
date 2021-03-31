---
title: MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 (clase)
description: La \_ clase RetrieveByTimeRange02 de informes de MDM \_ SecurityAuditing01 \_ se usa para recuperar los registros que existen en startTime y StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 (clase)
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801196"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="b4b77-105">\_Clase RetrieveByTimeRange02 de informes de MDM \_ SecurityAuditing01 \_</span><span class="sxs-lookup"><span data-stu-id="b4b77-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="b4b77-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b4b77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b4b77-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b4b77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b4b77-108">La **clase \_ RetrieveByTimeRange02 de informes de MDM \_ SecurityAuditing01 \_** se usa para recuperar los registros que existen en StartTime y StopTime. los startTime y los StopTime se expresan en formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="b4b77-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="b4b77-109">Si no se especifican las opciones StartTime y StopTime, los valores se interpretan como la primera vez existente o la última.</span><span class="sxs-lookup"><span data-stu-id="b4b77-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="b4b77-110">Estos son los otros escenarios posibles:</span><span class="sxs-lookup"><span data-stu-id="b4b77-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="b4b77-111">Si no se especifican StartTime y StopTime, devuelve todos los registros existentes.</span><span class="sxs-lookup"><span data-stu-id="b4b77-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="b4b77-112">Si se especifica StopTime, pero no se especifica StartTime, se devuelven todos los registros que existen antes de StopTime.</span><span class="sxs-lookup"><span data-stu-id="b4b77-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="b4b77-113">Si se especifica StartTime, pero no se especifica StopTime, se devuelven todos los registros que existen desde el StartTime.</span><span class="sxs-lookup"><span data-stu-id="b4b77-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="b4b77-114">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b4b77-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b77-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4b77-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="b4b77-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4b77-116">Members</span></span>

<span data-ttu-id="b4b77-117">La **clase \_ RetrieveByTimeRange02 de informes de MDM \_ SecurityAuditing01 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b4b77-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="b4b77-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4b77-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4b77-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4b77-119">Properties</span></span>

<span data-ttu-id="b4b77-120">La **clase \_ RetrieveByTimeRange02 de informes de MDM \_ SecurityAuditing01 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b4b77-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b4b77-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b4b77-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b77-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4b77-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4b77-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4b77-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b4b77-125">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b4b77-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="b4b77-126">Para esta clase, la cadena es "RetrieveByTimeRange".</span><span class="sxs-lookup"><span data-stu-id="b4b77-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="b4b77-127">Registros</span><span class="sxs-lookup"><span data-stu-id="b4b77-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b77-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4b77-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b4b77-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b4b77-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b4b77-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b77-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4b77-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4b77-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4b77-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b4b77-134">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b4b77-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="b4b77-135">Para esta clase, la cadena es "./Vendor/MSFT/SecurityAuditing".</span><span class="sxs-lookup"><span data-stu-id="b4b77-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="b4b77-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="b4b77-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b77-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4b77-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b4b77-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b4b77-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="b4b77-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4b77-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4b77-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4b77-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b4b77-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4b77-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4b77-142">Requirements</span></span>



| <span data-ttu-id="b4b77-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b77-143">Requirement</span></span> | <span data-ttu-id="b4b77-144">Value</span><span class="sxs-lookup"><span data-stu-id="b4b77-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b77-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4b77-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b77-146">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4b77-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b4b77-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4b77-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b77-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b4b77-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="b4b77-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4b77-149">Namespace</span></span><br/>                | <span data-ttu-id="b4b77-150">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b4b77-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="b4b77-151">MOF</span><span class="sxs-lookup"><span data-stu-id="b4b77-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4b77-152"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4b77-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="b4b77-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4b77-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4b77-154"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="b4b77-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

