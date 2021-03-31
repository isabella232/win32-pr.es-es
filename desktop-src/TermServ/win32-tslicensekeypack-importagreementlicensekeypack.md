---
title: Método ImportAgreementLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Método ImportAgreementLicenseKeyPack Servicios de Escritorio remoto
- Método ImportAgreementLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151084"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="77e81-106">Método ImportAgreementLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="77e81-106">ImportAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="77e81-107">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un contrato de licencia y se conecta automáticamente a través de Internet para validar la licencia del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="77e81-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e81-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77e81-108">Syntax</span></span>


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="77e81-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77e81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77e81-110">*AgreementType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-111">Tipo de contrato.</span><span class="sxs-lookup"><span data-stu-id="77e81-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="77e81-112">0</span><span class="sxs-lookup"><span data-stu-id="77e81-112">0</span></span>
</dt> <dd>

<span data-ttu-id="77e81-113">El paquete de claves de licencia procede de un contrato de licencia por volumen Select (para clientes con 250 o más equipos).</span><span class="sxs-lookup"><span data-stu-id="77e81-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="77e81-114">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="77e81-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-115">1</span><span class="sxs-lookup"><span data-stu-id="77e81-115">1</span></span>
</dt> <dd>

<span data-ttu-id="77e81-116">El paquete de claves de licencia procede de un contrato de licencia por volumen empresarial para clientes con 250 o más equipos.</span><span class="sxs-lookup"><span data-stu-id="77e81-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="77e81-117">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="77e81-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-118">2</span><span class="sxs-lookup"><span data-stu-id="77e81-118">2</span></span>
</dt> <dd>

<span data-ttu-id="77e81-119">El paquete de claves de licencia procede de un contrato de licencia por volumen de campus para una institución de educación superior.</span><span class="sxs-lookup"><span data-stu-id="77e81-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="77e81-120">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="77e81-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-121">3</span><span class="sxs-lookup"><span data-stu-id="77e81-121">3</span></span>
</dt> <dd>

<span data-ttu-id="77e81-122">El paquete de claves de licencia proviene de un contrato de licencia por volumen escolar para instituciones principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="77e81-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="77e81-123">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="77e81-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-124">4</span><span class="sxs-lookup"><span data-stu-id="77e81-124">4</span></span>
</dt> <dd>

<span data-ttu-id="77e81-125">El paquete de claves de licencia procede de un contrato de licencia de proveedor de servicios para que los proveedores de servicios de licencias de software de Microsoft se basen mensualmente.</span><span class="sxs-lookup"><span data-stu-id="77e81-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="77e81-126">El parámetro *sAgreementNumber* es el número de inscripción (siete dígitos) que se encuentra en el formulario del acuerdo firmado.</span><span class="sxs-lookup"><span data-stu-id="77e81-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-127">5</span><span class="sxs-lookup"><span data-stu-id="77e81-127">5</span></span>
</dt> <dd>

<span data-ttu-id="77e81-128">El paquete de claves de licencia procede de otro contrato de licencia, como un valor abierto, una licencia Open de varios años y una licencia de suscripción abierta.</span><span class="sxs-lookup"><span data-stu-id="77e81-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="77e81-129">El parámetro *sAgreementNumber* es el número de contrato proporcionado con la información del programa.</span><span class="sxs-lookup"><span data-stu-id="77e81-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="77e81-130">*sAgreementNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-131">Número de contrato o número de inscripción.</span><span class="sxs-lookup"><span data-stu-id="77e81-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="77e81-132">El parámetro *sAgreementNumber* es una cadena numérica de siete dígitos sin guiones.</span><span class="sxs-lookup"><span data-stu-id="77e81-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-133">*ProductVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-134">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="77e81-134">Product version.</span></span>

<dt>

<span data-ttu-id="77e81-135">0</span><span class="sxs-lookup"><span data-stu-id="77e81-135">0</span></span>
</dt> <dd>

<span data-ttu-id="77e81-136">No se admite.</span><span class="sxs-lookup"><span data-stu-id="77e81-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-137">1</span><span class="sxs-lookup"><span data-stu-id="77e81-137">1</span></span>
</dt> <dd>

<span data-ttu-id="77e81-138">No se admite.</span><span class="sxs-lookup"><span data-stu-id="77e81-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-139">2</span><span class="sxs-lookup"><span data-stu-id="77e81-139">2</span></span>
</dt> <dd>

<span data-ttu-id="77e81-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77e81-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="77e81-141">*ProductType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-142">Tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="77e81-142">Product type.</span></span>

<dt>

<span data-ttu-id="77e81-143">0</span><span class="sxs-lookup"><span data-stu-id="77e81-143">0</span></span>
</dt> <dd>

<span data-ttu-id="77e81-144">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77e81-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="77e81-145">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="77e81-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-146">1</span><span class="sxs-lookup"><span data-stu-id="77e81-146">1</span></span>
</dt> <dd>

<span data-ttu-id="77e81-147">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="77e81-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="77e81-148">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="77e81-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-149">2</span><span class="sxs-lookup"><span data-stu-id="77e81-149">2</span></span>
</dt> <dd>

<span data-ttu-id="77e81-150">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="77e81-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="77e81-151">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-152">Número de licencias que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="77e81-152">Number of licenses to import.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-153">*sSourceLSName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-153">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-154">Nombre del servidor de licencias de origen Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="77e81-154">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="77e81-155">Este es el nombre completo completo o la dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="77e81-155">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-156">*sSourceLSProductId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77e81-156">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-157">Identificador del servidor de licencias Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="77e81-157">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="77e81-158">Es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.</span><span class="sxs-lookup"><span data-stu-id="77e81-158">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="77e81-159">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="77e81-159">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77e81-160">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="77e81-160">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77e81-161">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77e81-161">Return value</span></span>

<span data-ttu-id="77e81-162">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="77e81-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="77e81-163">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="77e81-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="77e81-164">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="77e81-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77e81-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77e81-165">Requirements</span></span>



| <span data-ttu-id="77e81-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e81-166">Requirement</span></span> | <span data-ttu-id="77e81-167">Value</span><span class="sxs-lookup"><span data-stu-id="77e81-167">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="77e81-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77e81-168">Minimum supported client</span></span><br/> | <span data-ttu-id="77e81-169">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="77e81-169">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="77e81-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77e81-170">Minimum supported server</span></span><br/> | <span data-ttu-id="77e81-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77e81-171">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="77e81-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77e81-172">Namespace</span></span><br/>                | <span data-ttu-id="77e81-173">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="77e81-173">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="77e81-174">MOF</span><span class="sxs-lookup"><span data-stu-id="77e81-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77e81-175"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77e81-175"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="77e81-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77e81-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77e81-177"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e81-177"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e81-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="77e81-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e81-179">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="77e81-179">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





