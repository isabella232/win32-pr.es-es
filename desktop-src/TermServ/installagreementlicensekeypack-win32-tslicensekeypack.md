---
title: Método InstallAgreementLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Método InstallAgreementLicenseKeyPack Servicios de Escritorio remoto
- Método InstallAgreementLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686174"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="618ab-106">Método InstallAgreementLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="618ab-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="618ab-107">Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="618ab-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="618ab-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="618ab-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="618ab-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="618ab-109">Parameters</span></span>

<span data-ttu-id="618ab-110">*AgreementType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="618ab-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="618ab-111">Tipo de contrato.</span><span class="sxs-lookup"><span data-stu-id="618ab-111">Agreement type.</span></span>

| <span data-ttu-id="618ab-112">Value</span><span class="sxs-lookup"><span data-stu-id="618ab-112">Value</span></span> | <span data-ttu-id="618ab-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="618ab-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="618ab-114">0</span><span class="sxs-lookup"><span data-stu-id="618ab-114">0</span></span> | <span data-ttu-id="618ab-115">El paquete de claves de licencia procede de un contrato de licencia por volumen Select (para clientes con 250 o más equipos).</span><span class="sxs-lookup"><span data-stu-id="618ab-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="618ab-116">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="618ab-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="618ab-117">1</span><span class="sxs-lookup"><span data-stu-id="618ab-117">1</span></span> | <span data-ttu-id="618ab-118">El paquete de claves de licencia procede de un contrato de licencia por volumen empresarial para clientes con 250 o más equipos.</span><span class="sxs-lookup"><span data-stu-id="618ab-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="618ab-119">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="618ab-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="618ab-120">2</span><span class="sxs-lookup"><span data-stu-id="618ab-120">2</span></span> | <span data-ttu-id="618ab-121">El paquete de claves de licencia procede de un contrato de licencia por volumen de campus para una institución de educación superior.</span><span class="sxs-lookup"><span data-stu-id="618ab-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="618ab-122">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="618ab-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="618ab-123">3</span><span class="sxs-lookup"><span data-stu-id="618ab-123">3</span></span> | <span data-ttu-id="618ab-124">El paquete de claves de licencia proviene de un contrato de licencia por volumen escolar para instituciones principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="618ab-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="618ab-125">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="618ab-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="618ab-126">4</span><span class="sxs-lookup"><span data-stu-id="618ab-126">4</span></span> | <span data-ttu-id="618ab-127">El paquete de claves de licencia procede de un contrato de licencia de proveedor de servicios para que los proveedores de servicios de licencias de software de Microsoft se basen mensualmente.</span><span class="sxs-lookup"><span data-stu-id="618ab-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="618ab-128">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="618ab-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="618ab-129">5</span><span class="sxs-lookup"><span data-stu-id="618ab-129">5</span></span> | <span data-ttu-id="618ab-130">El paquete de claves de licencia procede de otro contrato de licencia, como un valor abierto, una licencia Open de varios años y una licencia de suscripción abierta.</span><span class="sxs-lookup"><span data-stu-id="618ab-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="618ab-131">El parámetro *sAgreementNumber* es el número de contrato proporcionado con la información del programa.</span><span class="sxs-lookup"><span data-stu-id="618ab-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="618ab-132">*sAgreementNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="618ab-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="618ab-133">Número de contrato o número de inscripción.</span><span class="sxs-lookup"><span data-stu-id="618ab-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="618ab-134">El parámetro *sAgreementNumber* es una cadena numérica de siete dígitos sin guiones.</span><span class="sxs-lookup"><span data-stu-id="618ab-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="618ab-135">*ProductVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="618ab-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="618ab-136">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="618ab-136">Product version.</span></span>

