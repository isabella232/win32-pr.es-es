---
title: Método ReinstallOpenPurchaseLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Vuelve a instalar una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Método ReinstallOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ReinstallOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803602"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="826a4-106">Método ReinstallOpenPurchaseLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="826a4-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="826a4-107">Vuelve a instalar una licencia abierta Servicios de Escritorio remoto paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="826a4-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="826a4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="826a4-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="826a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="826a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="826a4-110">*sLicenseNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="826a4-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826a4-111">cadena numérica de 8 caracteres que se proporciona con el paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="826a4-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="826a4-112">El parámetro *sLicenseNumber* no puede contener guiones.</span><span class="sxs-lookup"><span data-stu-id="826a4-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-113">*sAuthorizationNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="826a4-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826a4-114">cadena alfanumérica de 15 caracteres que se proporciona con la clave de licencia.</span><span class="sxs-lookup"><span data-stu-id="826a4-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="826a4-115">El parámetro *sAuthorizationNumber* no puede contener guiones.</span><span class="sxs-lookup"><span data-stu-id="826a4-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-116">*ProductVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="826a4-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826a4-117">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="826a4-117">Product version.</span></span>

<dt>

<span data-ttu-id="826a4-118">0</span><span class="sxs-lookup"><span data-stu-id="826a4-118">0</span></span>
</dt> <dd>

<span data-ttu-id="826a4-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="826a4-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-120">1</span><span class="sxs-lookup"><span data-stu-id="826a4-120">1</span></span>
</dt> <dd>

<span data-ttu-id="826a4-121">No se admite.</span><span class="sxs-lookup"><span data-stu-id="826a4-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-122">2</span><span class="sxs-lookup"><span data-stu-id="826a4-122">2</span></span>
</dt> <dd>

<span data-ttu-id="826a4-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="826a4-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="826a4-124">*ProductType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="826a4-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826a4-125">Tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="826a4-125">Product type.</span></span>

<dt>

<span data-ttu-id="826a4-126">0</span><span class="sxs-lookup"><span data-stu-id="826a4-126">0</span></span>
</dt> <dd>

<span data-ttu-id="826a4-127">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="826a4-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="826a4-128">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="826a4-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-129">1</span><span class="sxs-lookup"><span data-stu-id="826a4-129">1</span></span>
</dt> <dd>

<span data-ttu-id="826a4-130">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="826a4-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="826a4-131">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="826a4-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-132">2</span><span class="sxs-lookup"><span data-stu-id="826a4-132">2</span></span>
</dt> <dd>

<span data-ttu-id="826a4-133">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="826a4-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="826a4-134">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="826a4-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="826a4-135">El número de licencias que se van a instalar.</span><span class="sxs-lookup"><span data-stu-id="826a4-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="826a4-136">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="826a4-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="826a4-137">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="826a4-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="826a4-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="826a4-138">Return value</span></span>

<span data-ttu-id="826a4-139">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="826a4-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="826a4-140">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="826a4-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="826a4-141">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="826a4-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="826a4-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="826a4-142">Requirements</span></span>



| <span data-ttu-id="826a4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="826a4-143">Requirement</span></span> | <span data-ttu-id="826a4-144">Value</span><span class="sxs-lookup"><span data-stu-id="826a4-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="826a4-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826a4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="826a4-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="826a4-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="826a4-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="826a4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="826a4-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="826a4-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="826a4-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="826a4-149">Namespace</span></span><br/>                | <span data-ttu-id="826a4-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="826a4-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="826a4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="826a4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="826a4-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="826a4-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="826a4-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="826a4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="826a4-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="826a4-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826a4-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="826a4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826a4-156">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="826a4-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





