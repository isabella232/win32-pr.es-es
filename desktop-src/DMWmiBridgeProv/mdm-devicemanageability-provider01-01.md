---
title: MDM_DeviceManageability_Provider01_01 (clase)
description: La \_ clase DeviceManageability \_ Provider01 \_ 01 de MDM se usa para recuperar la información general sobre las funcionalidades de configuración de MDM en el dispositivo.
ms.assetid: 080e5cdd-4509-42d6-b5f8-36df6f8d9b45
keywords:
- MDM_DeviceManageability_Provider01_01 (clase)
- MDM_DeviceManageability_Provider01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_DeviceManageability_Provider01_01
- MDM_DeviceManageability_Provider01_01.InstanceID
- MDM_DeviceManageability_Provider01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1ef064bcffd5303a3ef820dc0b463a3b5e622b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905442"
---
# <a name="mdm_devicemanageability_provider01_01-class"></a><span data-ttu-id="92c06-105">\_Clase DeviceManageability \_ Provider01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="92c06-105">MDM\_DeviceManageability\_Provider01\_01 class</span></span>

<span data-ttu-id="92c06-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="92c06-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="92c06-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="92c06-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="92c06-108">La \_ clase DeviceManageability \_ Provider01 \_ 01 de MDM se usa para recuperar la información general sobre las funcionalidades de configuración de MDM en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92c06-108">The MDM\_DeviceManageability\_Provider01\_01 class is used retrieve the general information about MDM configuration capabilities on the device.</span></span>

<span data-ttu-id="92c06-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="92c06-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c06-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92c06-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_DeviceManageability_Provider01_01
{
  string InstanceID;
  string ParentID;
  string ConfigInfo;
  string EnrollmentInfo;
};
```

## <a name="members"></a><span data-ttu-id="92c06-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="92c06-111">Members</span></span>

<span data-ttu-id="92c06-112">La **clase \_ DeviceManageability \_ Provider01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="92c06-112">The **MDM\_DeviceManageability\_Provider01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="92c06-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92c06-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92c06-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92c06-114">Properties</span></span>

<span data-ttu-id="92c06-115">La **clase \_ DeviceManageability \_ Provider01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="92c06-115">The **MDM\_DeviceManageability\_Provider01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="92c06-116">ConfigInfo</span><span class="sxs-lookup"><span data-stu-id="92c06-116">ConfigInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c06-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="92c06-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c06-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="92c06-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="92c06-119">Debe establecer el valor en servidor de \_ puente WMI \_ .</span><span class="sxs-lookup"><span data-stu-id="92c06-119">You must set the value to WMI\_Bridge\_Server.</span></span> <span data-ttu-id="92c06-120">El autor de la llamada no puede establecer de forma dinámica el identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="92c06-120">The caller cannot dynamically set the Provider ID.</span></span>

</dd> <dt>

[<span data-ttu-id="92c06-121">EnrollmentInfo</span><span class="sxs-lookup"><span data-stu-id="92c06-121">EnrollmentInfo</span></span>](/windows/client-management/mdm/devicemanageability-csp#capabilities-cspversions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c06-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="92c06-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c06-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="92c06-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="92c06-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="92c06-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c06-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="92c06-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c06-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="92c06-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c06-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92c06-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="92c06-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="92c06-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c06-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="92c06-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c06-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="92c06-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c06-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92c06-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92c06-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c06-132">Requirements</span></span>



| <span data-ttu-id="92c06-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c06-133">Requirement</span></span> | <span data-ttu-id="92c06-134">Value</span><span class="sxs-lookup"><span data-stu-id="92c06-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c06-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92c06-135">Minimum supported client</span></span><br/> | <span data-ttu-id="92c06-136">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="92c06-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="92c06-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92c06-137">Minimum supported server</span></span><br/> | <span data-ttu-id="92c06-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="92c06-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="92c06-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="92c06-139">Namespace</span></span><br/>                | <span data-ttu-id="92c06-140">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="92c06-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="92c06-141">MOF</span><span class="sxs-lookup"><span data-stu-id="92c06-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c06-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c06-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c06-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92c06-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c06-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c06-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

