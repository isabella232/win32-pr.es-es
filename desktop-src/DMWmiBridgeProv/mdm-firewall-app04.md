---
title: MDM_Firewall_App04 (clase)
description: La \_ clase App04 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- MDM_Firewall_App04 (clase)
- MDM_Firewall_App04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150121"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="3e808-105">\_Clase App04 de Firewall de MDM \_</span><span class="sxs-lookup"><span data-stu-id="3e808-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="3e808-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3e808-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e808-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3e808-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e808-108">La \_ clase App04 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="3e808-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="3e808-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3e808-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e808-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e808-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="3e808-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e808-111">Members</span></span>

<span data-ttu-id="3e808-112">La **clase \_ \_ App04 de Firewall de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e808-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="3e808-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e808-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e808-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e808-114">Properties</span></span>

<span data-ttu-id="3e808-115">La **clase \_ \_ App04 de Firewall de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3e808-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3e808-116">FilePath</span><span class="sxs-lookup"><span data-stu-id="3e808-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e808-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e808-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e808-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e808-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e808-119">Fqbn</span><span class="sxs-lookup"><span data-stu-id="3e808-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e808-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e808-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e808-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e808-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e808-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e808-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e808-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e808-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e808-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e808-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e808-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e808-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e808-126">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="3e808-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e808-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e808-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e808-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e808-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e808-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3e808-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e808-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e808-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e808-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e808-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e808-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e808-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e808-133">ServiceName</span><span class="sxs-lookup"><span data-stu-id="3e808-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e808-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e808-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e808-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e808-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e808-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e808-136">Requirements</span></span>



| <span data-ttu-id="3e808-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e808-137">Requirement</span></span> | <span data-ttu-id="3e808-138">Value</span><span class="sxs-lookup"><span data-stu-id="3e808-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e808-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e808-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3e808-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e808-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e808-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e808-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3e808-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e808-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="3e808-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e808-143">Namespace</span></span><br/>                | <span data-ttu-id="3e808-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="3e808-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="3e808-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3e808-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e808-146"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e808-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e808-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e808-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e808-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e808-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

