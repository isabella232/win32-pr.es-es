---
title: Win32_TSGeneralSetting class (Clase Win32_TSGeneralSetting)
description: Representa la configuración general del terminal como el nivel de cifrado y el protocolo de transporte.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGeneralSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802480"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="9a96d-105">\_Clase Win32 TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="9a96d-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="9a96d-106">La clase WMI **\_ TSGeneralSetting de Win32** representa la configuración general del terminal como el nivel de cifrado y el protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="9a96d-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="9a96d-107">La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.</span><span class="sxs-lookup"><span data-stu-id="9a96d-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="9a96d-108">Para obtener información de referencia sobre los métodos, vea la tabla de métodos más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="9a96d-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a96d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a96d-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="9a96d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9a96d-110">Members</span></span>

<span data-ttu-id="9a96d-111">La **clase \_ TSGeneralSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9a96d-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="9a96d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a96d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9a96d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a96d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9a96d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="9a96d-114">Methods</span></span>

<span data-ttu-id="9a96d-115">La clase **Win32 \_ TSGeneralSetting** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9a96d-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="9a96d-116">Método</span><span class="sxs-lookup"><span data-stu-id="9a96d-116">Method</span></span>                                                                                        | <span data-ttu-id="9a96d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a96d-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a96d-118">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="9a96d-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="9a96d-119">Establece el nivel de cifrado.</span><span class="sxs-lookup"><span data-stu-id="9a96d-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9a96d-120">**SetSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="9a96d-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="9a96d-121">Establece el nivel de seguridad en uno de "nivel de seguridad RDP" (0), "Negotiate" (1) o "SSL" (2).</span><span class="sxs-lookup"><span data-stu-id="9a96d-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="9a96d-122">**SetUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="9a96d-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="9a96d-123">Habilita o deshabilita el requisito de que los usuarios se deben autenticar en el momento de la conexión estableciendo el valor de la propiedad **UserAuthenticationRequired** .</span><span class="sxs-lookup"><span data-stu-id="9a96d-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9a96d-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a96d-124">Properties</span></span>

<span data-ttu-id="9a96d-125">La **clase \_ TSGeneralSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9a96d-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a96d-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9a96d-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-129">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9a96d-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-130">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a96d-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="9a96d-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a96d-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="9a96d-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-135">Nombre para mostrar del nombre de sujeto del certificado personal del equipo local.</span><span class="sxs-lookup"><span data-stu-id="9a96d-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-136">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="9a96d-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-137">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="9a96d-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-139">Contiene un almacén de certificados serializado que contiene todos los certificados del almacén de **cuentas de usuario** del equipo que son certificados de servidor válidos para su uso con la capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="9a96d-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-140">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="9a96d-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9a96d-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-143">Nombre descriptivo de la combinación de nivel de sesión y Protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="9a96d-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9a96d-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-147">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a96d-147">Description of the object.</span></span>

