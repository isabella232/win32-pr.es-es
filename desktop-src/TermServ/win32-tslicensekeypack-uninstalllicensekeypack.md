---
title: Método UninstallLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Desinstala un paquete de claves de licencia de Servicios de Escritorio remoto.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Método UninstallLicenseKeyPack Servicios de Escritorio remoto
- Método UninstallLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421961"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="c8ba5-106">Método UninstallLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="c8ba5-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="c8ba5-107">Desinstala un paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ba5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8ba5-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="c8ba5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8ba5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ba5-110">*ProductVersion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8ba5-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-111">Identificador de la versión del producto para el paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="c8ba5-112">0</span><span class="sxs-lookup"><span data-stu-id="c8ba5-112">0</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-113">No se admite.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c8ba5-114">1</span><span class="sxs-lookup"><span data-stu-id="c8ba5-114">1</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-115">No se admite.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c8ba5-116">2</span><span class="sxs-lookup"><span data-stu-id="c8ba5-116">2</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8ba5-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8ba5-118">*ProductType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8ba5-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-119">Tipo de producto del paquete de claves de licencia de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="c8ba5-120">0</span><span class="sxs-lookup"><span data-stu-id="c8ba5-120">0</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-121">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="c8ba5-122">Por lo tanto, cada dispositivo que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="c8ba5-123">1</span><span class="sxs-lookup"><span data-stu-id="c8ba5-123">1</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-124">El tipo de producto del paquete de claves de licencia Servicios de Escritorio remoto es por usuario.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="c8ba5-125">Por lo tanto, cada usuario que se conecta al servidor host de sesión de escritorio remoto debe tener una licencia.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="c8ba5-126">2</span><span class="sxs-lookup"><span data-stu-id="c8ba5-126">2</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-127">Este tipo de producto no es válido.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8ba5-128">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8ba5-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ba5-129">El número de licencias que se van a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ba5-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8ba5-130">Return value</span></span>

<span data-ttu-id="c8ba5-131">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c8ba5-132">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c8ba5-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c8ba5-133">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c8ba5-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ba5-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8ba5-134">Requirements</span></span>



| <span data-ttu-id="c8ba5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8ba5-135">Requirement</span></span> | <span data-ttu-id="c8ba5-136">Value</span><span class="sxs-lookup"><span data-stu-id="c8ba5-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ba5-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8ba5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ba5-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c8ba5-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c8ba5-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8ba5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ba5-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8ba5-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c8ba5-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8ba5-141">Namespace</span></span><br/>                | <span data-ttu-id="c8ba5-142">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c8ba5-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c8ba5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c8ba5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8ba5-144"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8ba5-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8ba5-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8ba5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8ba5-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8ba5-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ba5-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8ba5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ba5-148">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="c8ba5-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





