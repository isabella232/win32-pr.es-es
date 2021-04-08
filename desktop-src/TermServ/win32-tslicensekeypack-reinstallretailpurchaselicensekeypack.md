---
title: Método ReinstallRetailPurchaseLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta directa.
ms.assetid: 19528726-8DEB-4D03-BFA6-647C8A612FA2
ms.tgt_platform: multiple
keywords:
- Método ReinstallRetailPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método ReinstallRetailPurchaseLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ReinstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4caa8635eaf28ad823add500883832a7fe885b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078963"
---
# <a name="reinstallretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e7e21-106">Método ReinstallRetailPurchaseLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="e7e21-106">ReinstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e7e21-107">Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta directa.</span><span class="sxs-lookup"><span data-stu-id="e7e21-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e21-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7e21-108">Syntax</span></span>


```mof
uint32 ReinstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="e7e21-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7e21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e21-110">*sLicenseCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e7e21-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e21-111">Contiene el código de licencia de 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7e21-111">Contains the 25-character license code.</span></span> <span data-ttu-id="e7e21-112">Solo se debe proporcionar como entrada la cadena de caracteres alfanuméricos de 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e7e21-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="e7e21-113">No se deben agregar guiones.</span><span class="sxs-lookup"><span data-stu-id="e7e21-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="e7e21-114">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e7e21-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e21-115">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="e7e21-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e21-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7e21-116">Return value</span></span>

<span data-ttu-id="e7e21-117">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e7e21-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e7e21-118">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e7e21-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e7e21-119">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e7e21-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e21-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7e21-120">Requirements</span></span>



| <span data-ttu-id="e7e21-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7e21-121">Requirement</span></span> | <span data-ttu-id="e7e21-122">Value</span><span class="sxs-lookup"><span data-stu-id="e7e21-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e21-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7e21-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e21-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e7e21-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e7e21-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7e21-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e21-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e21-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e7e21-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7e21-127">Namespace</span></span><br/>                | <span data-ttu-id="e7e21-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e7e21-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e7e21-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e7e21-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7e21-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7e21-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7e21-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7e21-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e21-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e21-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e21-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7e21-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e21-134">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="e7e21-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





