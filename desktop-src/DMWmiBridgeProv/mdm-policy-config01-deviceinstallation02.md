---
title: MDM_Policy_Config01_DeviceInstallation02 (clase)
description: La \_ clase Config01 de DeviceInstallation02 de directivas MDM \_ \_ configura las directivas de instalación de dispositivos disponibles.
ms.assetid: 6aa60809-d6c7-4dfb-9144-e5d69466f454
keywords:
- MDM_Policy_Config01_DeviceInstallation02 (clase)
- MDM_Policy_Config01_DeviceInstallation02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceInstallation02
- MDM_Policy_Config01_DeviceInstallation02.InstanceID
- MDM_Policy_Config01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79df6829f05a49ff5f16e3d8e0cd3dfabfc7bbf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905130"
---
# <a name="mdm_policy_config01_deviceinstallation02-class"></a><span data-ttu-id="2840a-105">\_ \_ Clase DeviceInstallation02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="2840a-105">MDM\_Policy\_Config01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="2840a-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2840a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2840a-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2840a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2840a-108">La \_ clase Config01 de DeviceInstallation02 de directivas MDM \_ \_ configura las directivas de instalación de dispositivos disponibles.</span><span class="sxs-lookup"><span data-stu-id="2840a-108">The MDM\_Policy\_Config01\_DeviceInstallation02 class configures the available device installation policies.</span></span>

<span data-ttu-id="2840a-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2840a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2840a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2840a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="2840a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2840a-111">Members</span></span>

<span data-ttu-id="2840a-112">La clase Config01 de la **\_ Directiva MDM \_ \_ DeviceInstallation02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2840a-112">The **MDM\_Policy\_Config01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="2840a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2840a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2840a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2840a-114">Properties</span></span>

<span data-ttu-id="2840a-115">La **clase \_ \_ Config01 de \_ DeviceInstallation02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2840a-115">The **MDM\_Policy\_Config01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2840a-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2840a-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2840a-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2840a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2840a-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2840a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2840a-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2840a-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2840a-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2840a-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2840a-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2840a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2840a-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2840a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2840a-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2840a-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2840a-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="2840a-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2840a-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2840a-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2840a-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2840a-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2840a-127">PreventInstallationOfMatchingDeviceSetupClasses</span><span class="sxs-lookup"><span data-stu-id="2840a-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2840a-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2840a-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2840a-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2840a-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2840a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2840a-130">Requirements</span></span>



| <span data-ttu-id="2840a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2840a-131">Requirement</span></span> | <span data-ttu-id="2840a-132">Value</span><span class="sxs-lookup"><span data-stu-id="2840a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2840a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2840a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2840a-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2840a-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2840a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2840a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2840a-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2840a-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2840a-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2840a-137">Namespace</span></span><br/>                | <span data-ttu-id="2840a-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2840a-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2840a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2840a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2840a-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2840a-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2840a-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2840a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2840a-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2840a-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

