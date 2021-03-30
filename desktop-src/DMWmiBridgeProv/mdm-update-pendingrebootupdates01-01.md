---
title: MDM_Update_PendingRebootUpdates01_01 (clase)
description: La \_ clase de actualización \_ PendingRebootUpdates01 01 de MDM \_ se utiliza para administrar las actualizaciones pendientes de reinicio.
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- MDM_Update_PendingRebootUpdates01_01 (clase)
- MDM_Update_PendingRebootUpdates01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca640a4de00ea9eb115b999129a16dd0bf930cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150965"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a><span data-ttu-id="dc8d1-105">\_ \_ Clase PendingRebootUpdates01 01 de actualización \_ de MDM</span><span class="sxs-lookup"><span data-stu-id="dc8d1-105">MDM\_Update\_PendingRebootUpdates01\_01 class</span></span>

<span data-ttu-id="dc8d1-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dc8d1-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="dc8d1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dc8d1-108">La clase de **\_ actualización \_ PendingRebootUpdates01 \_ 01 de MDM** se utiliza para administrar las actualizaciones pendientes de reinicio.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-108">The **MDM\_Update\_PendingRebootUpdates01\_01** class is used to manage updates that are pending on reboot.</span></span>

<span data-ttu-id="dc8d1-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8d1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc8d1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a><span data-ttu-id="dc8d1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc8d1-111">Members</span></span>

<span data-ttu-id="dc8d1-112">La clase de **\_ actualización \_ PendingRebootUpdates01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc8d1-112">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="dc8d1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc8d1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc8d1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc8d1-114">Properties</span></span>

<span data-ttu-id="dc8d1-115">La clase de **\_ actualización \_ PendingRebootUpdates01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-115">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dc8d1-116">InstalledTime</span><span class="sxs-lookup"><span data-stu-id="dc8d1-116">InstalledTime</span></span>](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc8d1-117">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc8d1-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc8d1-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dc8d1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dc8d1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dc8d1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc8d1-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc8d1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc8d1-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc8d1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc8d1-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc8d1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc8d1-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="dc8d1-124">Para esta clase, la cadena es el GUID de la actualización que está pendiente de reinicio.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-124">For this class, the string is the GUID of the update that is pending reboot.</span></span>

</dd> <dt>

<span data-ttu-id="dc8d1-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dc8d1-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc8d1-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dc8d1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc8d1-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dc8d1-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc8d1-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dc8d1-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dc8d1-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="dc8d1-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="dc8d1-130">Para esta clase, la cadena es "./Vendor/MSFT/Update/PendingRebootUpdates".</span><span class="sxs-lookup"><span data-stu-id="dc8d1-130">For this class, the string is "./Vendor/MSFT/Update/PendingRebootUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc8d1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc8d1-131">Requirements</span></span>



| <span data-ttu-id="dc8d1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc8d1-132">Requirement</span></span> | <span data-ttu-id="dc8d1-133">Value</span><span class="sxs-lookup"><span data-stu-id="dc8d1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8d1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc8d1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dc8d1-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc8d1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dc8d1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc8d1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dc8d1-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dc8d1-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="dc8d1-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc8d1-138">Namespace</span></span><br/>                | <span data-ttu-id="dc8d1-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="dc8d1-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="dc8d1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dc8d1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc8d1-141"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc8d1-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="dc8d1-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc8d1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc8d1-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc8d1-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

