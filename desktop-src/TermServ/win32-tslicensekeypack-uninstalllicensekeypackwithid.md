---
title: Método UninstallLicenseKeyPackWithId de la clase Win32_TSLicenseKeyPack
description: Desinstala el paquete de claves de licencia de Servicios de Escritorio remoto con el identificador de paquete de claves especificado.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Método UninstallLicenseKeyPackWithId Servicios de Escritorio remoto
- Método UninstallLicenseKeyPackWithId Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método UninstallLicenseKeyPackWithId
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489364"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="3b7bb-106">Método UninstallLicenseKeyPackWithId de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="3b7bb-106">UninstallLicenseKeyPackWithId method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="3b7bb-107">Desinstala el paquete de claves de licencia de Servicios de Escritorio remoto con el identificador de paquete de claves especificado.</span><span class="sxs-lookup"><span data-stu-id="3b7bb-107">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7bb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b7bb-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="3b7bb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b7bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7bb-110">*KeyPackId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b7bb-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b7bb-111">Identificador del paquete de claves que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="3b7bb-111">The identifier of the key pack to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7bb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b7bb-112">Return value</span></span>

<span data-ttu-id="3b7bb-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="3b7bb-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3b7bb-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="3b7bb-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3b7bb-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3b7bb-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7bb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b7bb-116">Requirements</span></span>



| <span data-ttu-id="3b7bb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b7bb-117">Requirement</span></span> | <span data-ttu-id="3b7bb-118">Value</span><span class="sxs-lookup"><span data-stu-id="3b7bb-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7bb-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b7bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7bb-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3b7bb-120">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3b7bb-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b7bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7bb-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b7bb-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3b7bb-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b7bb-123">Namespace</span></span><br/>                | <span data-ttu-id="3b7bb-124">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3b7bb-124">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3b7bb-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3b7bb-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b7bb-126"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b7bb-126"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b7bb-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b7bb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b7bb-128"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b7bb-128"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7bb-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b7bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7bb-130">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="3b7bb-130">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





