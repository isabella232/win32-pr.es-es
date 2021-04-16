---
title: MDM_AssignedAccess (clase)
description: La \_ clase AssignedAccess de MDM se usa para establecer que el dispositivo se ejecute en modo de quiosco.
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- MDM_AssignedAccess (clase)
- MDM_AssignedAccess clase, descrita
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492965"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="bf4d0-105">\_Clase AssignedAccess de MDM</span><span class="sxs-lookup"><span data-stu-id="bf4d0-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="bf4d0-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf4d0-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="bf4d0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf4d0-108">La **clase \_ AssignedAccess de MDM** se usa para establecer que el dispositivo se ejecute en modo de quiosco.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="bf4d0-109">Una vez que se ha ejecutado la clase, el siguiente inicio de sesión de usuario que está asociado con el modo de pantalla completa coloca el dispositivo en el modo de pantalla completa que ejecuta la aplicación especificada en el paquete de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="bf4d0-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf4d0-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf4d0-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="bf4d0-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf4d0-112">Members</span></span>

<span data-ttu-id="bf4d0-113">La **clase \_ AssignedAccess de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf4d0-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="bf4d0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf4d0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf4d0-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf4d0-115">Properties</span></span>

<span data-ttu-id="bf4d0-116">La **clase \_ AssignedAccess de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bf4d0-117">Configuración</span><span class="sxs-lookup"><span data-stu-id="bf4d0-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf4d0-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf4d0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf4d0-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bf4d0-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bf4d0-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf4d0-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf4d0-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf4d0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf4d0-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf4d0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf4d0-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf4d0-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf4d0-124">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="bf4d0-125">Para esta clase, la cadena es "AssignedAccess".</span><span class="sxs-lookup"><span data-stu-id="bf4d0-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="bf4d0-126">KioskModeApp</span><span class="sxs-lookup"><span data-stu-id="bf4d0-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf4d0-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf4d0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf4d0-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bf4d0-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bf4d0-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bf4d0-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf4d0-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf4d0-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf4d0-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf4d0-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf4d0-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf4d0-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf4d0-133">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="bf4d0-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="bf4d0-134">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="bf4d0-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf4d0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf4d0-135">Requirements</span></span>



| <span data-ttu-id="bf4d0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf4d0-136">Requirement</span></span> | <span data-ttu-id="bf4d0-137">Value</span><span class="sxs-lookup"><span data-stu-id="bf4d0-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4d0-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf4d0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bf4d0-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf4d0-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf4d0-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf4d0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bf4d0-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bf4d0-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bf4d0-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bf4d0-142">Namespace</span></span><br/>                | <span data-ttu-id="bf4d0-143">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="bf4d0-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bf4d0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="bf4d0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf4d0-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf4d0-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf4d0-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf4d0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf4d0-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf4d0-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf4d0-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf4d0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf4d0-149">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="bf4d0-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

