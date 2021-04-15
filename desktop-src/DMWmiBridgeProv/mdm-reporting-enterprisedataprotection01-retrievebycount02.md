---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 (clase)
description: La \_ \_ \_ clase RetrieveByCount02 de informes de MDM EnterpriseDataProtection01 se usa para recuperar un número especificado de registros del startTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 (clase)
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489167"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="abf87-105">\_Clase RetrieveByCount02 de informes de MDM \_ EnterpriseDataProtection01 \_</span><span class="sxs-lookup"><span data-stu-id="abf87-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="abf87-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="abf87-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="abf87-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="abf87-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="abf87-108">La **clase \_ RetrieveByCount02 de informes de MDM \_ EnterpriseDataProtection01 \_** se usa para recuperar un número especificado de registros del startTime.</span><span class="sxs-lookup"><span data-stu-id="abf87-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="abf87-109">StartTime se expresa en formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="abf87-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="abf87-110">Puede establecer el número de registros necesarios si establece LogCount y StartTime.</span><span class="sxs-lookup"><span data-stu-id="abf87-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="abf87-111">Devuelve el número especificado de registro o menos si el número total de registros es menor que LogCount.</span><span class="sxs-lookup"><span data-stu-id="abf87-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="abf87-112">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="abf87-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf87-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abf87-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="abf87-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="abf87-114">Members</span></span>

<span data-ttu-id="abf87-115">La **clase \_ RetrieveByCount02 de informes de MDM \_ EnterpriseDataProtection01 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="abf87-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="abf87-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abf87-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abf87-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abf87-117">Properties</span></span>

<span data-ttu-id="abf87-118">La **clase \_ RetrieveByCount02 de informes de MDM \_ EnterpriseDataProtection01 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="abf87-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abf87-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="abf87-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf87-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abf87-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf87-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abf87-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abf87-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="abf87-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="abf87-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="abf87-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="abf87-124">Para esta clase, la cadena es "RetrieveByCount".</span><span class="sxs-lookup"><span data-stu-id="abf87-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="abf87-125">LogCount</span><span class="sxs-lookup"><span data-stu-id="abf87-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf87-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="abf87-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="abf87-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abf87-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="abf87-128">Registros</span><span class="sxs-lookup"><span data-stu-id="abf87-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf87-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abf87-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf87-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abf87-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="abf87-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="abf87-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf87-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abf87-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf87-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abf87-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abf87-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="abf87-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="abf87-135">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="abf87-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="abf87-136">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="abf87-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="abf87-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="abf87-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf87-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abf87-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abf87-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abf87-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="abf87-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="abf87-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="abf87-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="abf87-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="abf87-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="abf87-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abf87-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abf87-143">Requirements</span></span>



| <span data-ttu-id="abf87-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="abf87-144">Requirement</span></span> | <span data-ttu-id="abf87-145">Value</span><span class="sxs-lookup"><span data-stu-id="abf87-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf87-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abf87-146">Minimum supported client</span></span><br/> | <span data-ttu-id="abf87-147">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="abf87-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="abf87-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abf87-148">Minimum supported server</span></span><br/> | <span data-ttu-id="abf87-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="abf87-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="abf87-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="abf87-150">Namespace</span></span><br/>                | <span data-ttu-id="abf87-151">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="abf87-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="abf87-152">MOF</span><span class="sxs-lookup"><span data-stu-id="abf87-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abf87-153"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abf87-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="abf87-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="abf87-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abf87-155"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="abf87-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

