---
title: MDM_EnterpriseModernAppManagement_AppManagement01_02 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM especifica si desea bloquear la actualización de una aplicación específica a través de actualizaciones automáticas.
ms.assetid: b018f61a-2458-4c1a-b75c-6ca5eebb2977
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_02 (clase)
- MDM_EnterpriseModernAppManagement_AppManagement01_02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_02
- MDM_EnterpriseModernAppManagement_AppManagement01_02.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11441e8700d10bc7b0d5bebd31c002802a857417
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491951"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_02-class"></a><span data-ttu-id="770ae-105">\_Clase EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM</span><span class="sxs-lookup"><span data-stu-id="770ae-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_02 class</span></span>

<span data-ttu-id="770ae-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="770ae-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="770ae-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="770ae-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="770ae-108">La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** especifica si desea bloquear la actualización de una aplicación específica a través de actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="770ae-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class specifies whether you want to block a specific app from being updated via auto-updates.</span></span>

<span data-ttu-id="770ae-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="770ae-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="770ae-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="770ae-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_02
{
  string InstanceID;
  string ParentID;
  sint32 DoNotUpdate;
};
```

## <a name="members"></a><span data-ttu-id="770ae-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="770ae-111">Members</span></span>

<span data-ttu-id="770ae-112">La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="770ae-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these types of members:</span></span>

-   [<span data-ttu-id="770ae-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="770ae-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="770ae-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="770ae-114">Properties</span></span>

<span data-ttu-id="770ae-115">La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 02 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="770ae-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="770ae-116">DoNotUpdate</span><span class="sxs-lookup"><span data-stu-id="770ae-116">DoNotUpdate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-donotupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="770ae-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="770ae-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="770ae-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="770ae-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="770ae-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="770ae-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="770ae-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="770ae-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="770ae-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="770ae-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="770ae-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="770ae-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="770ae-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="770ae-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="770ae-124">Para esta clase, la cadena es la instancia del nombre de familia del paquete.</span><span class="sxs-lookup"><span data-stu-id="770ae-124">For this class, the string is the instance of the package family name.</span></span>

</dd> <dt>

<span data-ttu-id="770ae-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="770ae-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="770ae-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="770ae-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="770ae-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="770ae-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="770ae-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="770ae-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="770ae-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="770ae-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="770ae-130">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*".</span><span class="sxs-lookup"><span data-stu-id="770ae-130">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="770ae-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="770ae-131">Requirements</span></span>



| <span data-ttu-id="770ae-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="770ae-132">Requirement</span></span> | <span data-ttu-id="770ae-133">Value</span><span class="sxs-lookup"><span data-stu-id="770ae-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="770ae-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="770ae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="770ae-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="770ae-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="770ae-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="770ae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="770ae-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="770ae-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="770ae-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="770ae-138">Namespace</span></span><br/>                | <span data-ttu-id="770ae-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="770ae-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="770ae-140">MOF</span><span class="sxs-lookup"><span data-stu-id="770ae-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="770ae-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="770ae-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="770ae-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="770ae-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="770ae-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="770ae-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="770ae-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="770ae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770ae-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="770ae-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

