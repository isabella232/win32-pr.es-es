---
title: MDM_Update_InstallableUpdates01_01 (clase)
description: La \_ \_ \_ clase de actualización INSTALLABLEUPDATES01 01 de MDM se utiliza para administrar y controlar el lanzamiento de las actualizaciones aprobadas.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- MDM_Update_InstallableUpdates01_01 (clase)
- MDM_Update_InstallableUpdates01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905020"
---
# <a name="mdm_update_installableupdates01_01-class"></a><span data-ttu-id="0764b-105">\_ \_ Clase InstallableUpdates01 01 de actualización \_ de MDM</span><span class="sxs-lookup"><span data-stu-id="0764b-105">MDM\_Update\_InstallableUpdates01\_01 class</span></span>

<span data-ttu-id="0764b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0764b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0764b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0764b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0764b-108">La clase de **\_ actualización \_ InstallableUpdates01 \_ 01 de MDM** se utiliza para administrar y controlar el lanzamiento de las actualizaciones aprobadas.</span><span class="sxs-lookup"><span data-stu-id="0764b-108">The **MDM\_Update\_InstallableUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="0764b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0764b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0764b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0764b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a><span data-ttu-id="0764b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0764b-111">Members</span></span>

<span data-ttu-id="0764b-112">La clase de **\_ actualización \_ InstallableUpdates01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0764b-112">The **MDM\_Update\_InstallableUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="0764b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0764b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0764b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0764b-114">Properties</span></span>

<span data-ttu-id="0764b-115">La clase de **\_ actualización \_ InstallableUpdates01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0764b-115">The **MDM\_Update\_InstallableUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0764b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0764b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0764b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0764b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0764b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0764b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0764b-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0764b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0764b-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0764b-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="0764b-121">Para esta clase, la cadena es el GUID de la actualización aprobada.</span><span class="sxs-lookup"><span data-stu-id="0764b-121">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="0764b-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0764b-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0764b-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0764b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0764b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0764b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0764b-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0764b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0764b-126">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0764b-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="0764b-127">Para esta clase, la cadena es "./Vendor/MSFT/Update/InstallableUpdates".</span><span class="sxs-lookup"><span data-stu-id="0764b-127">For this class, the string is "./Vendor/MSFT/Update/InstallableUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="0764b-128">RevisionNumber</span><span class="sxs-lookup"><span data-stu-id="0764b-128">RevisionNumber</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0764b-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0764b-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0764b-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0764b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0764b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0764b-131">Type</span></span>](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0764b-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0764b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0764b-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0764b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0764b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0764b-134">Requirements</span></span>



| <span data-ttu-id="0764b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0764b-135">Requirement</span></span> | <span data-ttu-id="0764b-136">Value</span><span class="sxs-lookup"><span data-stu-id="0764b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0764b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0764b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0764b-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0764b-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0764b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0764b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0764b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0764b-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="0764b-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0764b-141">Namespace</span></span><br/>                | <span data-ttu-id="0764b-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="0764b-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="0764b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0764b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0764b-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0764b-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="0764b-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0764b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0764b-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="0764b-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