<span data-ttu-id="9a96d-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a96d-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9a96d-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-150">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9a96d-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-152">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="9a96d-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-153">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="9a96d-153">The date the object was installed.</span></span> <span data-ttu-id="9a96d-154">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="9a96d-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9a96d-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a96d-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-156">**MinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="9a96d-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-159">Calificadores: **bajo** ("solo los datos enviados del cliente al servidor están protegidos por cifrado según el nivel de clave estándar del servidor.</span><span class="sxs-lookup"><span data-stu-id="9a96d-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="9a96d-160">Los datos enviados desde el servidor al cliente no están protegidos. "), **medio** (" todos los datos enviados entre el servidor y el cliente están protegidos por cifrado según el nivel de clave estándar del servidor. "), **alto** (" todos los datos enviados entre el servidor y el cliente están protegidos con el nivel máximo de clave del servidor basado en cifrado ").</span><span class="sxs-lookup"><span data-stu-id="9a96d-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-161">El nivel mínimo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="9a96d-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="9a96d-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-163">Bajo nivel de cifrado.</span><span class="sxs-lookup"><span data-stu-id="9a96d-163">Low level of encryption.</span></span> <span data-ttu-id="9a96d-164">Solo los datos enviados desde el cliente al servidor se cifran mediante el cifrado de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="9a96d-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="9a96d-165">Tenga en cuenta que no se cifran los datos enviados desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="9a96d-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="9a96d-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medio/cliente compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="9a96d-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-167">Nivel de cifrado compatible con el cliente.</span><span class="sxs-lookup"><span data-stu-id="9a96d-167">Client compatible level of encryption.</span></span> <span data-ttu-id="9a96d-168">Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran con el nivel de clave máximo admitido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="9a96d-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="9a96d-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (3)</span><span class="sxs-lookup"><span data-stu-id="9a96d-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-170">Alto nivel de cifrado.</span><span class="sxs-lookup"><span data-stu-id="9a96d-170">High level of encryption.</span></span> <span data-ttu-id="9a96d-171">Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran mediante cifrado de 128 bits seguro.</span><span class="sxs-lookup"><span data-stu-id="9a96d-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="9a96d-172">Los clientes que no admiten este nivel de cifrado no se pueden conectar.</span><span class="sxs-lookup"><span data-stu-id="9a96d-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="9a96d-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatible con FIPS** (4)</span><span class="sxs-lookup"><span data-stu-id="9a96d-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-174">Cifrado compatible con FIPS.</span><span class="sxs-lookup"><span data-stu-id="9a96d-174">FIPS compliant encryption.</span></span> <span data-ttu-id="9a96d-175">Todos los datos enviados del cliente al servidor y del servidor al cliente están cifrados y descifrados con los algoritmos de cifrado de Estándar federal de procesamiento de información (FIPS) mediante los módulos criptográficos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a96d-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="9a96d-176">FIPS es un estándar titulado "requisitos de seguridad para los módulos criptográficos".</span><span class="sxs-lookup"><span data-stu-id="9a96d-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="9a96d-177">FIPS 140-1 (1994) y FIPS 140-2 (2001) describen los requisitos gubernamentales para los módulos criptográficos de hardware y software que se usan en el gobierno de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="9a96d-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-178">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9a96d-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-181">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a96d-181">The name of the object.</span></span>

