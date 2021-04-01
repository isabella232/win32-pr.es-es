---
title: MDM_ClientCertificateInstall_PFXCertInstall01_01 (clase)
description: La \_ clase ClientCertificateInstall \_ PFXCertInstall01 \_ 01 de MDM permite a la empresa usar identificadores únicos para diferenciar las distintas solicitudes de instalación de certificados.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- MDM_ClientCertificateInstall_PFXCertInstall01_01 (clase)
- MDM_ClientCertificateInstall_PFXCertInstall01_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150731"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="1df50-105">\_Clase ClientCertificateInstall \_ PFXCertInstall01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="1df50-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="1df50-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1df50-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1df50-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1df50-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1df50-108">La **clase \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01 de MDM** permite a la empresa usar identificadores únicos para diferenciar las distintas solicitudes de instalación de certificados.</span><span class="sxs-lookup"><span data-stu-id="1df50-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="1df50-109">Necesario para la instalación del certificado PFX.</span><span class="sxs-lookup"><span data-stu-id="1df50-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="1df50-110">Al llamar a delete en este nodo, se deben eliminar los certificados y las claves instaladas por el BLOB PFX correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1df50-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="1df50-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1df50-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df50-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1df50-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="1df50-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="1df50-113">Members</span></span>

<span data-ttu-id="1df50-114">La **clase \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1df50-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="1df50-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1df50-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1df50-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1df50-116">Properties</span></span>

<span data-ttu-id="1df50-117">La **clase \_ ClientCertificateInstall \_ PFXCertInstall01 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1df50-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1df50-118">ContainerName</span><span class="sxs-lookup"><span data-stu-id="1df50-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1df50-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1df50-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1df50-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1df50-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1df50-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1df50-125">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1df50-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="1df50-126">Para esta clase, un identificador único para diferenciar las distintas solicitudes de instalación de certificados.</span><span class="sxs-lookup"><span data-stu-id="1df50-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="1df50-127">KeyLocation</span><span class="sxs-lookup"><span data-stu-id="1df50-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1df50-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1df50-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1df50-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1df50-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1df50-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1df50-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1df50-134">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1df50-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="1df50-135">La cadena es "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span><span class="sxs-lookup"><span data-stu-id="1df50-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="1df50-136">PFXCertBlob</span><span class="sxs-lookup"><span data-stu-id="1df50-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1df50-139">Calificadores: **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="1df50-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1df50-140">PFXCertPassword</span><span class="sxs-lookup"><span data-stu-id="1df50-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1df50-143">PFXCertPasswordEncryptionStore</span><span class="sxs-lookup"><span data-stu-id="1df50-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1df50-146">PFXCertPasswordEncryptionType</span><span class="sxs-lookup"><span data-stu-id="1df50-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1df50-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1df50-149">PFXKeyExportable</span><span class="sxs-lookup"><span data-stu-id="1df50-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-150">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1df50-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1df50-152">Estado</span><span class="sxs-lookup"><span data-stu-id="1df50-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1df50-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1df50-155">Huella digital</span><span class="sxs-lookup"><span data-stu-id="1df50-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1df50-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1df50-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1df50-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1df50-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1df50-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1df50-158">Requirements</span></span>



| <span data-ttu-id="1df50-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="1df50-159">Requirement</span></span> | <span data-ttu-id="1df50-160">Value</span><span class="sxs-lookup"><span data-stu-id="1df50-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df50-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1df50-161">Minimum supported client</span></span><br/> | <span data-ttu-id="1df50-162">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1df50-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1df50-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1df50-163">Minimum supported server</span></span><br/> | <span data-ttu-id="1df50-164">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1df50-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1df50-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1df50-165">Namespace</span></span><br/>                | <span data-ttu-id="1df50-166">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1df50-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1df50-167">MOF</span><span class="sxs-lookup"><span data-stu-id="1df50-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1df50-168"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1df50-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1df50-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1df50-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1df50-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df50-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df50-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="1df50-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df50-172">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="1df50-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

