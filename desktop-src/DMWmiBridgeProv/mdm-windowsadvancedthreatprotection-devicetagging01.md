---
title: MDM_WindowsAdvancedThreatProtection_DeviceTagging01 (clase)
description: La \_ clase DeviceTagging01 de WindowsAdvancedThreatProtection de MDM \_ se usa para incorporar, determinar el estado de configuración y mantenimiento, y los puntos de conexión de externalización para la protección contra amenazas avanzada de Windows Defender.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 (clase)
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01 clase, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150707"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="7d7f5-105">\_Clase DeviceTagging01 WindowsAdvancedThreatProtection de MDM \_</span><span class="sxs-lookup"><span data-stu-id="7d7f5-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="7d7f5-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d7f5-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7d7f5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d7f5-108">La \_ clase DeviceTagging01 de WindowsAdvancedThreatProtection de MDM \_ se usa para incorporar, determinar el estado de configuración y mantenimiento, y los puntos de conexión de externalización para la protección contra amenazas avanzada de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="7d7f5-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7f5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d7f5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="7d7f5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d7f5-111">Members</span></span>

<span data-ttu-id="7d7f5-112">La **clase \_ \_ DeviceTagging01 de MDM WindowsAdvancedThreatProtection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7d7f5-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="7d7f5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d7f5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d7f5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d7f5-114">Properties</span></span>

<span data-ttu-id="7d7f5-115">La **clase \_ \_ DeviceTagging01 de MDM WindowsAdvancedThreatProtection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7d7f5-116">Grado de importancia</span><span class="sxs-lookup"><span data-stu-id="7d7f5-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7f5-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7d7f5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d7f5-119">Grupo</span><span class="sxs-lookup"><span data-stu-id="7d7f5-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7f5-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7d7f5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d7f5-122">**IdMethod**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7f5-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7d7f5-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7d7f5-125">TBD</span><span class="sxs-lookup"><span data-stu-id="7d7f5-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="7d7f5-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7f5-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d7f5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d7f5-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d7f5-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d7f5-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d7f5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d7f5-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d7f5-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d7f5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d7f5-134">Requirements</span></span>



| <span data-ttu-id="7d7f5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d7f5-135">Requirement</span></span> | <span data-ttu-id="7d7f5-136">Value</span><span class="sxs-lookup"><span data-stu-id="7d7f5-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7f5-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d7f5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7d7f5-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d7f5-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d7f5-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d7f5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7d7f5-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7d7f5-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7d7f5-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d7f5-141">Namespace</span></span><br/>                | <span data-ttu-id="7d7f5-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7d7f5-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="7d7f5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7d7f5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d7f5-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d7f5-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d7f5-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d7f5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d7f5-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d7f5-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