<span data-ttu-id="9a96d-182">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a96d-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-183">**PolicySourceMinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="9a96d-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-184">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-186">Indica si la propiedad **MinEncryptionLevel** está configurada por el servidor, por la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a96d-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="9a96d-187">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="9a96d-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-188">Servidor</span><span class="sxs-lookup"><span data-stu-id="9a96d-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-189">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-190">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9a96d-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-191">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="9a96d-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-192">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9a96d-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-193">**PolicySourceSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="9a96d-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-194">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-196">Indica si la propiedad **SecurityLayer** está configurada por el servidor, por la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a96d-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="9a96d-197">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="9a96d-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-198">Servidor</span><span class="sxs-lookup"><span data-stu-id="9a96d-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-199">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-200">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9a96d-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-201">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="9a96d-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-202">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9a96d-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-203">**PolicySourceUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="9a96d-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-204">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-206">Indica si la propiedad **UserAuthenticationRequired** está configurada por el servidor, por la Directiva de grupo o de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9a96d-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="9a96d-207">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="9a96d-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-208">Servidor</span><span class="sxs-lookup"><span data-stu-id="9a96d-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-209">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-210">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9a96d-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-211">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="9a96d-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-212">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="9a96d-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-213">**SecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="9a96d-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-214">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-216">Calificadores: **RDPSecurityLayer** ("capa de seguridad de RDP: comunicación entre serverand el cliente usará el cifrado RDP nativo"), **Negotiate** ("se usará la capa más segura compatible con el cliente. Si se admite, se usará TLS 1,0. "), se usará **SSL** (" SSL (TLS 1,0) para la autenticación del servidor, así como forencrypting todos los datos transferidos entre el servidor y el cliente. Esta configuración requiere que el servidor tenga un certificado compatible con SSL. "), **NEWTBD** (" un nuevo nivel de seguridad en Longhorn ").</span><span class="sxs-lookup"><span data-stu-id="9a96d-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-217">Especifica el nivel de seguridad utilizado entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="9a96d-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="9a96d-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Nivel de seguridad de RDP** (1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-219">La comunicación entre el servidor y el cliente usa el cifrado RDP nativo.</span><span class="sxs-lookup"><span data-stu-id="9a96d-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="9a96d-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span><span class="sxs-lookup"><span data-stu-id="9a96d-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-221">Se usa la capa más segura compatible con el cliente.</span><span class="sxs-lookup"><span data-stu-id="9a96d-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="9a96d-222">Si se admite, se usa SSL (TLS 1,0).</span><span class="sxs-lookup"><span data-stu-id="9a96d-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="9a96d-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span><span class="sxs-lookup"><span data-stu-id="9a96d-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-224">SSL (TLS 1,0) se utiliza para la autenticación de servidor y para el cifrado de todos los datos transferidos entre el servidor y el cliente.</span><span class="sxs-lookup"><span data-stu-id="9a96d-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="9a96d-225">Esta configuración requiere que el servidor tenga un certificado compatible con SSL.</span><span class="sxs-lookup"><span data-stu-id="9a96d-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="9a96d-226">Esta configuración no es compatible con un valor de **MinEncryptionLevel** de 1.</span><span class="sxs-lookup"><span data-stu-id="9a96d-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="9a96d-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span><span class="sxs-lookup"><span data-stu-id="9a96d-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-228">Un nuevo nivel de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9a96d-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="9a96d-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-231">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9a96d-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-232">Especifica el hash SHA1 en formato hexadecimal del certificado SSL que va a usar el servidor de destino.</span><span class="sxs-lookup"><span data-stu-id="9a96d-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="9a96d-233">La huella digital de un certificado puede encontrarse con el complemento MMC certificados en la pestaña detalles de la página Propiedades del certificado.</span><span class="sxs-lookup"><span data-stu-id="9a96d-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="9a96d-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-235">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-237">Indica el estado de la propiedad **SSLCertificateSHA1Hash** .</span><span class="sxs-lookup"><span data-stu-id="9a96d-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="9a96d-238">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="9a96d-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-239">No válido</span><span class="sxs-lookup"><span data-stu-id="9a96d-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-240">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-241">Autofirmado predeterminado</span><span class="sxs-lookup"><span data-stu-id="9a96d-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-242">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="9a96d-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-243">Directiva de grupo predeterminada aplicada</span><span class="sxs-lookup"><span data-stu-id="9a96d-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-244">3 (0X3)</span><span class="sxs-lookup"><span data-stu-id="9a96d-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="9a96d-245">Personalizados</span><span class="sxs-lookup"><span data-stu-id="9a96d-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-246">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9a96d-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-249">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="9a96d-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-250">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="9a96d-250">Current status of the object.</span></span> <span data-ttu-id="9a96d-251">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="9a96d-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9a96d-252">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="9a96d-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9a96d-253">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="9a96d-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9a96d-254">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="9a96d-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9a96d-255">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="9a96d-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9a96d-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9a96d-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="9a96d-257">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="9a96d-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-258">("Error")</span><span class="sxs-lookup"><span data-stu-id="9a96d-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-259">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="9a96d-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-260">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="9a96d-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-261">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="9a96d-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-262">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="9a96d-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-263">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="9a96d-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9a96d-264">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="9a96d-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-265">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="9a96d-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-266">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-268">Nombre del terminal.</span><span class="sxs-lookup"><span data-stu-id="9a96d-268">The name of the terminal.</span></span>

