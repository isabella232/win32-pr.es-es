---
title: Win32_RDCentralPublishedDeploymentSettings (clase)
description: Contiene la configuración de implementación usada para generar archivos RDP para los recursos publicados en una granja.
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedDeploymentSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDCentralPublishedDeploymentSettings de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422565"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="40d79-105">\_Clase Win32 RDCentralPublishedDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="40d79-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="40d79-106">Contiene la configuración de implementación usada para generar archivos RDP para los recursos publicados en una granja.</span><span class="sxs-lookup"><span data-stu-id="40d79-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="40d79-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="40d79-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d79-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40d79-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="40d79-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="40d79-109">Members</span></span>

<span data-ttu-id="40d79-110">La **clase \_ RDCentralPublishedDeploymentSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="40d79-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="40d79-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40d79-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40d79-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40d79-112">Properties</span></span>

<span data-ttu-id="40d79-113">La **clase \_ RDCentralPublishedDeploymentSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="40d79-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40d79-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="40d79-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-115">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="40d79-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-117">**true** para permitir el suavizado de fuentes; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="40d79-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="40d79-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40d79-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d79-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="40d79-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="40d79-122">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="40d79-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="40d79-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40d79-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d79-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="40d79-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-125">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="40d79-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="40d79-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-127">Certificado usado para firmar los archivos RDP; necesariamente solo si *HasCertificate* es true.</span><span class="sxs-lookup"><span data-stu-id="40d79-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-128">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="40d79-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="40d79-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-131">Contiene la profundidad de bits de color:</span><span class="sxs-lookup"><span data-stu-id="40d79-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="40d79-132">**4** ()</span><span class="sxs-lookup"><span data-stu-id="40d79-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="40d79-133">**8** ()</span><span class="sxs-lookup"><span data-stu-id="40d79-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="40d79-134">**15** ()</span><span class="sxs-lookup"><span data-stu-id="40d79-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="40d79-135">**16** ()</span><span class="sxs-lookup"><span data-stu-id="40d79-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="40d79-136">**24** ()</span><span class="sxs-lookup"><span data-stu-id="40d79-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="40d79-137">**32** ()</span><span class="sxs-lookup"><span data-stu-id="40d79-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40d79-138">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="40d79-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-141">Incluye el contenido del archivo RDP correspondiente a la configuración personalizada de RDP.</span><span class="sxs-lookup"><span data-stu-id="40d79-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-142">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="40d79-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-145">Incluye el contenido del archivo RDP correspondiente a la configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="40d79-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="40d79-146">Si se establece este parámetro, el sistema usará este archivo RDP y pasará por alto la configuración de RDP en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="40d79-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40d79-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40d79-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d79-150">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="40d79-150">Description of the object.</span></span>

