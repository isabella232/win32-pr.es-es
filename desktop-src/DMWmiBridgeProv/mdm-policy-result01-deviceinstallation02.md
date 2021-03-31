---
title: MDM_Policy_Result01_DeviceInstallation02 (clase)
description: La \_ clase Result01 de DeviceInstallation02 de directivas MDM \_ \_ representa las directivas de instalación de dispositivos disponibles.
ms.assetid: a5c89661-16f1-42e7-a11d-2c3a7945dac3
keywords:
- MDM_Policy_Result01_DeviceInstallation02 (clase)
- MDM_Policy_Result01_DeviceInstallation02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceInstallation02
- MDM_Policy_Result01_DeviceInstallation02.InstanceID
- MDM_Policy_Result01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6ec11cbfc5b0b38aa5e7482507108204b8798d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996100"
---
# <a name="mdm_policy_result01_deviceinstallation02-class"></a><span data-ttu-id="cac11-105">\_ \_ Clase DeviceInstallation02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="cac11-105">MDM\_Policy\_Result01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="cac11-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="cac11-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cac11-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="cac11-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cac11-108">La \_ clase Result01 de DeviceInstallation02 de directivas MDM \_ \_ representa las directivas de instalación de dispositivos disponibles.</span><span class="sxs-lookup"><span data-stu-id="cac11-108">The MDM\_Policy\_Result01\_DeviceInstallation02 class represents the available device installation policies.</span></span>

<span data-ttu-id="cac11-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cac11-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac11-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cac11-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="cac11-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cac11-111">Members</span></span>

<span data-ttu-id="cac11-112">La clase Result01 de la **\_ Directiva MDM \_ \_ DeviceInstallation02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cac11-112">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="cac11-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cac11-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cac11-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cac11-114">Properties</span></span>

<span data-ttu-id="cac11-115">La **clase \_ \_ Result01 de \_ DeviceInstallation02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cac11-115">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cac11-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cac11-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cac11-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cac11-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cac11-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cac11-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cac11-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cac11-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cac11-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cac11-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cac11-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cac11-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cac11-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cac11-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cac11-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cac11-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cac11-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="cac11-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cac11-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cac11-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cac11-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cac11-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cac11-127">PreventInstallationOfMatchingDeviceSetupClasses</span><span class="sxs-lookup"><span data-stu-id="cac11-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cac11-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cac11-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cac11-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cac11-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cac11-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac11-130">Requirements</span></span>



| <span data-ttu-id="cac11-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac11-131">Requirement</span></span> | <span data-ttu-id="cac11-132">Value</span><span class="sxs-lookup"><span data-stu-id="cac11-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac11-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cac11-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cac11-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="cac11-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cac11-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cac11-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cac11-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cac11-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cac11-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cac11-137">Namespace</span></span><br/>                | <span data-ttu-id="cac11-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="cac11-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cac11-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cac11-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cac11-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cac11-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cac11-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cac11-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac11-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac11-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

