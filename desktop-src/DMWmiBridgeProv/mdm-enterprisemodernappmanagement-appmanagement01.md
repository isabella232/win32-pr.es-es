---
title: MDM_EnterpriseModernAppManagement_AppManagement01 (clase)
description: La \_ clase AppManagement01 de EnterpriseModernAppManagement de MDM \_ inicia el examen Windows Update e informa del último error de examen.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01 (clase)
- MDM_EnterpriseModernAppManagement_AppManagement01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274529"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="47d01-105">\_Clase AppManagement01 EnterpriseModernAppManagement de MDM \_</span><span class="sxs-lookup"><span data-stu-id="47d01-105">MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="47d01-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="47d01-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="47d01-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="47d01-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="47d01-108">La **clase \_ \_ AppManagement01 de EnterpriseModernAppManagement de MDM** inicia el examen Windows Update e informa del último error de examen.</span><span class="sxs-lookup"><span data-stu-id="47d01-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class starts the Windows Update scan and reports the last scan error.</span></span>

<span data-ttu-id="47d01-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="47d01-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d01-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47d01-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a><span data-ttu-id="47d01-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="47d01-111">Members</span></span>

<span data-ttu-id="47d01-112">La **clase \_ \_ AppManagement01 de MDM EnterpriseModernAppManagement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="47d01-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these types of members:</span></span>

-   [<span data-ttu-id="47d01-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="47d01-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="47d01-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47d01-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="47d01-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="47d01-115">Methods</span></span>

<span data-ttu-id="47d01-116">La **clase \_ \_ AppManagement01 de MDM EnterpriseModernAppManagement** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="47d01-116">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these methods.</span></span>



| <span data-ttu-id="47d01-117">Método</span><span class="sxs-lookup"><span data-stu-id="47d01-117">Method</span></span>                                                                                               | <span data-ttu-id="47d01-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="47d01-118">Description</span></span>                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="47d01-119">**RemovePackageMethod**</span><span class="sxs-lookup"><span data-stu-id="47d01-119">**RemovePackageMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | <span data-ttu-id="47d01-120">Método para quitar paquetes.</span><span class="sxs-lookup"><span data-stu-id="47d01-120">Method for removing packages.</span></span><br/>                |
| [<span data-ttu-id="47d01-121">**UpdateScanMethod**</span><span class="sxs-lookup"><span data-stu-id="47d01-121">**UpdateScanMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | <span data-ttu-id="47d01-122">Método para iniciar el examen de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="47d01-122">Method for starting the Windows Update scan.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="47d01-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47d01-123">Properties</span></span>

<span data-ttu-id="47d01-124">La **clase \_ \_ AppManagement01 de MDM EnterpriseModernAppManagement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47d01-124">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="47d01-125">AppInventoryQuery</span><span class="sxs-lookup"><span data-stu-id="47d01-125">AppInventoryQuery</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47d01-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47d01-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47d01-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47d01-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47d01-128">AppInventoryResults</span><span class="sxs-lookup"><span data-stu-id="47d01-128">AppInventoryResults</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47d01-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47d01-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47d01-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47d01-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47d01-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="47d01-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47d01-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47d01-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47d01-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47d01-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47d01-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47d01-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47d01-135">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="47d01-135">Identifies the name of the parent node.</span></span> <span data-ttu-id="47d01-136">Para esta clase, la cadena es "AppManagement".</span><span class="sxs-lookup"><span data-stu-id="47d01-136">For this class, the string is "AppManagement".</span></span>

</dd> <dt>

[<span data-ttu-id="47d01-137">LastScanError</span><span class="sxs-lookup"><span data-stu-id="47d01-137">LastScanError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47d01-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="47d01-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="47d01-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47d01-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47d01-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="47d01-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47d01-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47d01-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47d01-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47d01-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47d01-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47d01-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47d01-144">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="47d01-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="47d01-145">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/".</span><span class="sxs-lookup"><span data-stu-id="47d01-145">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/"</span></span>

</dd> <dt>

[<span data-ttu-id="47d01-146">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="47d01-146">RemovePackage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47d01-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47d01-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47d01-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47d01-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47d01-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47d01-149">Requirements</span></span>



| <span data-ttu-id="47d01-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d01-150">Requirement</span></span> | <span data-ttu-id="47d01-151">Value</span><span class="sxs-lookup"><span data-stu-id="47d01-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d01-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47d01-152">Minimum supported client</span></span><br/> | <span data-ttu-id="47d01-153">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="47d01-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47d01-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47d01-154">Minimum supported server</span></span><br/> | <span data-ttu-id="47d01-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="47d01-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="47d01-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47d01-156">Namespace</span></span><br/>                | <span data-ttu-id="47d01-157">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="47d01-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="47d01-158">MOF</span><span class="sxs-lookup"><span data-stu-id="47d01-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47d01-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47d01-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="47d01-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47d01-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47d01-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47d01-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d01-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="47d01-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d01-163">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="47d01-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

