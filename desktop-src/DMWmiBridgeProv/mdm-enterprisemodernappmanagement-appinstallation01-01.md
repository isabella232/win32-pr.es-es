---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM se usa para instalar aplicaciones de la tienda Windows o de una ubicación hospedada.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 (clase)
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996788"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="c85fa-105">\_Clase EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="c85fa-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="c85fa-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c85fa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c85fa-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c85fa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c85fa-108">La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** se usa para instalar aplicaciones de la tienda Windows o de una ubicación hospedada.</span><span class="sxs-lookup"><span data-stu-id="c85fa-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="c85fa-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c85fa-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c85fa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c85fa-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="c85fa-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c85fa-111">Members</span></span>

<span data-ttu-id="c85fa-112">La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c85fa-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="c85fa-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c85fa-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="c85fa-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c85fa-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c85fa-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c85fa-115">Methods</span></span>

<span data-ttu-id="c85fa-116">La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c85fa-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="c85fa-117">Método</span><span class="sxs-lookup"><span data-stu-id="c85fa-117">Method</span></span>                                                                                                    | <span data-ttu-id="c85fa-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c85fa-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c85fa-119">**HostedInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="c85fa-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="c85fa-120">Método para realizar una instalación de un paquete de la aplicación desde una ubicación hospedada (puede ser una unidad local, un origen de datos UNC o https).</span><span class="sxs-lookup"><span data-stu-id="c85fa-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="c85fa-121">**StoreInstallMethod**</span><span class="sxs-lookup"><span data-stu-id="c85fa-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="c85fa-122">Método para realizar una instalación de una aplicación y una licencia de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="c85fa-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="c85fa-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c85fa-123">Properties</span></span>

<span data-ttu-id="c85fa-124">La **clase \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c85fa-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c85fa-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c85fa-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85fa-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c85fa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c85fa-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c85fa-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c85fa-129">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c85fa-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="c85fa-130">Para esta clase, la cadena es "AppInstallation".</span><span class="sxs-lookup"><span data-stu-id="c85fa-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="c85fa-131">LastError</span><span class="sxs-lookup"><span data-stu-id="c85fa-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85fa-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c85fa-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c85fa-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c85fa-134">LastErrorDesc</span><span class="sxs-lookup"><span data-stu-id="c85fa-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85fa-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c85fa-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c85fa-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c85fa-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c85fa-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85fa-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c85fa-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c85fa-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c85fa-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c85fa-141">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="c85fa-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="c85fa-142">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation".</span><span class="sxs-lookup"><span data-stu-id="c85fa-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="c85fa-143">ProgressStatus</span><span class="sxs-lookup"><span data-stu-id="c85fa-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85fa-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c85fa-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c85fa-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c85fa-146">Estado</span><span class="sxs-lookup"><span data-stu-id="c85fa-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c85fa-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c85fa-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c85fa-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c85fa-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c85fa-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c85fa-149">Requirements</span></span>



| <span data-ttu-id="c85fa-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="c85fa-150">Requirement</span></span> | <span data-ttu-id="c85fa-151">Value</span><span class="sxs-lookup"><span data-stu-id="c85fa-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85fa-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c85fa-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c85fa-153">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c85fa-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c85fa-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c85fa-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c85fa-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c85fa-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c85fa-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c85fa-156">Namespace</span></span><br/>                | <span data-ttu-id="c85fa-157">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="c85fa-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c85fa-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c85fa-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c85fa-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c85fa-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c85fa-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c85fa-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c85fa-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c85fa-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c85fa-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="c85fa-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c85fa-163">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="c85fa-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

