---
title: MDM_EnterpriseDataProtection (clase)
description: La \_ clase EnterpriseDataProtection de MDM se usa para determinar el estado actual de la configuración específica de Windows Information Protection (WIP) (anteriormente conocido como protección de datos empresariales).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- MDM_EnterpriseDataProtection (clase)
- MDM_EnterpriseDataProtection clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b4a3a1d9d491b6970ee95a081de8bb240d54d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491956"
---
# <a name="mdm_enterprisedataprotection-class"></a><span data-ttu-id="ed2ac-105">\_Clase EnterpriseDataProtection de MDM</span><span class="sxs-lookup"><span data-stu-id="ed2ac-105">MDM\_EnterpriseDataProtection class</span></span>

<span data-ttu-id="ed2ac-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed2ac-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ed2ac-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed2ac-108">La **clase \_ EnterpriseDataProtection de MDM** se usa para determinar el estado actual de la configuración específica de Windows Information Protection (WIP) (anteriormente conocido como protección de datos empresariales).</span><span class="sxs-lookup"><span data-stu-id="ed2ac-108">The **MDM\_EnterpriseDataProtection** class is used to determine the current status of Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span>

<span data-ttu-id="ed2ac-109">Para obtener más información sobre WIP, consulte protección [de los datos de la empresa mediante la protección de datos empresariales (este)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="ed2ac-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="ed2ac-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2ac-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed2ac-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="ed2ac-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="ed2ac-112">Members</span></span>

<span data-ttu-id="ed2ac-113">La **clase \_ EnterpriseDataProtection de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ed2ac-113">The **MDM\_EnterpriseDataProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="ed2ac-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed2ac-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed2ac-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed2ac-115">Properties</span></span>

<span data-ttu-id="ed2ac-116">La **clase \_ EnterpriseDataProtection de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-116">The **MDM\_EnterpriseDataProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed2ac-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ed2ac-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2ac-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ed2ac-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2ac-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed2ac-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed2ac-120">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed2ac-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed2ac-121">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-121">Identifies the name of the parent node.</span></span> <span data-ttu-id="ed2ac-122">Para esta clase, la cadena es "EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="ed2ac-122">For this class, the string is "EnterpriseDataProtection".</span></span>

</dd> <dt>

<span data-ttu-id="ed2ac-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ed2ac-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2ac-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ed2ac-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed2ac-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ed2ac-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed2ac-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed2ac-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed2ac-127">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ed2ac-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="ed2ac-128">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="ed2ac-128">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="ed2ac-129">Estado</span><span class="sxs-lookup"><span data-stu-id="ed2ac-129">Status</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed2ac-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ed2ac-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed2ac-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ed2ac-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed2ac-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed2ac-132">Requirements</span></span>



| <span data-ttu-id="ed2ac-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed2ac-133">Requirement</span></span> | <span data-ttu-id="ed2ac-134">Value</span><span class="sxs-lookup"><span data-stu-id="ed2ac-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2ac-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed2ac-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ed2ac-136">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed2ac-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ed2ac-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed2ac-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ed2ac-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ed2ac-138">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ed2ac-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed2ac-139">Namespace</span></span><br/>                | <span data-ttu-id="ed2ac-140">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ed2ac-140">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ed2ac-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ed2ac-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed2ac-142"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed2ac-142"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ed2ac-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ed2ac-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed2ac-144"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="ed2ac-144"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

