---
title: MDM_Policy_Result01_Maps02 (clase)
description: La \_ clase Result01 de Maps02 de directivas MDM \_ \_ representa las directivas de asignación disponibles.
ms.assetid: 09a2755c-1d2c-4c34-a5e7-d8fc07b55ad8
keywords:
- MDM_Policy_Result01_Maps02 (clase)
- MDM_Policy_Result01_Maps02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Maps02
- MDM_Policy_Result01_Maps02.InstanceID
- MDM_Policy_Result01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bc3676a8c2900cba6afcbeff20839153ec3320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490162"
---
# <a name="mdm_policy_result01_maps02-class"></a><span data-ttu-id="4d01e-105">\_ \_ Clase Maps02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="4d01e-105">MDM\_Policy\_Result01\_Maps02 class</span></span>

<span data-ttu-id="4d01e-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="4d01e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4d01e-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="4d01e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4d01e-108">La **clase \_ \_ Result01 de \_ Maps02 de directivas MDM** representa las directivas de asignación disponibles.</span><span class="sxs-lookup"><span data-stu-id="4d01e-108">The **MDM\_Policy\_Result01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="4d01e-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4d01e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d01e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d01e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="4d01e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d01e-111">Members</span></span>

<span data-ttu-id="4d01e-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Maps02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d01e-112">The **MDM\_Policy\_Result01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="4d01e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d01e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d01e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d01e-114">Properties</span></span>

<span data-ttu-id="4d01e-115">La **clase \_ \_ Result01 de \_ Maps02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d01e-115">The **MDM\_Policy\_Result01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4d01e-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="4d01e-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d01e-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4d01e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d01e-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d01e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4d01e-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4d01e-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d01e-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4d01e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4d01e-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d01e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4d01e-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4d01e-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d01e-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d01e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d01e-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d01e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d01e-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4d01e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4d01e-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="4d01e-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="4d01e-127">Para esta clase, la cadena es "Maps".</span><span class="sxs-lookup"><span data-stu-id="4d01e-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="4d01e-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4d01e-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d01e-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d01e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d01e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d01e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d01e-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4d01e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4d01e-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="4d01e-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="4d01e-133">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="4d01e-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d01e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d01e-134">Requirements</span></span>



| <span data-ttu-id="4d01e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d01e-135">Requirement</span></span> | <span data-ttu-id="4d01e-136">Value</span><span class="sxs-lookup"><span data-stu-id="4d01e-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d01e-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d01e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4d01e-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d01e-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4d01e-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d01e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4d01e-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4d01e-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4d01e-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d01e-141">Namespace</span></span><br/>                | <span data-ttu-id="4d01e-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="4d01e-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="4d01e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4d01e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d01e-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d01e-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="4d01e-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d01e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d01e-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="4d01e-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

