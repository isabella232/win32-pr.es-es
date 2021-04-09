---
title: Método RemoveLicensesWithIdCount de la clase Win32_TSLicenseKeyPack
description: Quita el número especificado de licencias de Servicios de Escritorio remoto del paquete de claves especificado.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Método RemoveLicensesWithIdCount Servicios de Escritorio remoto
- Método RemoveLicensesWithIdCount Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078962"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="6ae0a-106">Método RemoveLicensesWithIdCount de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="6ae0a-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="6ae0a-107">Quita el número especificado de licencias de Servicios de Escritorio remoto del paquete de claves especificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae0a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ae0a-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="6ae0a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ae0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae0a-110">*KeyPackId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ae0a-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae0a-111">Identificador del paquete de claves que contiene las licencias que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="6ae0a-112">*LicenseCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ae0a-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ae0a-113">El número de licencias que se van a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae0a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ae0a-114">Return value</span></span>

<span data-ttu-id="6ae0a-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6ae0a-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6ae0a-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6ae0a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae0a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ae0a-118">Requirements</span></span>



| <span data-ttu-id="6ae0a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae0a-119">Requirement</span></span> | <span data-ttu-id="6ae0a-120">Value</span><span class="sxs-lookup"><span data-stu-id="6ae0a-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae0a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ae0a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae0a-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6ae0a-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6ae0a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ae0a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae0a-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ae0a-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="6ae0a-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ae0a-125">Namespace</span></span><br/>                | <span data-ttu-id="6ae0a-126">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6ae0a-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6ae0a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6ae0a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ae0a-128"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0a-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ae0a-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ae0a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ae0a-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0a-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae0a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ae0a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae0a-132">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="6ae0a-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





