---
title: MDM_EnterpriseModernAppManagement_AppManagement01_03 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM proporciona información específica sobre la aplicación, como el nombre, la versión y el publicador.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- MDM_EnterpriseModernAppManagement_AppManagement01_03 (clase)
- MDM_EnterpriseModernAppManagement_AppManagement01_03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150721"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="7629a-105">\_Clase EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM</span><span class="sxs-lookup"><span data-stu-id="7629a-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="7629a-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7629a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7629a-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7629a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7629a-108">La **clase \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03 de MDM** proporciona información específica sobre la aplicación, como el nombre, la versión y el publicador.</span><span class="sxs-lookup"><span data-stu-id="7629a-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="7629a-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7629a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7629a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7629a-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="7629a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7629a-111">Members</span></span>

<span data-ttu-id="7629a-112">La clase **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7629a-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="7629a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7629a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7629a-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7629a-114">Properties</span></span>

<span data-ttu-id="7629a-115">La clase **MDM \_ EnterpriseModernAppManagement \_ AppManagement01 \_ 03** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7629a-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7629a-116">Arquitectura</span><span class="sxs-lookup"><span data-stu-id="7629a-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="7629a-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-122">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="7629a-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7629a-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7629a-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7629a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7629a-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7629a-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7629a-129">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7629a-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="7629a-130">Para esta clase, la cadena es la instancia del nombre completo del paquete.</span><span class="sxs-lookup"><span data-stu-id="7629a-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="7629a-131">IsBundle</span><span class="sxs-lookup"><span data-stu-id="7629a-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7629a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-134">IsFramework</span><span class="sxs-lookup"><span data-stu-id="7629a-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7629a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-137">IsProvisioned</span><span class="sxs-lookup"><span data-stu-id="7629a-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7629a-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="7629a-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-143">PackageStatus</span><span class="sxs-lookup"><span data-stu-id="7629a-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7629a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7629a-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7629a-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7629a-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7629a-149">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7629a-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7629a-150">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7629a-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="7629a-151">Para esta clase, la cadena es "./Vendor/msft/EnterpriseModernAppManagement/AppManagement/*EnterpriseID* / *PackageFamilyName*"</span><span class="sxs-lookup"><span data-stu-id="7629a-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="7629a-152">Publicador</span><span class="sxs-lookup"><span data-stu-id="7629a-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-155">RequiresReinstall</span><span class="sxs-lookup"><span data-stu-id="7629a-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7629a-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="7629a-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-161">Usuarios</span><span class="sxs-lookup"><span data-stu-id="7629a-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7629a-164">Versión</span><span class="sxs-lookup"><span data-stu-id="7629a-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7629a-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7629a-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7629a-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7629a-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7629a-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7629a-167">Requirements</span></span>



| <span data-ttu-id="7629a-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="7629a-168">Requirement</span></span> | <span data-ttu-id="7629a-169">Value</span><span class="sxs-lookup"><span data-stu-id="7629a-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7629a-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7629a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7629a-171">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7629a-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7629a-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7629a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7629a-173">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7629a-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7629a-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7629a-174">Namespace</span></span><br/>                | <span data-ttu-id="7629a-175">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7629a-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7629a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="7629a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7629a-177"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7629a-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7629a-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7629a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7629a-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7629a-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7629a-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="7629a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7629a-181">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="7629a-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

