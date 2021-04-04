---
description: Representa la configuración del equipo virtual Terminal Services en un host.
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Msvm_TerminalServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811318"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="d49f2-103">MSVM \_ TerminalServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="d49f2-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="d49f2-104">Representa la configuración del equipo virtual Terminal Services en un host.</span><span class="sxs-lookup"><span data-stu-id="d49f2-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="d49f2-105">Las propiedades de esta clase no se pueden modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="d49f2-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="d49f2-106">El cliente debe llamar al método [**MSVM \_ TerminalService. ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) para modificar cualquiera de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d49f2-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="d49f2-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d49f2-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49f2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d49f2-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="d49f2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d49f2-109">Members</span></span>

<span data-ttu-id="d49f2-110">La clase **MSVM \_ TerminalServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d49f2-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d49f2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d49f2-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d49f2-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d49f2-112">Properties</span></span>

<span data-ttu-id="d49f2-113">La clase **MSVM \_ TerminalServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d49f2-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d49f2-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="d49f2-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-115">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d49f2-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-117">La lista de algoritmos hash aceptados para comprobar la firma de los tokens de autenticación federada.</span><span class="sxs-lookup"><span data-stu-id="d49f2-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="d49f2-118">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d49f2-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-119">**AuthCertificateHash**</span><span class="sxs-lookup"><span data-stu-id="d49f2-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-120">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="d49f2-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-122">El hash del certificado que se va a usar para la autenticación remota.</span><span class="sxs-lookup"><span data-stu-id="d49f2-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d49f2-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d49f2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-126">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d49f2-126">A short description of the object.</span></span> <span data-ttu-id="d49f2-127">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d49f2-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d49f2-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d49f2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-131">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d49f2-131">A description of the object.</span></span> <span data-ttu-id="d49f2-132">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d49f2-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-133">**DisableSelfSignedCertificateGeneration**</span><span class="sxs-lookup"><span data-stu-id="d49f2-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d49f2-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-136">Deshabilita la generación de certificados autofirmados.</span><span class="sxs-lookup"><span data-stu-id="d49f2-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d49f2-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d49f2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-140">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d49f2-140">A display name for the object.</span></span> <span data-ttu-id="d49f2-141">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d49f2-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d49f2-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d49f2-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-145">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d49f2-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-146">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d49f2-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d49f2-147">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d49f2-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-148">**ListenerPort**</span><span class="sxs-lookup"><span data-stu-id="d49f2-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49f2-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-151">Puerto de red en el que se realizará la conexión inicial de la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="d49f2-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="d49f2-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="d49f2-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49f2-153">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d49f2-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d49f2-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49f2-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d49f2-155">La lista de hashes de certificado de emisor de confianza para comprobar la firma de los tokens de autenticación federada.</span><span class="sxs-lookup"><span data-stu-id="d49f2-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="d49f2-156">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d49f2-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d49f2-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d49f2-157">Requirements</span></span>



| <span data-ttu-id="d49f2-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="d49f2-158">Requirement</span></span> | <span data-ttu-id="d49f2-159">Value</span><span class="sxs-lookup"><span data-stu-id="d49f2-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d49f2-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d49f2-160">Minimum supported client</span></span><br/> | <span data-ttu-id="d49f2-161">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d49f2-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d49f2-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d49f2-162">Minimum supported server</span></span><br/> | <span data-ttu-id="d49f2-163">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d49f2-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d49f2-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d49f2-164">Namespace</span></span><br/>                | <span data-ttu-id="d49f2-165">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d49f2-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d49f2-166">MOF</span><span class="sxs-lookup"><span data-stu-id="d49f2-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d49f2-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d49f2-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d49f2-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d49f2-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d49f2-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d49f2-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