<span data-ttu-id="9a96d-269">Esta propiedad se hereda de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9a96d-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-270">**TerminalProtocol**</span><span class="sxs-lookup"><span data-stu-id="9a96d-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-273">Nombre del Protocolo de capa de sesión; por ejemplo, Microsoft RDP 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a96d-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-274">**Transporte**</span><span class="sxs-lookup"><span data-stu-id="9a96d-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-275">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9a96d-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-277">El tipo de transporte utilizado en la conexión; por ejemplo, TCP, NetBIOS o IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="9a96d-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="9a96d-278">**UserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="9a96d-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-279">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9a96d-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-281">Especifica el tipo de autenticación de usuario que se usa para las conexiones remotas.</span><span class="sxs-lookup"><span data-stu-id="9a96d-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="9a96d-282">Si se establece en 1, lo que significa habilitado, **UserAuthenticationRequired** requiere autenticación de usuario en el momento de la conexión para aumentar la protección del servidor frente a ataques de red.</span><span class="sxs-lookup"><span data-stu-id="9a96d-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="9a96d-283">Solo los clientes [Protocolo de escritorio remoto](remote-desktop-protocol.md) (RDP) que admiten la versión 6,0 o posterior de RDP pueden conectarse.</span><span class="sxs-lookup"><span data-stu-id="9a96d-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="9a96d-284">Para evitar interrupciones para los usuarios remotos, se recomienda que implemente los clientes RDP que admitan la versión de protocolo adecuada antes de habilitar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9a96d-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="9a96d-285">Use el método [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) para habilitar o deshabilitar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9a96d-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="9a96d-286"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="9a96d-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-287">La autenticación de usuario en la conexión está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="9a96d-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="9a96d-288"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-289">La autenticación de usuario en la conexión está habilitada.</span><span class="sxs-lookup"><span data-stu-id="9a96d-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9a96d-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="9a96d-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a96d-291">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a96d-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9a96d-292">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9a96d-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9a96d-293">Especifica si la conexión tiene como valor predeterminado el proceso de autenticación de Windows estándar o un paquete de autenticación que se ha instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9a96d-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="9a96d-294"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="9a96d-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-295">No tiene como valor predeterminado el proceso de autenticación de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="9a96d-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="9a96d-296"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="9a96d-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9a96d-297">Tiene como valor predeterminado el proceso de autenticación de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="9a96d-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a96d-298">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a96d-298">Remarks</span></span>

<span data-ttu-id="9a96d-299">Tenga en cuenta que las estaciones de ventana no asociadas a la sesión de consola no pueden tener acceso a los métodos y las propiedades de esta clase.</span><span class="sxs-lookup"><span data-stu-id="9a96d-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="9a96d-300">Si se realiza un intento de hacerlo especificando "Console" como el valor de la propiedad TerminalName, los métodos de este objeto devolverán **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="9a96d-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="9a96d-301">También se devolverá este código de error si una estación de ventana intenta llamar a métodos de este objeto con el fin de agregar o modificar las propiedades de seguridad de las cuentas LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="9a96d-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="9a96d-302">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="9a96d-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="9a96d-303">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C.</span><span class="sxs-lookup"><span data-stu-id="9a96d-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="9a96d-304">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="9a96d-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="9a96d-305">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="9a96d-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="9a96d-306">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9a96d-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9a96d-307">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9a96d-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9a96d-308">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="9a96d-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9a96d-309">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9a96d-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a96d-310">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a96d-310">Requirements</span></span>



| <span data-ttu-id="9a96d-311">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a96d-311">Requirement</span></span> | <span data-ttu-id="9a96d-312">Value</span><span class="sxs-lookup"><span data-stu-id="9a96d-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a96d-313">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a96d-313">Minimum supported client</span></span><br/> | <span data-ttu-id="9a96d-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a96d-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a96d-315">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a96d-315">Minimum supported server</span></span><br/> | <span data-ttu-id="9a96d-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a96d-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a96d-317">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9a96d-317">Namespace</span></span><br/>                | <span data-ttu-id="9a96d-318">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9a96d-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9a96d-319">MOF</span><span class="sxs-lookup"><span data-stu-id="9a96d-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a96d-320"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a96d-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a96d-321">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a96d-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a96d-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a96d-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a96d-323">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a96d-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a96d-324">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="9a96d-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

