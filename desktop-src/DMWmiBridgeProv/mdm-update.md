---
title: MDM_Update (clase)
description: La \_ clase de actualización de MDM se utiliza para administrar y controlar el lanzamiento de nuevas actualizaciones.
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- MDM_Update (clase)
- MDM_Update clase, descrita
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2735b5eaaef4abc468586cb7608be7969a1eab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905164"
---
# <a name="mdm_update-class"></a><span data-ttu-id="ae08b-105">\_Clase de actualización MDM</span><span class="sxs-lookup"><span data-stu-id="ae08b-105">MDM\_Update class</span></span>

<span data-ttu-id="ae08b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ae08b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ae08b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ae08b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ae08b-108">La clase de **\_ actualización de MDM** se utiliza para administrar y controlar el lanzamiento de nuevas actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="ae08b-108">The **MDM\_Update** class is used to manage and control the rollout of new updates.</span></span>

<span data-ttu-id="ae08b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ae08b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae08b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae08b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a><span data-ttu-id="ae08b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae08b-111">Members</span></span>

<span data-ttu-id="ae08b-112">La clase de **\_ actualización MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ae08b-112">The **MDM\_Update** class has these types of members:</span></span>

-   [<span data-ttu-id="ae08b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae08b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae08b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae08b-114">Properties</span></span>

<span data-ttu-id="ae08b-115">La clase de **\_ actualización MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ae08b-115">The **MDM\_Update** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ae08b-116">DeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="ae08b-116">DeferUpgrade</span></span>](/windows/client-management/mdm/update-csp#deferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae08b-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ae08b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae08b-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ae08b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae08b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae08b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae08b-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae08b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae08b-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae08b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae08b-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae08b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae08b-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ae08b-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="ae08b-124">Para esta clase, la cadena es "Update".</span><span class="sxs-lookup"><span data-stu-id="ae08b-124">For this class, the string is "Update".</span></span>

</dd> <dt>

[<span data-ttu-id="ae08b-125">LastSuccessfulScanTime</span><span class="sxs-lookup"><span data-stu-id="ae08b-125">LastSuccessfulScanTime</span></span>](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae08b-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae08b-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae08b-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ae08b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae08b-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ae08b-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae08b-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae08b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae08b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae08b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae08b-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae08b-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae08b-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ae08b-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="ae08b-133">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="ae08b-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae08b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae08b-134">Requirements</span></span>



| <span data-ttu-id="ae08b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae08b-135">Requirement</span></span> | <span data-ttu-id="ae08b-136">Value</span><span class="sxs-lookup"><span data-stu-id="ae08b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae08b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae08b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ae08b-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae08b-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ae08b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae08b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ae08b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ae08b-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ae08b-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae08b-141">Namespace</span></span><br/>                | <span data-ttu-id="ae08b-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ae08b-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ae08b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ae08b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae08b-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae08b-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ae08b-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae08b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae08b-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="ae08b-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

