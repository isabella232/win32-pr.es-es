---
title: MDM_DeviceStatus_UAC01 (clase)
description: '\_ \_ La empresa usa la clase UAC01 de DEVICESTATUS de MDM para consultar el estado de UAC de los dispositivos con sus directivas de empresa.'
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- MDM_DeviceStatus_UAC01 (clase)
- MDM_DeviceStatus_UAC01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803115"
---
# <a name="mdm_devicestatus_uac01-class"></a><span data-ttu-id="0cd96-105">\_Clase UAC01 DeviceStatus de MDM \_</span><span class="sxs-lookup"><span data-stu-id="0cd96-105">MDM\_DeviceStatus\_UAC01 class</span></span>

<span data-ttu-id="0cd96-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0cd96-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0cd96-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0cd96-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0cd96-108">La empresa usa la clase **\_ \_ UAC01 de DeviceStatus de MDM** para consultar el estado de UAC de los dispositivos con sus directivas de empresa.</span><span class="sxs-lookup"><span data-stu-id="0cd96-108">The **MDM\_DeviceStatus\_UAC01** class is used by the enterprise to query the UAC status of devices with their enterprise policies.</span></span>

<span data-ttu-id="0cd96-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0cd96-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cd96-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cd96-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="0cd96-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0cd96-111">Members</span></span>

<span data-ttu-id="0cd96-112">La **clase \_ \_ UAC01 de MDM DeviceStatus** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0cd96-112">The **MDM\_DeviceStatus\_UAC01** class has these types of members:</span></span>

-   [<span data-ttu-id="0cd96-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0cd96-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0cd96-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0cd96-114">Properties</span></span>

<span data-ttu-id="0cd96-115">La **clase \_ \_ UAC01 de MDM DeviceStatus** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0cd96-115">The **MDM\_DeviceStatus\_UAC01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0cd96-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0cd96-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cd96-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0cd96-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cd96-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0cd96-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cd96-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0cd96-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0cd96-120">Nodo para la consulta de UAC.</span><span class="sxs-lookup"><span data-stu-id="0cd96-120">Node for the UAC query.</span></span>

</dd> <dt>

<span data-ttu-id="0cd96-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0cd96-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cd96-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0cd96-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0cd96-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0cd96-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0cd96-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0cd96-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0cd96-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0cd96-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="0cd96-126">Para esta clase, la cadena es "./Vendor/MSFT/DeviceStatus".</span><span class="sxs-lookup"><span data-stu-id="0cd96-126">For this class, the string is "./Vendor/MSFT/DeviceStatus"</span></span>

</dd> <dt>

[<span data-ttu-id="0cd96-127">Estado</span><span class="sxs-lookup"><span data-stu-id="0cd96-127">Status</span></span>](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0cd96-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0cd96-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0cd96-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0cd96-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cd96-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cd96-130">Requirements</span></span>



| <span data-ttu-id="0cd96-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cd96-131">Requirement</span></span> | <span data-ttu-id="0cd96-132">Value</span><span class="sxs-lookup"><span data-stu-id="0cd96-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cd96-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cd96-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0cd96-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0cd96-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0cd96-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cd96-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0cd96-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0cd96-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0cd96-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0cd96-137">Namespace</span></span><br/>                | <span data-ttu-id="0cd96-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="0cd96-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0cd96-139">MOF</span><span class="sxs-lookup"><span data-stu-id="0cd96-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cd96-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cd96-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cd96-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0cd96-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cd96-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cd96-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

