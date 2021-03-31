---
title: MDM_EnterpriseModernAppManagement_AppSettingPolicy04 (clase)
description: La \_ clase AppSettingPolicy04 de EnterpriseModernAppManagement de MDM \_ especifica todos los valores de configuración de aplicación administrados.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04 (clase)
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9003ea7c9106f177958f7a15def3c60393346b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079596"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a><span data-ttu-id="0497b-105">\_Clase AppSettingPolicy04 EnterpriseModernAppManagement de MDM \_</span><span class="sxs-lookup"><span data-stu-id="0497b-105">MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04 class</span></span>

<span data-ttu-id="0497b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0497b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0497b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0497b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0497b-108">La **clase \_ \_ AppSettingPolicy04 de EnterpriseModernAppManagement de MDM** especifica todos los valores de configuración de aplicación administrados.</span><span class="sxs-lookup"><span data-stu-id="0497b-108">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class specifies all managed app setting values.</span></span>

<span data-ttu-id="0497b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0497b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0497b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0497b-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a><span data-ttu-id="0497b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0497b-111">Members</span></span>

<span data-ttu-id="0497b-112">La **clase \_ \_ AppSettingPolicy04 de MDM EnterpriseModernAppManagement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0497b-112">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these types of members:</span></span>

-   [<span data-ttu-id="0497b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0497b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0497b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0497b-114">Properties</span></span>

<span data-ttu-id="0497b-115">La **clase \_ \_ AppSettingPolicy04 de MDM EnterpriseModernAppManagement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0497b-115">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0497b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0497b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0497b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0497b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0497b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0497b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0497b-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0497b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0497b-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0497b-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="0497b-121">Para esta clase, la cadena "AppSettingPolicy".</span><span class="sxs-lookup"><span data-stu-id="0497b-121">For this class, the string "AppSettingPolicy".</span></span>

</dd> <dt>

[<span data-ttu-id="0497b-122">IsVariableLeaf</span><span class="sxs-lookup"><span data-stu-id="0497b-122">IsVariableLeaf</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0497b-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0497b-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0497b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0497b-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0497b-125">Agregado en Windows 10, versión 1511.</span><span class="sxs-lookup"><span data-stu-id="0497b-125">Added in Windows 10, version 1511.</span></span> <span data-ttu-id="0497b-126">Los **SettingValue** y los datos representan un par clave-valor que se configurará para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0497b-126">The **SettingValue** and data represent a key value pair to be configured for the app.</span></span> <span data-ttu-id="0497b-127">El nodo representa el nombre de la clave y los datos representan el valor.</span><span class="sxs-lookup"><span data-stu-id="0497b-127">The node represents the name of the key and the data represents the value.</span></span> <span data-ttu-id="0497b-128">Puede encontrar este valor en LocalSettings en el contenedor Managed. app. Settings.</span><span class="sxs-lookup"><span data-stu-id="0497b-128">You can find this value in LocalSettings in the Managed.App.Settings container.</span></span>

<span data-ttu-id="0497b-129">Esta configuración solo funciona para las aplicaciones que admiten la característica y solo se admite en el contexto de usuario.</span><span class="sxs-lookup"><span data-stu-id="0497b-129">This setting only works for apps that support the feature and it is only supported in the user context.</span></span>

</dd> <dt>

<span data-ttu-id="0497b-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0497b-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0497b-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0497b-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0497b-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0497b-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0497b-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0497b-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0497b-134">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0497b-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="0497b-135">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*".</span><span class="sxs-lookup"><span data-stu-id="0497b-135">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="0497b-136">**Value**</span><span class="sxs-lookup"><span data-stu-id="0497b-136">**Value**</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0497b-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0497b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0497b-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0497b-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0497b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0497b-139">Requirements</span></span>



| <span data-ttu-id="0497b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0497b-140">Requirement</span></span> | <span data-ttu-id="0497b-141">Value</span><span class="sxs-lookup"><span data-stu-id="0497b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0497b-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0497b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0497b-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0497b-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0497b-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0497b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0497b-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0497b-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0497b-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0497b-146">Namespace</span></span><br/>                | <span data-ttu-id="0497b-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="0497b-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0497b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0497b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0497b-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0497b-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0497b-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0497b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0497b-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0497b-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0497b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="0497b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0497b-153">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="0497b-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

