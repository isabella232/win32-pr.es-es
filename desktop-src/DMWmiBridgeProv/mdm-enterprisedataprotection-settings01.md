---
title: MDM_EnterpriseDataProtection_Settings01 (clase)
description: La \_ clase Settings01 de EnterpriseDataProtection de MDM \_ se usa para configurar las opciones específicas de Windows Information Protection (WIP) (anteriormente conocido como protección de datos empresariales).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- MDM_EnterpriseDataProtection_Settings01 (clase)
- MDM_EnterpriseDataProtection_Settings01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491957"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="f22b5-105">\_Clase Settings01 EnterpriseDataProtection de MDM \_</span><span class="sxs-lookup"><span data-stu-id="f22b5-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="f22b5-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f22b5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f22b5-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f22b5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f22b5-108">La **clase \_ \_ Settings01 de EnterpriseDataProtection de MDM** se usa para configurar las opciones específicas de Windows Information Protection (WIP) (anteriormente conocido como protección de datos empresariales).</span><span class="sxs-lookup"><span data-stu-id="f22b5-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="f22b5-109">Para obtener más información sobre WIP, consulte protección [de los datos de la empresa mediante la protección de datos empresariales (este)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="f22b5-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="f22b5-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f22b5-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f22b5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f22b5-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="f22b5-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="f22b5-112">Members</span></span>

<span data-ttu-id="f22b5-113">La **clase \_ \_ Settings01 de MDM EnterpriseDataProtection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f22b5-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="f22b5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f22b5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f22b5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f22b5-115">Properties</span></span>

<span data-ttu-id="f22b5-116">La **clase \_ \_ Settings01 de MDM EnterpriseDataProtection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f22b5-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f22b5-117">AllowAzureRMSForEDP</span><span class="sxs-lookup"><span data-stu-id="f22b5-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f22b5-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-120">AllowUserDecryption</span><span class="sxs-lookup"><span data-stu-id="f22b5-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f22b5-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-123">DataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="f22b5-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f22b5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-126">Calificadores: **Octetstring**</span><span class="sxs-lookup"><span data-stu-id="f22b5-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-127">EDPEnforcementLevel</span><span class="sxs-lookup"><span data-stu-id="f22b5-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f22b5-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-130">EDPShowIcons</span><span class="sxs-lookup"><span data-stu-id="f22b5-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f22b5-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-133">EnterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="f22b5-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f22b5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f22b5-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f22b5-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f22b5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22b5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-139">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f22b5-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f22b5-140">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f22b5-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="f22b5-141">Para esta clase, la cadena es "Settings".</span><span class="sxs-lookup"><span data-stu-id="f22b5-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="f22b5-142">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f22b5-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f22b5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f22b5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f22b5-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f22b5-146">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="f22b5-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="f22b5-147">Para esta clase, la cadena es "./Vendor/MSFT/EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="f22b5-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="f22b5-148">RevokeOnUnenroll</span><span class="sxs-lookup"><span data-stu-id="f22b5-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-149">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f22b5-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-151">RMSTemplateIDForEDP</span><span class="sxs-lookup"><span data-stu-id="f22b5-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f22b5-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f22b5-154">SMBAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="f22b5-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f22b5-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f22b5-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f22b5-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f22b5-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f22b5-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f22b5-157">Requirements</span></span>



| <span data-ttu-id="f22b5-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="f22b5-158">Requirement</span></span> | <span data-ttu-id="f22b5-159">Value</span><span class="sxs-lookup"><span data-stu-id="f22b5-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f22b5-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f22b5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f22b5-161">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f22b5-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f22b5-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f22b5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f22b5-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f22b5-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f22b5-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f22b5-164">Namespace</span></span><br/>                | <span data-ttu-id="f22b5-165">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f22b5-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f22b5-166">MOF</span><span class="sxs-lookup"><span data-stu-id="f22b5-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f22b5-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f22b5-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="f22b5-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f22b5-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f22b5-169"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="f22b5-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

