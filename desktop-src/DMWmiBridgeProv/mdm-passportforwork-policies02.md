---
title: MDM_PassportForWork_Policies02 (clase)
description: La \_ clase Policies02 de PassportForWork de MDM \_ aprovisiona Windows Hello para empresas.
ms.assetid: 362fe819-a68a-4433-8b43-201d9678a8da
keywords:
- MDM_PassportForWork_Policies02 (clase)
- MDM_PassportForWork_Policies02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Policies02
- MDM_PassportForWork_Policies02.InstanceID
- MDM_PassportForWork_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf407289f93f5ecff0e57ebf7b7fa8d9844183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996198"
---
# <a name="mdm_passportforwork_policies02-class"></a><span data-ttu-id="701ee-105">\_Clase Policies02 PassportForWork de MDM \_</span><span class="sxs-lookup"><span data-stu-id="701ee-105">MDM\_PassportForWork\_Policies02 class</span></span>

<span data-ttu-id="701ee-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="701ee-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="701ee-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="701ee-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="701ee-108">La **clase \_ \_ Policies02 de PassportForWork de MDM** aprovisiona Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="701ee-108">The **MDM\_PassportForWork\_Policies02** class provisions Windows Hello for Business.</span></span>

<span data-ttu-id="701ee-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="701ee-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="701ee-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="701ee-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UsePassportForWork;
  boolean RequireSecurityDevice;
};
```

## <a name="members"></a><span data-ttu-id="701ee-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="701ee-111">Members</span></span>

<span data-ttu-id="701ee-112">La **clase \_ \_ Policies02 de MDM PassportForWork** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="701ee-112">The **MDM\_PassportForWork\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="701ee-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="701ee-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="701ee-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="701ee-114">Properties</span></span>

<span data-ttu-id="701ee-115">La **clase \_ \_ Policies02 de MDM PassportForWork** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="701ee-115">The **MDM\_PassportForWork\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="701ee-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="701ee-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701ee-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="701ee-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701ee-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="701ee-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701ee-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="701ee-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="701ee-120">Nodo raíz para las directivas de Windows Hello para empresas.</span><span class="sxs-lookup"><span data-stu-id="701ee-120">Root node for Windows Hello for Business policies.</span></span>

</dd> <dt>

<span data-ttu-id="701ee-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="701ee-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="701ee-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="701ee-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="701ee-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="701ee-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="701ee-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="701ee-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="701ee-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="701ee-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="701ee-126">Para esta clase, la cadena es "./Vendor/MSFT/PassPortForWork/*TenantID*"</span><span class="sxs-lookup"><span data-stu-id="701ee-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*"</span></span>

</dd> <dt>

[<span data-ttu-id="701ee-127">RequireSecurityDevice</span><span class="sxs-lookup"><span data-stu-id="701ee-127">RequireSecurityDevice</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-requiresecuritydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="701ee-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="701ee-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701ee-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="701ee-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="701ee-130">UsePassportForWork</span><span class="sxs-lookup"><span data-stu-id="701ee-130">UsePassportForWork</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-usepassportforwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="701ee-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="701ee-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="701ee-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="701ee-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="701ee-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="701ee-133">Requirements</span></span>



| <span data-ttu-id="701ee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="701ee-134">Requirement</span></span> | <span data-ttu-id="701ee-135">Value</span><span class="sxs-lookup"><span data-stu-id="701ee-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="701ee-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="701ee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="701ee-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="701ee-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="701ee-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="701ee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="701ee-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="701ee-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="701ee-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="701ee-140">Namespace</span></span><br/>                | <span data-ttu-id="701ee-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="701ee-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="701ee-142">MOF</span><span class="sxs-lookup"><span data-stu-id="701ee-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="701ee-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="701ee-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="701ee-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="701ee-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="701ee-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="701ee-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="701ee-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="701ee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701ee-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="701ee-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

