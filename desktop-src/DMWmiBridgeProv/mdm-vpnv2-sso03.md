---
title: MDM_VPNv2_Sso03 (clase)
description: La \_ clase Sso03 de MDM VPNv2 \_ se puede usar para seleccionar un certificado diferente al certificado de autenticación de VPN para la autenticación Kerberos en el caso de cumplimiento de dispositivos.
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- MDM_VPNv2_Sso03 (clase)
- MDM_VPNv2_Sso03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996784"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="aeebc-105">\_Clase Sso03 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="aeebc-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="aeebc-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="aeebc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aeebc-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="aeebc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aeebc-108">La **clase \_ \_ Sso03 de MDM VPNv2** se puede usar para seleccionar un certificado diferente al certificado de autenticación de VPN para la autenticación Kerberos en el caso de cumplimiento de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aeebc-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="aeebc-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aeebc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeebc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aeebc-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="aeebc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="aeebc-111">Members</span></span>

<span data-ttu-id="aeebc-112">La **clase \_ \_ Sso03 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aeebc-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="aeebc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeebc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aeebc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeebc-114">Properties</span></span>

<span data-ttu-id="aeebc-115">La **clase \_ \_ Sso03 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aeebc-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="aeebc-116">EKU</span><span class="sxs-lookup"><span data-stu-id="aeebc-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeebc-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeebc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="aeebc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aeebc-119">Enabled</span><span class="sxs-lookup"><span data-stu-id="aeebc-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeebc-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aeebc-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="aeebc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aeebc-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aeebc-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeebc-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeebc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeebc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aeebc-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aeebc-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="aeebc-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="aeebc-127">IssuerHash</span><span class="sxs-lookup"><span data-stu-id="aeebc-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeebc-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeebc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="aeebc-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aeebc-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="aeebc-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aeebc-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aeebc-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aeebc-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aeebc-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aeebc-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aeebc-134">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="aeebc-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="aeebc-135">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span><span class="sxs-lookup"><span data-stu-id="aeebc-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aeebc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeebc-136">Requirements</span></span>



| <span data-ttu-id="aeebc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeebc-137">Requirement</span></span> | <span data-ttu-id="aeebc-138">Value</span><span class="sxs-lookup"><span data-stu-id="aeebc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeebc-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeebc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="aeebc-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="aeebc-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aeebc-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aeebc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="aeebc-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aeebc-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aeebc-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aeebc-143">Namespace</span></span><br/>                | <span data-ttu-id="aeebc-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="aeebc-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aeebc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="aeebc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aeebc-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aeebc-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aeebc-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aeebc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeebc-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeebc-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeebc-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeebc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeebc-150">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="aeebc-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

