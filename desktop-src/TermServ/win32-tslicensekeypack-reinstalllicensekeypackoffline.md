---
title: Método ReinstallLicenseKeyPackOffline de la clase Win32_TSLicenseKeyPack
description: Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto que usa el identificador de licencia que se recibió a través de Internet o el teléfono.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Método ReinstallLicenseKeyPackOffline Servicios de Escritorio remoto
- Método ReinstallLicenseKeyPackOffline Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905048"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="91a53-106">Método ReinstallLicenseKeyPackOffline de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="91a53-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="91a53-107">Vuelve a instalar un paquete de claves de licencia Servicios de Escritorio remoto que usa el identificador de licencia que se recibió a través de Internet o el teléfono.</span><span class="sxs-lookup"><span data-stu-id="91a53-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a53-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91a53-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="91a53-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91a53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a53-110">*sLicenseKeyPackId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91a53-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a53-111">Contiene el código de licencia de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="91a53-111">Contains the 35-character license code.</span></span> <span data-ttu-id="91a53-112">Solo se debe proporcionar como entrada la cadena de caracteres alfanuméricos de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="91a53-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="91a53-113">No se deben agregar guiones.</span><span class="sxs-lookup"><span data-stu-id="91a53-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="91a53-114">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="91a53-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91a53-115">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="91a53-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a53-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91a53-116">Return value</span></span>

<span data-ttu-id="91a53-117">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="91a53-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="91a53-118">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="91a53-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="91a53-119">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="91a53-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91a53-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a53-120">Requirements</span></span>



| <span data-ttu-id="91a53-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a53-121">Requirement</span></span> | <span data-ttu-id="91a53-122">Value</span><span class="sxs-lookup"><span data-stu-id="91a53-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a53-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91a53-123">Minimum supported client</span></span><br/> | <span data-ttu-id="91a53-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="91a53-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="91a53-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91a53-125">Minimum supported server</span></span><br/> | <span data-ttu-id="91a53-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91a53-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="91a53-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="91a53-127">Namespace</span></span><br/>                | <span data-ttu-id="91a53-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="91a53-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="91a53-129">MOF</span><span class="sxs-lookup"><span data-stu-id="91a53-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91a53-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91a53-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="91a53-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91a53-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91a53-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91a53-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a53-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="91a53-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a53-134">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="91a53-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





