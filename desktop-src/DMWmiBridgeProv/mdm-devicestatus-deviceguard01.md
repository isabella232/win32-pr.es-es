---
title: MDM_DeviceStatus_DeviceGuard01 (clase)
description: '\_ \_ La empresa usa la clase DeviceGuard01 de DEVICESTATUS de MDM para realizar un seguimiento del inventario de dispositivos y consultar el estado de cumplimiento de estos dispositivos con sus directivas de empresa.'
ms.assetid: 267129f6-ec37-43ae-bba3-e21917012f27
keywords:
- MDM_DeviceStatus_DeviceGuard01 (clase)
- MDM_DeviceStatus_DeviceGuard01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_DeviceGuard01
- MDM_DeviceStatus_DeviceGuard01.InstanceID
- MDM_DeviceStatus_DeviceGuard01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5f4dffa67ad86b5486dce372018efd29e62620
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996792"
---
# <a name="mdm_devicestatus_deviceguard01-class"></a><span data-ttu-id="58598-105">\_Clase DeviceGuard01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="58598-105">MDM\_DeviceStatus\_DeviceGuard01 class</span></span>

<span data-ttu-id="58598-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="58598-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="58598-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="58598-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="58598-108">\_ \_ La empresa usa la clase DeviceGuard01 de DEVICESTATUS de MDM para realizar un seguimiento del inventario de dispositivos y consultar el estado de cumplimiento de estos dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="58598-108">The MDM\_DeviceStatus\_DeviceGuard01 class is used by the enterprise to keep track of device inventory and query the state of compliance of these devices with their enterprise policies.</span></span>

<span data-ttu-id="58598-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="58598-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58598-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58598-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_DeviceGuard01
{
  string InstanceID;
  string ParentID;
  sint32 VirtualizationBasedSecurityHwReq;
  sint32 VirtualizationBasedSecurityStatus;
  sint32 LsaCfgCredGuardStatus;
};
```

## <a name="members"></a><span data-ttu-id="58598-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="58598-111">Members</span></span>

<span data-ttu-id="58598-112">La **clase \_ \_ DeviceGuard01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="58598-112">The **MDM\_DeviceStatus\_DeviceGuard01** class has these types of members:</span></span>

-   [<span data-ttu-id="58598-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58598-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58598-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="58598-114">Properties</span></span>

<span data-ttu-id="58598-115">La **clase \_ \_ DeviceGuard01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="58598-115">The **MDM\_DeviceStatus\_DeviceGuard01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58598-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="58598-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58598-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="58598-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58598-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="58598-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58598-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58598-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="58598-120">LsaCfgCredGuardStatus</span><span class="sxs-lookup"><span data-stu-id="58598-120">LsaCfgCredGuardStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-lsacfgcredguardstatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="58598-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="58598-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="58598-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="58598-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="58598-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="58598-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58598-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="58598-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58598-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="58598-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58598-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58598-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="58598-127">VirtualizationBasedSecurityHwReq</span><span class="sxs-lookup"><span data-stu-id="58598-127">VirtualizationBasedSecurityHwReq</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecurityhwreq)
</dt> <dd> <dl> <dt>

<span data-ttu-id="58598-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="58598-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="58598-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="58598-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="58598-130">VirtualizationBasedSecurityStatus</span><span class="sxs-lookup"><span data-stu-id="58598-130">VirtualizationBasedSecurityStatus</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-deviceguard-virtualizationbasedsecuritystatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="58598-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="58598-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="58598-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="58598-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58598-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58598-133">Requirements</span></span>



| <span data-ttu-id="58598-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="58598-134">Requirement</span></span> | <span data-ttu-id="58598-135">Value</span><span class="sxs-lookup"><span data-stu-id="58598-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58598-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58598-136">Minimum supported client</span></span><br/> | <span data-ttu-id="58598-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="58598-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58598-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58598-138">Minimum supported server</span></span><br/> | <span data-ttu-id="58598-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="58598-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="58598-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="58598-140">Namespace</span></span><br/>                | <span data-ttu-id="58598-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="58598-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="58598-142">MOF</span><span class="sxs-lookup"><span data-stu-id="58598-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58598-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58598-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="58598-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58598-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58598-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58598-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

