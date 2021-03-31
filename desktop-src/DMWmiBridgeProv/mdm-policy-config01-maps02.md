---
title: MDM_Policy_Config01_Maps02 (clase)
description: La \_ clase Config01 de Maps02 de directivas MDM \_ \_ representa las directivas de asignación disponibles.
ms.assetid: d2965f1f-a858-4b43-9c46-17ba718291b1
keywords:
- MDM_Policy_Config01_Maps02 (clase)
- MDM_Policy_Config01_Maps02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Maps02
- MDM_Policy_Config01_Maps02.InstanceID
- MDM_Policy_Config01_Maps02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090c8d077b3df4446054d29a8100a32923932736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150262"
---
# <a name="mdm_policy_config01_maps02-class"></a><span data-ttu-id="63885-105">\_ \_ Clase Maps02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="63885-105">MDM\_Policy\_Config01\_Maps02 class</span></span>

<span data-ttu-id="63885-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="63885-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="63885-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="63885-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="63885-108">La **clase \_ \_ Config01 de \_ Maps02 de directivas MDM** representa las directivas de asignación disponibles.</span><span class="sxs-lookup"><span data-stu-id="63885-108">The **MDM\_Policy\_Config01\_Maps02** class represents the map policies available.</span></span>

<span data-ttu-id="63885-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="63885-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63885-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63885-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Maps02
{
  string InstanceID;
  string ParentID;
  sint32 AllowOfflineMapsDownloadOverMeteredConnection;
  sint32 EnableOfflineMapsAutoUpdate;
};
```

## <a name="members"></a><span data-ttu-id="63885-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="63885-111">Members</span></span>

<span data-ttu-id="63885-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Maps02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63885-112">The **MDM\_Policy\_Config01\_Maps02** class has these types of members:</span></span>

-   [<span data-ttu-id="63885-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63885-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63885-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63885-114">Properties</span></span>

<span data-ttu-id="63885-115">La **clase \_ \_ Config01 de \_ Maps02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63885-115">The **MDM\_Policy\_Config01\_Maps02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="63885-116">AllowOfflineMapsDownloadOverMeteredConnection</span><span class="sxs-lookup"><span data-stu-id="63885-116">AllowOfflineMapsDownloadOverMeteredConnection</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-allowofflinemapsdownloadovermeteredconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63885-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63885-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63885-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63885-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63885-119">EnableOfflineMapsAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="63885-119">EnableOfflineMapsAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-maps#maps-enableofflinemapsautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63885-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63885-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63885-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63885-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63885-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63885-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63885-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63885-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63885-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63885-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63885-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63885-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63885-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="63885-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="63885-127">Para esta clase, la cadena es "Maps".</span><span class="sxs-lookup"><span data-stu-id="63885-127">For this class, the string is "Maps".</span></span>

</dd> <dt>

<span data-ttu-id="63885-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="63885-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63885-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63885-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63885-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63885-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63885-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63885-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63885-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="63885-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="63885-133">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="63885-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63885-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63885-134">Requirements</span></span>



| <span data-ttu-id="63885-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="63885-135">Requirement</span></span> | <span data-ttu-id="63885-136">Value</span><span class="sxs-lookup"><span data-stu-id="63885-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63885-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63885-137">Minimum supported client</span></span><br/> | <span data-ttu-id="63885-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="63885-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="63885-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63885-139">Minimum supported server</span></span><br/> | <span data-ttu-id="63885-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63885-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="63885-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63885-141">Namespace</span></span><br/>                | <span data-ttu-id="63885-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="63885-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="63885-143">MOF</span><span class="sxs-lookup"><span data-stu-id="63885-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63885-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63885-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="63885-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63885-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63885-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="63885-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