<span data-ttu-id="40d79-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40d79-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d79-152">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="40d79-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-155">Nombre de la granja.</span><span class="sxs-lookup"><span data-stu-id="40d79-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-156">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="40d79-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-157">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="40d79-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-159">Contiene el modo de autenticación de puerta de enlace:</span><span class="sxs-lookup"><span data-stu-id="40d79-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="40d79-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Contraseña (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="40d79-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="40d79-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Tarjeta inteligente (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="40d79-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="40d79-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Permitir al usuario elegir (4)** (4)</span><span class="sxs-lookup"><span data-stu-id="40d79-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40d79-163">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="40d79-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-166">El nombre de la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="40d79-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-167">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="40d79-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="40d79-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-170">Describe cómo se usa la puerta de enlace:</span><span class="sxs-lookup"><span data-stu-id="40d79-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="40d79-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**Nogateway** (0)</span><span class="sxs-lookup"><span data-stu-id="40d79-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="40d79-172">Ninguna puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="40d79-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="40d79-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span><span class="sxs-lookup"><span data-stu-id="40d79-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="40d79-174">Usar la puerta de enlace pass by local.</span><span class="sxs-lookup"><span data-stu-id="40d79-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="40d79-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span><span class="sxs-lookup"><span data-stu-id="40d79-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="40d79-176">Use la puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="40d79-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="40d79-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span><span class="sxs-lookup"><span data-stu-id="40d79-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="40d79-178">Detección de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="40d79-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40d79-179">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="40d79-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="40d79-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-182">**true** para utilizar las mismas credenciales de usuario para la puerta de enlace de TS y el servidor de TS siempre que sea posible; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="40d79-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-183">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="40d79-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="40d79-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-186">**true** para usar un certificado para firmar los archivos RDP; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="40d79-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40d79-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-188">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="40d79-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40d79-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d79-190">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="40d79-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="40d79-191">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="40d79-191">The date the object was installed.</span></span> <span data-ttu-id="40d79-192">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="40d79-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="40d79-193">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40d79-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d79-194">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="40d79-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40d79-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40d79-197">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="40d79-197">The name of the object.</span></span>

<span data-ttu-id="40d79-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40d79-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40d79-199">**Puerto**</span><span class="sxs-lookup"><span data-stu-id="40d79-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-200">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="40d79-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-201">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-202">El puerto RDP.</span><span class="sxs-lookup"><span data-stu-id="40d79-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-203">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="40d79-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="40d79-206">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40d79-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40d79-207">El alias de la granja que publicó la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40d79-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="40d79-208">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="40d79-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-209">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="40d79-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-210">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-211">Opciones de redireccionamiento:</span><span class="sxs-lookup"><span data-stu-id="40d79-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="40d79-212">0</span><span class="sxs-lookup"><span data-stu-id="40d79-212">0</span></span>
</dt> <dd>

<span data-ttu-id="40d79-213">None</span><span class="sxs-lookup"><span data-stu-id="40d79-213">None</span></span>

</dd> <dt>

<span data-ttu-id="40d79-214">1</span><span class="sxs-lookup"><span data-stu-id="40d79-214">1</span></span>
</dt> <dd>

<span data-ttu-id="40d79-215">Unidades</span><span class="sxs-lookup"><span data-stu-id="40d79-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="40d79-216">2</span><span class="sxs-lookup"><span data-stu-id="40d79-216">2</span></span>
</dt> <dd>

<span data-ttu-id="40d79-217">Impresoras</span><span class="sxs-lookup"><span data-stu-id="40d79-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="40d79-218">4</span><span class="sxs-lookup"><span data-stu-id="40d79-218">4</span></span>
</dt> <dd>

<span data-ttu-id="40d79-219">Portapapeles</span><span class="sxs-lookup"><span data-stu-id="40d79-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="40d79-220">8</span><span class="sxs-lookup"><span data-stu-id="40d79-220">8</span></span>
</dt> <dd>

<span data-ttu-id="40d79-221">Plug and Play</span><span class="sxs-lookup"><span data-stu-id="40d79-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="40d79-222">16</span><span class="sxs-lookup"><span data-stu-id="40d79-222">16</span></span>
</dt> <dd>

<span data-ttu-id="40d79-223">Tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="40d79-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40d79-224">**Estado**</span><span class="sxs-lookup"><span data-stu-id="40d79-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="40d79-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="40d79-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40d79-227">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="40d79-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="40d79-228">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="40d79-228">Current status of the object.</span></span> <span data-ttu-id="40d79-229">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="40d79-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="40d79-230">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="40d79-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="40d79-231">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="40d79-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="40d79-232">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="40d79-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="40d79-233">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="40d79-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="40d79-234">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40d79-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="40d79-235">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="40d79-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-236">("Error")</span><span class="sxs-lookup"><span data-stu-id="40d79-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-237">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="40d79-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-238">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="40d79-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-239">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="40d79-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-240">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="40d79-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-241">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="40d79-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="40d79-242">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="40d79-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40d79-243">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="40d79-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d79-244">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="40d79-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40d79-245">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="40d79-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40d79-246">**true** para habilitar varios monitores para escritorio (no raíl); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="40d79-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40d79-247">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40d79-247">Requirements</span></span>



| <span data-ttu-id="40d79-248">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d79-248">Requirement</span></span> | <span data-ttu-id="40d79-249">Value</span><span class="sxs-lookup"><span data-stu-id="40d79-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40d79-250">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40d79-250">Minimum supported client</span></span><br/> | <span data-ttu-id="40d79-251">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="40d79-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="40d79-252">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40d79-252">Minimum supported server</span></span><br/> | <span data-ttu-id="40d79-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="40d79-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="40d79-254">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40d79-254">Namespace</span></span><br/>                | <span data-ttu-id="40d79-255">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="40d79-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="40d79-256">MOF</span><span class="sxs-lookup"><span data-stu-id="40d79-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40d79-257"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40d79-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="40d79-258">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40d79-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d79-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d79-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

