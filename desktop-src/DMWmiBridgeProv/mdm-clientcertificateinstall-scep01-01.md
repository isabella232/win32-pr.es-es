---
title: MDM_ClientCertificateInstall_SCEP01_01 (clase)
description: La \_ clase ClientCertificateInstall \_ SCEP01 \_ 01 de MDM permite el acceso al nodo para la instalación de certificados SCEP, mediante el uso de identificadores únicos para diferenciar las diferentes solicitudes de instalación de certificados.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- MDM_ClientCertificateInstall_SCEP01_01 (clase)
- MDM_ClientCertificateInstall_SCEP01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905445"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="ffed4-105">\_Clase ClientCertificateInstall \_ SCEP01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="ffed4-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="ffed4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ffed4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ffed4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ffed4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ffed4-108">La **clase \_ ClientCertificateInstall \_ SCEP01 \_ 01 de MDM** permite el acceso al nodo para la instalación de certificados SCEP, mediante el uso de identificadores únicos para diferenciar las diferentes solicitudes de instalación de certificados.</span><span class="sxs-lookup"><span data-stu-id="ffed4-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="ffed4-109">Necesario para la instalación del certificado SCEP.</span><span class="sxs-lookup"><span data-stu-id="ffed4-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="ffed4-110">Las operaciones admitidas son get, Add y DELETE.</span><span class="sxs-lookup"><span data-stu-id="ffed4-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="ffed4-111">La llamada a delete en este nodo debe eliminar el certificado SCEP correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ffed4-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="ffed4-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ffed4-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffed4-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffed4-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="ffed4-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="ffed4-114">Members</span></span>

<span data-ttu-id="ffed4-115">La **clase \_ ClientCertificateInstall \_ SCEP01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ffed4-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="ffed4-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffed4-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffed4-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffed4-117">Properties</span></span>

<span data-ttu-id="ffed4-118">La **clase \_ ClientCertificateInstall \_ SCEP01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ffed4-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ffed4-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="ffed4-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ffed4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffed4-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffed4-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="ffed4-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed4-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ffed4-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffed4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ffed4-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ffed4-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed4-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ffed4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ffed4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ffed4-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ffed4-129">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ffed4-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="ffed4-130">Para esta clase, un identificador único para diferenciar las distintas solicitudes de instalación de certificados.</span><span class="sxs-lookup"><span data-stu-id="ffed4-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="ffed4-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ffed4-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed4-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ffed4-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ffed4-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ffed4-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ffed4-135">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="ffed4-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="ffed4-136">La cadena es "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span><span class="sxs-lookup"><span data-stu-id="ffed4-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="ffed4-137">RespondentServerUrl</span><span class="sxs-lookup"><span data-stu-id="ffed4-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed4-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ffed4-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffed4-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ffed4-140">Estado</span><span class="sxs-lookup"><span data-stu-id="ffed4-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffed4-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ffed4-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ffed4-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ffed4-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffed4-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffed4-143">Requirements</span></span>



| <span data-ttu-id="ffed4-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffed4-144">Requirement</span></span> | <span data-ttu-id="ffed4-145">Value</span><span class="sxs-lookup"><span data-stu-id="ffed4-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffed4-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffed4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ffed4-147">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffed4-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffed4-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffed4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ffed4-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ffed4-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ffed4-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ffed4-150">Namespace</span></span><br/>                | <span data-ttu-id="ffed4-151">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ffed4-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ffed4-152">MOF</span><span class="sxs-lookup"><span data-stu-id="ffed4-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffed4-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffed4-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffed4-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffed4-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffed4-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffed4-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffed4-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffed4-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffed4-157">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="ffed4-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