| <span data-ttu-id="618ab-137">Value</span><span class="sxs-lookup"><span data-stu-id="618ab-137">Value</span></span> | <span data-ttu-id="618ab-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="618ab-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="618ab-139">0</span><span class="sxs-lookup"><span data-stu-id="618ab-139">0</span></span> | <span data-ttu-id="618ab-140">No compatible</span><span class="sxs-lookup"><span data-stu-id="618ab-140">Not supported</span></span> |
| <span data-ttu-id="618ab-141">1</span><span class="sxs-lookup"><span data-stu-id="618ab-141">1</span></span> | <span data-ttu-id="618ab-142">No compatible</span><span class="sxs-lookup"><span data-stu-id="618ab-142">Not supported</span></span> |
| <span data-ttu-id="618ab-143">2</span><span class="sxs-lookup"><span data-stu-id="618ab-143">2</span></span> | <span data-ttu-id="618ab-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="618ab-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="618ab-145">4</span><span class="sxs-lookup"><span data-stu-id="618ab-145">4</span></span> | <span data-ttu-id="618ab-146">Windows Server 2012 o Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="618ab-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="618ab-147">5</span><span class="sxs-lookup"><span data-stu-id="618ab-147">5</span></span> | <span data-ttu-id="618ab-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="618ab-148">Windows Server 2016</span></span> |
| <span data-ttu-id="618ab-149">6</span><span class="sxs-lookup"><span data-stu-id="618ab-149">6</span></span> | <span data-ttu-id="618ab-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="618ab-150">Windows Server 2019</span></span> |

<span data-ttu-id="618ab-151">*ProductType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="618ab-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="618ab-152">Tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="618ab-152">Product type.</span></span>

| <span data-ttu-id="618ab-153">Value</span><span class="sxs-lookup"><span data-stu-id="618ab-153">Value</span></span> | <span data-ttu-id="618ab-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="618ab-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="618ab-155">0</span><span class="sxs-lookup"><span data-stu-id="618ab-155">0</span></span> | <span data-ttu-id="618ab-156">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="618ab-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="618ab-157">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="618ab-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="618ab-158">1</span><span class="sxs-lookup"><span data-stu-id="618ab-158">1</span></span> | <span data-ttu-id="618ab-159">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="618ab-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="618ab-160">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="618ab-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="618ab-161">2</span><span class="sxs-lookup"><span data-stu-id="618ab-161">2</span></span> | <span data-ttu-id="618ab-162">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="618ab-162">This product type is not valid.</span></span> |

<span data-ttu-id="618ab-163">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="618ab-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="618ab-164">Número de licencias que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="618ab-164">Number of licenses to install.</span></span>

<span data-ttu-id="618ab-165">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="618ab-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="618ab-166">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="618ab-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="618ab-167">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="618ab-167">Return value</span></span>

<span data-ttu-id="618ab-168">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="618ab-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="618ab-169">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="618ab-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="618ab-170">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="618ab-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="618ab-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="618ab-171">Remarks</span></span>

<span data-ttu-id="618ab-172">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="618ab-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="618ab-173">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="618ab-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="618ab-174">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="618ab-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="618ab-175">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="618ab-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="618ab-176">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="618ab-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="618ab-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="618ab-177">Requirements</span></span>

| <span data-ttu-id="618ab-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="618ab-178">Requirement</span></span> | <span data-ttu-id="618ab-179">Value</span><span class="sxs-lookup"><span data-stu-id="618ab-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="618ab-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="618ab-180">Minimum supported client</span></span><br/> | <span data-ttu-id="618ab-181">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="618ab-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="618ab-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="618ab-182">Minimum supported server</span></span><br/> | <span data-ttu-id="618ab-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="618ab-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="618ab-184">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="618ab-184">Namespace</span></span><br/>                | <span data-ttu-id="618ab-185">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="618ab-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="618ab-186">MOF</span><span class="sxs-lookup"><span data-stu-id="618ab-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="618ab-187"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="618ab-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="618ab-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="618ab-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="618ab-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="618ab-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="618ab-190">Vea también</span><span class="sxs-lookup"><span data-stu-id="618ab-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="618ab-191">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="618ab-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

