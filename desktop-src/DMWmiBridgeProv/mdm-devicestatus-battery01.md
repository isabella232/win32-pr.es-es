---
title: MDM_DeviceStatus_Battery01 (clase)
description: '\_ \_ La empresa usa la clase Battery01 de DEVICESTATUS de MDM para consultar el estado de cumplimiento de la batería de los dispositivos con sus directivas de empresa.'
ms.assetid: f4e92e2a-e267-467a-9905-2539dcaf8d8c
keywords:
- MDM_DeviceStatus_Battery01 (clase)
- MDM_DeviceStatus_Battery01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Battery01
- MDM_DeviceStatus_Battery01.InstanceID
- MDM_DeviceStatus_Battery01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b89cd709c4d0d3d5ad3490114bc82d36aa4ef0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658281"
---
# <a name="mdm_devicestatus_battery01-class"></a><span data-ttu-id="2fd01-105">\_Clase Battery01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="2fd01-105">MDM\_DeviceStatus\_Battery01 class</span></span>

<span data-ttu-id="2fd01-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2fd01-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2fd01-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2fd01-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2fd01-108">La empresa usa la clase **\_ \_ Battery01 de DeviceStatus de MDM** para consultar el estado de cumplimiento de la batería de los dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="2fd01-108">The **MDM\_DeviceStatus\_Battery01** class is used by the enterprise to query the state of battery compliance of devices with their enterprise policies.</span></span>

<span data-ttu-id="2fd01-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2fd01-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd01-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fd01-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Battery01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  sint32 EstimatedChargeRemaining;
  sint32 EstimatedRuntime;
};
```

## <a name="members"></a><span data-ttu-id="2fd01-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2fd01-111">Members</span></span>

<span data-ttu-id="2fd01-112">La **clase \_ \_ Battery01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2fd01-112">The **MDM\_DeviceStatus\_Battery01** class has these types of members:</span></span>

-   [<span data-ttu-id="2fd01-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fd01-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fd01-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fd01-114">Properties</span></span>

<span data-ttu-id="2fd01-115">La **clase \_ \_ Battery01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2fd01-115">The **MDM\_DeviceStatus\_Battery01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2fd01-116">EstimatedChargeRemaining</span><span class="sxs-lookup"><span data-stu-id="2fd01-116">EstimatedChargeRemaining</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedchargeremaining)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd01-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fd01-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fd01-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2fd01-119">EstimatedRuntime</span><span class="sxs-lookup"><span data-stu-id="2fd01-119">EstimatedRuntime</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-estimatedruntime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd01-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fd01-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fd01-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2fd01-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2fd01-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd01-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fd01-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fd01-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fd01-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2fd01-126">Nodo para la consulta de batería.</span><span class="sxs-lookup"><span data-stu-id="2fd01-126">Node for the battery query.</span></span>

</dd> <dt>

<span data-ttu-id="2fd01-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2fd01-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd01-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fd01-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fd01-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fd01-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2fd01-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="2fd01-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="2fd01-132">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="2fd01-132">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="2fd01-133">Estado</span><span class="sxs-lookup"><span data-stu-id="2fd01-133">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fd01-134">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fd01-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fd01-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fd01-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fd01-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd01-136">Requirements</span></span>



| <span data-ttu-id="2fd01-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd01-137">Requirement</span></span> | <span data-ttu-id="2fd01-138">Value</span><span class="sxs-lookup"><span data-stu-id="2fd01-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd01-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fd01-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd01-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fd01-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2fd01-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fd01-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd01-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2fd01-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2fd01-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2fd01-143">Namespace</span></span><br/>                | <span data-ttu-id="2fd01-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2fd01-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2fd01-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2fd01-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fd01-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fd01-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fd01-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fd01-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd01-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fd01-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

