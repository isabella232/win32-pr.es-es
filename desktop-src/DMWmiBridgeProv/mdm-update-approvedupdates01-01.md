---
title: MDM_Update_ApprovedUpdates01_01 (clase)
description: La \_ \_ \_ clase de actualización APPROVEDUPDATES01 01 de MDM se utiliza para administrar y controlar el lanzamiento de las actualizaciones aprobadas.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- MDM_Update_ApprovedUpdates01_01 (clase)
- MDM_Update_ApprovedUpdates01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995960"
---
# <a name="mdm_update_approvedupdates01_01-class"></a><span data-ttu-id="f6e6c-105">\_ \_ Clase ApprovedUpdates01 01 de actualización \_ de MDM</span><span class="sxs-lookup"><span data-stu-id="f6e6c-105">MDM\_Update\_ApprovedUpdates01\_01 class</span></span>

<span data-ttu-id="f6e6c-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f6e6c-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f6e6c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f6e6c-108">La clase de **\_ actualización \_ ApprovedUpdates01 \_ 01 de MDM** se utiliza para administrar y controlar el lanzamiento de las actualizaciones aprobadas.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-108">The **MDM\_Update\_ApprovedUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="f6e6c-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e6c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6e6c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a><span data-ttu-id="f6e6c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6e6c-111">Members</span></span>

<span data-ttu-id="f6e6c-112">La clase de **\_ actualización \_ ApprovedUpdates01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6e6c-112">The **MDM\_Update\_ApprovedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="f6e6c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6e6c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6e6c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6e6c-114">Properties</span></span>

<span data-ttu-id="f6e6c-115">La clase de **\_ actualización \_ ApprovedUpdates01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-115">The **MDM\_Update\_ApprovedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f6e6c-116">ApprovedTime</span><span class="sxs-lookup"><span data-stu-id="f6e6c-116">ApprovedTime</span></span>](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e6c-117">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f6e6c-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f6e6c-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6e6c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6e6c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6e6c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e6c-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6e6c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6e6c-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e6c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6e6c-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6e6c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6e6c-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f6e6c-124">Para esta clase, la cadena es el GUID de la actualización aprobada.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-124">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="f6e6c-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f6e6c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e6c-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6e6c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6e6c-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e6c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6e6c-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6e6c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6e6c-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f6e6c-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="f6e6c-130">Para esta clase, la cadena es "./Vendor/MSFT/Update/ApprovedUpdates".</span><span class="sxs-lookup"><span data-stu-id="f6e6c-130">For this class, the string is "./Vendor/MSFT/Update/ApprovedUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6e6c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6e6c-131">Requirements</span></span>



| <span data-ttu-id="f6e6c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6e6c-132">Requirement</span></span> | <span data-ttu-id="f6e6c-133">Value</span><span class="sxs-lookup"><span data-stu-id="f6e6c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e6c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6e6c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e6c-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6e6c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f6e6c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6e6c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e6c-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f6e6c-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f6e6c-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6e6c-138">Namespace</span></span><br/>                | <span data-ttu-id="f6e6c-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f6e6c-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f6e6c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f6e6c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6e6c-141"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6e6c-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="f6e6c-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6e6c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e6c-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="f6e6c-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

