---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 (clase)
description: La \_ clase EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM se usa para administrar las licencias de las aplicaciones de la tienda.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 (clase)
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079595"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="2ba71-105">\_Clase EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="2ba71-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="2ba71-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2ba71-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2ba71-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2ba71-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2ba71-108">La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** se usa para administrar las licencias de las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="2ba71-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="2ba71-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2ba71-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba71-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ba71-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="2ba71-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ba71-111">Members</span></span>

<span data-ttu-id="2ba71-112">La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2ba71-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="2ba71-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ba71-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2ba71-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ba71-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2ba71-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="2ba71-115">Methods</span></span>

<span data-ttu-id="2ba71-116">La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2ba71-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="2ba71-117">Método</span><span class="sxs-lookup"><span data-stu-id="2ba71-117">Method</span></span>                                                                                                              | <span data-ttu-id="2ba71-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ba71-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="2ba71-119">**AddLicenseMethod**</span><span class="sxs-lookup"><span data-stu-id="2ba71-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="2ba71-120">Método para agregar una licencia.</span><span class="sxs-lookup"><span data-stu-id="2ba71-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="2ba71-121">**GetLicenseFromStoreMethod**</span><span class="sxs-lookup"><span data-stu-id="2ba71-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="2ba71-122">Método para obtener una licencia del almacén.</span><span class="sxs-lookup"><span data-stu-id="2ba71-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2ba71-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ba71-123">Properties</span></span>

<span data-ttu-id="2ba71-124">La **clase \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2ba71-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ba71-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2ba71-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ba71-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2ba71-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2ba71-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ba71-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ba71-129">Nodo opcional.</span><span class="sxs-lookup"><span data-stu-id="2ba71-129">Optional node.</span></span> <span data-ttu-id="2ba71-130">IDENTIFICADOR de licencia para una aplicación instalada en el almacén.</span><span class="sxs-lookup"><span data-stu-id="2ba71-130">License ID for a store installed app.</span></span> <span data-ttu-id="2ba71-131">El identificador de licencia es generalmente el PFN de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ba71-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="2ba71-132">Las operaciones admitidas son Add, get y DELETE.</span><span class="sxs-lookup"><span data-stu-id="2ba71-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="2ba71-133">LicenseCategory</span><span class="sxs-lookup"><span data-stu-id="2ba71-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ba71-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2ba71-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2ba71-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2ba71-136">LicenseUsage</span><span class="sxs-lookup"><span data-stu-id="2ba71-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ba71-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2ba71-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2ba71-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2ba71-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2ba71-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ba71-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2ba71-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2ba71-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-142">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2ba71-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2ba71-143">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="2ba71-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="2ba71-144">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses".</span><span class="sxs-lookup"><span data-stu-id="2ba71-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="2ba71-145">RequesterID</span><span class="sxs-lookup"><span data-stu-id="2ba71-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ba71-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2ba71-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2ba71-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2ba71-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ba71-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ba71-148">Requirements</span></span>



| <span data-ttu-id="2ba71-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ba71-149">Requirement</span></span> | <span data-ttu-id="2ba71-150">Value</span><span class="sxs-lookup"><span data-stu-id="2ba71-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba71-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ba71-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2ba71-152">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ba71-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ba71-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ba71-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2ba71-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2ba71-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2ba71-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2ba71-155">Namespace</span></span><br/>                | <span data-ttu-id="2ba71-156">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2ba71-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2ba71-157">MOF</span><span class="sxs-lookup"><span data-stu-id="2ba71-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ba71-158"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ba71-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ba71-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ba71-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ba71-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ba71-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba71-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ba71-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba71-162">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="2ba71-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

