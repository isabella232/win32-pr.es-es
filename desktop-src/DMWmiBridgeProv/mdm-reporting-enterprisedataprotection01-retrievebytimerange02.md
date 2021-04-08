---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 (clase)
description: La \_ clase RetrieveByTimeRange02 de informes de MDM \_ EnterpriseDataProtection01 \_ se usa para recuperar los registros que existen en startTime y StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 (clase)
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078903"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="64b45-105">\_Clase RetrieveByTimeRange02 de informes de MDM \_ EnterpriseDataProtection01 \_</span><span class="sxs-lookup"><span data-stu-id="64b45-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="64b45-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="64b45-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="64b45-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="64b45-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="64b45-108">La **clase \_ RetrieveByTimeRange02 de informes de MDM \_ EnterpriseDataProtection01 \_** se usa para recuperar los registros que existen en startTime y StopTime.</span><span class="sxs-lookup"><span data-stu-id="64b45-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="64b45-109">StartTime y StopTime se expresan en formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="64b45-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="64b45-110">Si no se especifican las opciones StartTime y StopTime, los valores se interpretan como la primera vez existente o la última.</span><span class="sxs-lookup"><span data-stu-id="64b45-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="64b45-111">Estos son los otros escenarios posibles:</span><span class="sxs-lookup"><span data-stu-id="64b45-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="64b45-112">Si no se especifican StartTime y StopTime, devuelve todos los registros existentes.</span><span class="sxs-lookup"><span data-stu-id="64b45-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="64b45-113">Si se especifica StopTime, pero no se especifica StartTime, se devuelven todos los registros que existen antes de StopTime.</span><span class="sxs-lookup"><span data-stu-id="64b45-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="64b45-114">Si se especifica StartTime, pero no se especifica StopTime, se devuelven todos los registros que existen desde el StartTime.</span><span class="sxs-lookup"><span data-stu-id="64b45-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="64b45-115">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="64b45-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b45-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64b45-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="64b45-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="64b45-117">Members</span></span>

<span data-ttu-id="64b45-118">La **clase \_ RetrieveByTimeRange02 de informes de MDM \_ EnterpriseDataProtection01 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="64b45-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="64b45-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64b45-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64b45-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64b45-120">Properties</span></span>

<span data-ttu-id="64b45-121">La **clase \_ RetrieveByTimeRange02 de informes de MDM \_ EnterpriseDataProtection01 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="64b45-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64b45-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="64b45-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b45-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64b45-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b45-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64b45-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64b45-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64b45-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="64b45-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="64b45-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="64b45-127">Para esta clase, la cadena es "RetrieveByTimeRange".</span><span class="sxs-lookup"><span data-stu-id="64b45-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="64b45-128">Registros</span><span class="sxs-lookup"><span data-stu-id="64b45-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b45-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64b45-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b45-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="64b45-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64b45-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="64b45-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b45-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64b45-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b45-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="64b45-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64b45-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64b45-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="64b45-135">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="64b45-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="64b45-136">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="64b45-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="64b45-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="64b45-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b45-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64b45-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b45-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="64b45-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b45-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="64b45-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b45-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="64b45-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b45-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="64b45-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b45-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="64b45-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b45-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="64b45-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64b45-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="64b45-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64b45-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64b45-146">Requirements</span></span>



| <span data-ttu-id="64b45-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b45-147">Requirement</span></span> | <span data-ttu-id="64b45-148">Value</span><span class="sxs-lookup"><span data-stu-id="64b45-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b45-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b45-149">Minimum supported client</span></span><br/> | <span data-ttu-id="64b45-150">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="64b45-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="64b45-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64b45-151">Minimum supported server</span></span><br/> | <span data-ttu-id="64b45-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="64b45-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="64b45-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="64b45-153">Namespace</span></span><br/>                | <span data-ttu-id="64b45-154">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="64b45-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="64b45-155">MOF</span><span class="sxs-lookup"><span data-stu-id="64b45-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64b45-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64b45-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="64b45-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64b45-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64b45-158"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="64b45-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

