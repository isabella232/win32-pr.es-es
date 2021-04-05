---
title: MDM_VPNv2_DomainNameInformationList02_01 (clase)
description: La \_ clase VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM describe las reglas de la tabla de directivas de resolución de nombres (NRPT) para el perfil de VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- MDM_VPNv2_DomainNameInformationList02_01 (clase)
- MDM_VPNv2_DomainNameInformationList02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996956"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="48a4c-105">\_Clase VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="48a4c-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="48a4c-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="48a4c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="48a4c-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="48a4c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="48a4c-108">La **clase \_ VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM** describe las reglas de la tabla de directivas de resolución de nombres (NRPT) para el perfil de VPN.</span><span class="sxs-lookup"><span data-stu-id="48a4c-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="48a4c-109">La tabla de directivas de resolución de nombres (NRPT) es una tabla de espacios de nombres y la configuración correspondiente almacenada en el registro de Windows que determina el comportamiento del cliente DNS cuando se emiten consultas y procesan respuestas.</span><span class="sxs-lookup"><span data-stu-id="48a4c-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="48a4c-110">Cada fila de la tabla NRPT representa una regla para una parte del espacio de nombres para la que el cliente DNS emite consultas.</span><span class="sxs-lookup"><span data-stu-id="48a4c-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="48a4c-111">Antes de emitir consultas de resolución de nombres, el cliente DNS consulta la NRPT para determinar si se debe establecer alguna marca adicional en la consulta.</span><span class="sxs-lookup"><span data-stu-id="48a4c-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="48a4c-112">Después de recibir la respuesta, el cliente consulta de nuevo la tabla NRPT para comprobar si hay algún requisito de procesamiento o Directiva especial.</span><span class="sxs-lookup"><span data-stu-id="48a4c-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="48a4c-113">En ausencia de la NRPT, el cliente opera en función de los servidores DNS y los sufijos establecidos en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="48a4c-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="48a4c-114">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="48a4c-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a4c-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48a4c-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="48a4c-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="48a4c-116">Members</span></span>

<span data-ttu-id="48a4c-117">La **clase \_ VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48a4c-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="48a4c-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48a4c-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48a4c-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48a4c-119">Properties</span></span>

<span data-ttu-id="48a4c-120">La **clase \_ VPNv2 \_ DomainNameInformationList02 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="48a4c-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="48a4c-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="48a4c-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a4c-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48a4c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48a4c-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="48a4c-124">DomainName</span><span class="sxs-lookup"><span data-stu-id="48a4c-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a4c-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48a4c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48a4c-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="48a4c-127">DomainNameType</span><span class="sxs-lookup"><span data-stu-id="48a4c-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a4c-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48a4c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48a4c-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="48a4c-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="48a4c-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a4c-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48a4c-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48a4c-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48a4c-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48a4c-134">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="48a4c-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="48a4c-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="48a4c-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a4c-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48a4c-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48a4c-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-138">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48a4c-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48a4c-139">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="48a4c-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="48a4c-140">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="48a4c-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="48a4c-141">WebProxyServers</span><span class="sxs-lookup"><span data-stu-id="48a4c-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a4c-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48a4c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48a4c-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48a4c-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48a4c-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48a4c-144">Requirements</span></span>



| <span data-ttu-id="48a4c-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a4c-145">Requirement</span></span> | <span data-ttu-id="48a4c-146">Value</span><span class="sxs-lookup"><span data-stu-id="48a4c-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a4c-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a4c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="48a4c-148">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="48a4c-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48a4c-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48a4c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="48a4c-150">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="48a4c-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="48a4c-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48a4c-151">Namespace</span></span><br/>                | <span data-ttu-id="48a4c-152">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="48a4c-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="48a4c-153">MOF</span><span class="sxs-lookup"><span data-stu-id="48a4c-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48a4c-154"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48a4c-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="48a4c-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48a4c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a4c-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a4c-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a4c-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="48a4c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a4c-158">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="48a4c-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

