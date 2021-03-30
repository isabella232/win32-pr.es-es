---
title: Win32_TSDeploymentSettings (clase)
description: Define la configuración predeterminada que utiliza el Administrador de RemoteApp al crear archivos de Protocolo de escritorio remoto (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSDeploymentSettings de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490283"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="6b9bc-105">\_Clase Win32 TSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="6b9bc-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="6b9bc-106">Define la configuración predeterminada que utiliza el Administrador de RemoteApp al crear archivos de Protocolo de escritorio remoto (RDP).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="6b9bc-107">Esta configuración no afecta a ninguna aplicación o escritorio publicado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b9bc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b9bc-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="6b9bc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b9bc-109">Members</span></span>

<span data-ttu-id="6b9bc-110">La **clase \_ TSDeploymentSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6b9bc-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="6b9bc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b9bc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b9bc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6b9bc-112">Properties</span></span>

<span data-ttu-id="6b9bc-113">La **clase \_ TSDeploymentSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b9bc-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-115">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-117">Indica si se permite el suavizado de fuentes.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6b9bc-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-122">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6b9bc-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-124">**CertificateExpiresOn**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-127">Fecha en la que expira el certificado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-127">The date that the certificate expires on.</span></span> <span data-ttu-id="6b9bc-128">Este valor se almacena como un formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-130">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="6b9bc-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-132">Huella digital del certificado que se usa para firmar los archivos RDP.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-133">**CertificateIssuedBy**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-136">Especifica a quién emite el certificado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-137">**CertificateIssuedTo**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-140">Especifica a quién se emite el certificado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-141">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-142">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-144">Profundidad de bits de color de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-144">The color bit depth of the display.</span></span> <span data-ttu-id="6b9bc-145">Los valores posibles son 4, 8, 15, 16, 24 y 32.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-146">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-149">El contenido del archivo RDP que se corresponde con la configuración personalizada de RDP en Administrador de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-150">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-153">El contenido del archivo RDP que corresponde a la configuración de implementación de Administrador de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="6b9bc-154">Si se establece este valor, la configuración de implementación de RDP sustituye a la configuración predeterminada de esta clase.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="6b9bc-155">Por ejemplo, si establece la propiedad **GatewayAuthMode** en esta clase y establece la propiedad **DeploymentRDPSettings** , se omitirá la propiedad **GatewayAuthMode** de esta clase y se usará el valor **GatewayAuthMode** de **DeploymentRDPSettings** .</span><span class="sxs-lookup"><span data-stu-id="6b9bc-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-159">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-159">Description of the object.</span></span>

<span data-ttu-id="6b9bc-160">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-161">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-164">El nombre del servidor host de sesión de escritorio remoto o el nombre de dominio completo (FQDN) de la granja de servidores host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-165">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-166">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-168">Método de autenticación de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="6b9bc-169">Los valores siguientes son posibles.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="6b9bc-170">0</span><span class="sxs-lookup"><span data-stu-id="6b9bc-170">0</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-171">Contraseña</span><span class="sxs-lookup"><span data-stu-id="6b9bc-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-172">1</span><span class="sxs-lookup"><span data-stu-id="6b9bc-172">1</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-173">Tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="6b9bc-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-174">4</span><span class="sxs-lookup"><span data-stu-id="6b9bc-174">4</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-175">Permitir al usuario seleccionar durante la conexión.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b9bc-176">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-179">Nombre del servidor de puerta de enlace de escritorio remoto que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-180">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-181">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-183">Indica si se debe usar un servidor de puerta de enlace de escritorio remoto para conectarse al servidor host de sesión de escritorio remoto de destino a través de un firewall.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="6b9bc-184">Los valores siguientes son posibles.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="6b9bc-185">0</span><span class="sxs-lookup"><span data-stu-id="6b9bc-185">0</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-186">No use un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-187">1</span><span class="sxs-lookup"><span data-stu-id="6b9bc-187">1</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-188">Usar un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-188">Use an RD Gateway server.</span></span> <span data-ttu-id="6b9bc-189">Omitir el servidor de puerta de enlace de escritorio remoto para direcciones locales.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-190">2</span><span class="sxs-lookup"><span data-stu-id="6b9bc-190">2</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-191">Usar un servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-192">3</span><span class="sxs-lookup"><span data-stu-id="6b9bc-192">3</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-193">Detectar automáticamente la configuración del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b9bc-194">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-195">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-196">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-197">Siempre que sea posible, use las mismas credenciales de usuario para el servidor de puerta de enlace de escritorio remoto y el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-198">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-199">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-200">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-201">Indica si se debe utilizar un certificado para firmar los archivos RDP.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-203">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-205">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-206">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-206">The date the object was installed.</span></span> <span data-ttu-id="6b9bc-207">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6b9bc-208">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-209">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-212">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-212">The name of the object.</span></span>

<span data-ttu-id="6b9bc-213">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-214">**Puerto**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-215">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-216">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-217">Puerto RDP que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-218">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-219">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-221">Especifica las opciones de redireccionamiento de dispositivos y recursos para las conexiones de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="6b9bc-222">Las marcas de **RedirectionOptions** se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="6b9bc-223">Los valores siguientes son posibles.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="6b9bc-224">0</span><span class="sxs-lookup"><span data-stu-id="6b9bc-224">0</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-225">Sin redireccionamiento de dispositivos o recursos.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-226">1</span><span class="sxs-lookup"><span data-stu-id="6b9bc-226">1</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-227">Redirigir unidades de disco.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-228">2</span><span class="sxs-lookup"><span data-stu-id="6b9bc-228">2</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-229">Redirigir impresoras.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-230">4</span><span class="sxs-lookup"><span data-stu-id="6b9bc-230">4</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-231">Redirigir el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-232">8</span><span class="sxs-lookup"><span data-stu-id="6b9bc-232">8</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-233">Redireccionamiento de dispositivos Plug and Play admitidos.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-234">16</span><span class="sxs-lookup"><span data-stu-id="6b9bc-234">16</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-235">Redirigir tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-236">32</span><span class="sxs-lookup"><span data-stu-id="6b9bc-236">32</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-237">Redirigir audio.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-238">64</span><span class="sxs-lookup"><span data-stu-id="6b9bc-238">64</span></span>
</dt> <dd>

<span data-ttu-id="6b9bc-239">Redirija los puertos serie.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6b9bc-240">**RequireServerAuth**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-241">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-242">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-243">Indica si se requiere la autenticación del servidor.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="6b9bc-244">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-247">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6b9bc-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-248">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-248">Current status of the object.</span></span> <span data-ttu-id="6b9bc-249">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6b9bc-250">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6b9bc-251">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="6b9bc-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6b9bc-252">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6b9bc-253">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6b9bc-254">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6b9bc-255">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-256">("Error")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-257">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-258">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-259">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-260">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-261">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6b9bc-262">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="6b9bc-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6b9bc-263">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b9bc-264">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6b9bc-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6b9bc-265">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6b9bc-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6b9bc-266">Indica si están habilitados varios monitores para el escritorio.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b9bc-267">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b9bc-267">Remarks</span></span>

<span data-ttu-id="6b9bc-268">Debe ser miembro del grupo administradores para establecer las propiedades utilizando esta clase.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="6b9bc-269">Si **RequireServerAuth** está establecido en **true**, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6b9bc-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="6b9bc-270">Si el programa RemoteApp es para uso de la intranet y todos los equipos cliente ejecutan Windows Server 2008 o Windows Vista, no es necesario configurar el servidor host de sesión de escritorio remoto para que use un certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="6b9bc-271">En este caso, se usa la Autenticación a nivel de red.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="6b9bc-272">Debe especificar el FQDN del servidor o la granja de servidores para el valor de la propiedad **FarmName** .</span><span class="sxs-lookup"><span data-stu-id="6b9bc-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="6b9bc-273">Para conectarse al espacio de nombres "CIMV2 \\ TerminalServices", el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="6b9bc-274">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="6b9bc-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="6b9bc-275">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="6b9bc-276">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="6b9bc-277">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6b9bc-278">Se instalan en el equipo cuando se agrega el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="6b9bc-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="6b9bc-279">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6b9bc-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9bc-280">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b9bc-280">Requirements</span></span>



| <span data-ttu-id="6b9bc-281">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b9bc-281">Requirement</span></span> | <span data-ttu-id="6b9bc-282">Value</span><span class="sxs-lookup"><span data-stu-id="6b9bc-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9bc-283">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b9bc-283">Minimum supported client</span></span><br/> | <span data-ttu-id="6b9bc-284">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6b9bc-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6b9bc-285">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b9bc-285">Minimum supported server</span></span><br/> | <span data-ttu-id="6b9bc-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b9bc-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b9bc-287">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b9bc-287">Namespace</span></span><br/>                | <span data-ttu-id="6b9bc-288">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6b9bc-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6b9bc-289">MOF</span><span class="sxs-lookup"><span data-stu-id="6b9bc-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b9bc-290"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b9bc-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="6b9bc-291">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b9bc-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b9bc-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b9bc-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

