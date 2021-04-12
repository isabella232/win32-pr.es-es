---
title: MDM_VPNv2_CryptographySuite03 (clase)
description: La \_ \_ clase CryptographySuite03 de VPNV2 de MDM contiene información de criptografía para el perfil de VPN nativo.
ms.assetid: d8d16d43-bd54-4ca8-a850-ce48390df7d6
keywords:
- MDM_VPNv2_CryptographySuite03 (clase)
- MDM_VPNv2_CryptographySuite03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_CryptographySuite03
- MDM_VPNv2_CryptographySuite03.InstanceID
- MDM_VPNv2_CryptographySuite03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553f2dcddd4d7c7e0926945a80f74f6aba2a9467
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490661"
---
# <a name="mdm_vpnv2_cryptographysuite03-class"></a><span data-ttu-id="49193-105">\_Clase CryptographySuite03 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="49193-105">MDM\_VPNv2\_CryptographySuite03 class</span></span>

<span data-ttu-id="49193-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="49193-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="49193-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="49193-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="49193-108">La **clase \_ \_ CryptographySuite03 de VPNv2 de MDM** contiene información de criptografía para el perfil de VPN nativo.</span><span class="sxs-lookup"><span data-stu-id="49193-108">The **MDM\_VPNv2\_CryptographySuite03** class contains cryptography information for the native VPN profile.</span></span>

<span data-ttu-id="49193-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="49193-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="49193-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49193-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_CryptographySuite03
{
  string InstanceID;
  string ParentID;
  string AuthenticationTransformConstants;
  string CipherTransformConstants;
  string EncryptionMethod;
  string IntegrityCheckMethod;
  string DHGroup;
  string PfsGroup;
};
```

## <a name="members"></a><span data-ttu-id="49193-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="49193-111">Members</span></span>

<span data-ttu-id="49193-112">La **clase \_ \_ CryptographySuite03 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="49193-112">The **MDM\_VPNv2\_CryptographySuite03** class has these types of members:</span></span>

-   [<span data-ttu-id="49193-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49193-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49193-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49193-114">Properties</span></span>

<span data-ttu-id="49193-115">La **clase \_ \_ CryptographySuite03 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="49193-115">The **MDM\_VPNv2\_CryptographySuite03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="49193-116">AuthenticationTransformConstants</span><span class="sxs-lookup"><span data-stu-id="49193-116">AuthenticationTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-authenticationtransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49193-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49193-119">CipherTransformConstants</span><span class="sxs-lookup"><span data-stu-id="49193-119">CipherTransformConstants</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-ciphertransformconstants)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49193-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49193-122">Grupo DH</span><span class="sxs-lookup"><span data-stu-id="49193-122">DHGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-dhgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49193-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="49193-125">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="49193-125">EncryptionMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49193-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="49193-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="49193-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49193-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49193-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="49193-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="49193-132">Nodo que contiene las propiedades de los túneles IPSec.</span><span class="sxs-lookup"><span data-stu-id="49193-132">Node containing the properties of IPSec tunnels.</span></span>

</dd> <dt>

[<span data-ttu-id="49193-133">IntegrityCheckMethod</span><span class="sxs-lookup"><span data-stu-id="49193-133">IntegrityCheckMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-integritycheckmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49193-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="49193-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="49193-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49193-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49193-139">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="49193-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="49193-140">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="49193-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="49193-141">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="49193-141">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="49193-142">PfsGroup</span><span class="sxs-lookup"><span data-stu-id="49193-142">PfsGroup</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-cryptographysuite-pfsgroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="49193-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49193-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49193-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="49193-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49193-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49193-145">Requirements</span></span>



| <span data-ttu-id="49193-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="49193-146">Requirement</span></span> | <span data-ttu-id="49193-147">Value</span><span class="sxs-lookup"><span data-stu-id="49193-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49193-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49193-148">Minimum supported client</span></span><br/> | <span data-ttu-id="49193-149">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="49193-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49193-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49193-150">Minimum supported server</span></span><br/> | <span data-ttu-id="49193-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49193-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="49193-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="49193-152">Namespace</span></span><br/>                | <span data-ttu-id="49193-153">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="49193-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="49193-154">MOF</span><span class="sxs-lookup"><span data-stu-id="49193-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49193-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49193-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="49193-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49193-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49193-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49193-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

