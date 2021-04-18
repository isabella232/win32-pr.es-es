---
title: Método ImportOpenPurchaseLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Open Servicios de Escritorio remoto.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Método ImportOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ImportOpenPurchaseLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676953"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="3def2-106">Método ImportOpenPurchaseLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="3def2-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="3def2-107">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia Open Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3def2-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="3def2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3def2-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="3def2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3def2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3def2-110">*sLicenseNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-111">cadena numérica de 8 caracteres que se proporciona con el paquete de claves de licencia.</span><span class="sxs-lookup"><span data-stu-id="3def2-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="3def2-112">El parámetro *sLicenseNumber* no puede contener guiones.</span><span class="sxs-lookup"><span data-stu-id="3def2-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-113">*sAuthorizationNumber* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-114">cadena alfanumérica de 15 caracteres que se proporciona con la clave de licencia.</span><span class="sxs-lookup"><span data-stu-id="3def2-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="3def2-115">El parámetro *sAuthorizationNumber* no puede contener guiones.</span><span class="sxs-lookup"><span data-stu-id="3def2-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-116">*ProductVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-117">Versión del producto.</span><span class="sxs-lookup"><span data-stu-id="3def2-117">Product version.</span></span>

<dt>

<span data-ttu-id="3def2-118">0</span><span class="sxs-lookup"><span data-stu-id="3def2-118">0</span></span>
</dt> <dd>

<span data-ttu-id="3def2-119">No se admite.</span><span class="sxs-lookup"><span data-stu-id="3def2-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-120">1</span><span class="sxs-lookup"><span data-stu-id="3def2-120">1</span></span>
</dt> <dd>

<span data-ttu-id="3def2-121">No se admite.</span><span class="sxs-lookup"><span data-stu-id="3def2-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-122">2</span><span class="sxs-lookup"><span data-stu-id="3def2-122">2</span></span>
</dt> <dd>

<span data-ttu-id="3def2-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3def2-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3def2-124">*ProductType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-125">Tipo de producto.</span><span class="sxs-lookup"><span data-stu-id="3def2-125">Product type.</span></span>

<dt>

<span data-ttu-id="3def2-126">0</span><span class="sxs-lookup"><span data-stu-id="3def2-126">0</span></span>
</dt> <dd>

<span data-ttu-id="3def2-127">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3def2-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="3def2-128">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="3def2-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-129">1</span><span class="sxs-lookup"><span data-stu-id="3def2-129">1</span></span>
</dt> <dd>

<span data-ttu-id="3def2-130">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="3def2-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="3def2-131">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="3def2-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-132">2</span><span class="sxs-lookup"><span data-stu-id="3def2-132">2</span></span>
</dt> <dd>

<span data-ttu-id="3def2-133">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="3def2-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3def2-134">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-135">El número de licencias que se van a importar</span><span class="sxs-lookup"><span data-stu-id="3def2-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="3def2-136">*sSourceLSName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-137">Nombre del servidor de licencias de origen Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3def2-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="3def2-138">Este es el nombre completo completo o la dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="3def2-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-139">*sSourceLSProductId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3def2-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-140">Identificador del servidor de licencias Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3def2-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="3def2-141">Es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.</span><span class="sxs-lookup"><span data-stu-id="3def2-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="3def2-142">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3def2-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3def2-143">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="3def2-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3def2-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3def2-144">Return value</span></span>

<span data-ttu-id="3def2-145">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3def2-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3def2-146">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3def2-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3def2-147">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3def2-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3def2-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3def2-148">Requirements</span></span>



| <span data-ttu-id="3def2-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3def2-149">Requirement</span></span> | <span data-ttu-id="3def2-150">Value</span><span class="sxs-lookup"><span data-stu-id="3def2-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3def2-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3def2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3def2-152">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3def2-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3def2-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3def2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3def2-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3def2-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3def2-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3def2-155">Namespace</span></span><br/>                | <span data-ttu-id="3def2-156">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3def2-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3def2-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3def2-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3def2-158"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3def2-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3def2-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3def2-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3def2-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3def2-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3def2-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="3def2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3def2-162">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="3def2-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





