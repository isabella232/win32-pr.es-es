---
title: Método InstallOpenLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Instala una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- Método InstallOpenLicenseKeyPack Servicios de Escritorio remoto
- Método InstallOpenLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método InstallOpenLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489838"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="b8b24-106">Método InstallOpenLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="b8b24-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="b8b24-107">Instala una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="b8b24-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b24-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8b24-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="b8b24-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8b24-109">Parameters</span></span>

<span data-ttu-id="b8b24-110">*sLicenseNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8b24-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="b8b24-111">cadena numérica de 8 caracteres que se proporciona con el paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="b8b24-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="b8b24-112">El parámetro *sLicenseNumber* no puede contener guiones.</span><span class="sxs-lookup"><span data-stu-id="b8b24-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="b8b24-113">*sAuthorizationNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8b24-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="b8b24-114">cadena alfanumérica de 15 caracteres que se proporciona con la clave de licencia.</span><span class="sxs-lookup"><span data-stu-id="b8b24-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="b8b24-115">El parámetro *sAuthorizationNumber* no puede contener guiones.</span><span class="sxs-lookup"><span data-stu-id="b8b24-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="b8b24-116">*ProductVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8b24-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="b8b24-117">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="b8b24-117">Product version.</span></span>

| <span data-ttu-id="b8b24-118">Value</span><span class="sxs-lookup"><span data-stu-id="b8b24-118">Value</span></span> | <span data-ttu-id="b8b24-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8b24-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b8b24-120">0</span><span class="sxs-lookup"><span data-stu-id="b8b24-120">0</span></span> | <span data-ttu-id="b8b24-121">No compatible</span><span class="sxs-lookup"><span data-stu-id="b8b24-121">Not supported</span></span> |
| <span data-ttu-id="b8b24-122">1</span><span class="sxs-lookup"><span data-stu-id="b8b24-122">1</span></span> | <span data-ttu-id="b8b24-123">No compatible</span><span class="sxs-lookup"><span data-stu-id="b8b24-123">Not supported</span></span> |
| <span data-ttu-id="b8b24-124">2</span><span class="sxs-lookup"><span data-stu-id="b8b24-124">2</span></span> | <span data-ttu-id="b8b24-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8b24-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="b8b24-126">4</span><span class="sxs-lookup"><span data-stu-id="b8b24-126">4</span></span> | <span data-ttu-id="b8b24-127">Windows Server 2012 o Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b8b24-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="b8b24-128">5</span><span class="sxs-lookup"><span data-stu-id="b8b24-128">5</span></span> | <span data-ttu-id="b8b24-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b8b24-129">Windows Server 2016</span></span> |
| <span data-ttu-id="b8b24-130">6</span><span class="sxs-lookup"><span data-stu-id="b8b24-130">6</span></span> | <span data-ttu-id="b8b24-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="b8b24-131">Windows Server 2019</span></span> |

<span data-ttu-id="b8b24-132">*ProductType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8b24-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8b24-133">Tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="b8b24-133">Product type.</span></span>

| <span data-ttu-id="b8b24-134">Value</span><span class="sxs-lookup"><span data-stu-id="b8b24-134">Value</span></span> | <span data-ttu-id="b8b24-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8b24-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b8b24-136">0</span><span class="sxs-lookup"><span data-stu-id="b8b24-136">0</span></span> | <span data-ttu-id="b8b24-137">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8b24-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="b8b24-138">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="b8b24-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="b8b24-139">1</span><span class="sxs-lookup"><span data-stu-id="b8b24-139">1</span></span> | <span data-ttu-id="b8b24-140">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="b8b24-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="b8b24-141">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="b8b24-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="b8b24-142">2</span><span class="sxs-lookup"><span data-stu-id="b8b24-142">2</span></span> | <span data-ttu-id="b8b24-143">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="b8b24-143">This product type is not valid.</span></span> |

<span data-ttu-id="b8b24-144">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8b24-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="b8b24-145">El número de licencias que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="b8b24-145">The number of licenses to install.</span></span>

<span data-ttu-id="b8b24-146">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b8b24-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="b8b24-147">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="b8b24-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8b24-148">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8b24-148">Return value</span></span>

<span data-ttu-id="b8b24-149">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="b8b24-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b8b24-150">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="b8b24-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b8b24-151">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b8b24-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b24-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8b24-152">Remarks</span></span>

<span data-ttu-id="b8b24-153">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="b8b24-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b8b24-154">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b8b24-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b8b24-155">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b8b24-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b8b24-156">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b8b24-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b8b24-157">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b8b24-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b24-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8b24-158">Requirements</span></span>



| <span data-ttu-id="b8b24-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8b24-159">Requirement</span></span> | <span data-ttu-id="b8b24-160">Value</span><span class="sxs-lookup"><span data-stu-id="b8b24-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b24-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8b24-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b24-162">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b8b24-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b8b24-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8b24-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b24-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8b24-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b8b24-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8b24-165">Namespace</span></span><br/>                | <span data-ttu-id="b8b24-166">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b8b24-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b8b24-167">MOF</span><span class="sxs-lookup"><span data-stu-id="b8b24-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8b24-168"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8b24-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8b24-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8b24-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8b24-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8b24-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b24-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8b24-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b24-172">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b8b24-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

