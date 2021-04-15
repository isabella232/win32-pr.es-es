---
title: Método ConvertLicenses de la clase Win32_TSLicenseKeyPack
description: Convierte las licencias en el paquete de claves actual.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Método ConvertLicenses Servicios de Escritorio remoto
- Método ConvertLicenses Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422024"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="337c3-106">Método ConvertLicenses de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="337c3-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="337c3-107">Convierte las licencias en el paquete de claves actual.</span><span class="sxs-lookup"><span data-stu-id="337c3-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="337c3-108">Si se trata de una licencia por usuario, se convierte en una licencia por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="337c3-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="337c3-109">Si la licencia es una licencia por dispositivo, se convierte en una licencia por usuario.</span><span class="sxs-lookup"><span data-stu-id="337c3-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="337c3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="337c3-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="337c3-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="337c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337c3-112">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="337c3-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="337c3-113">El número de licencias que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="337c3-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="337c3-114">*KeypackID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="337c3-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="337c3-115">Identificador del paquete de claves resultante.</span><span class="sxs-lookup"><span data-stu-id="337c3-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337c3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="337c3-116">Return value</span></span>

<span data-ttu-id="337c3-117">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="337c3-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="337c3-118">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="337c3-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="337c3-119">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="337c3-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="337c3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="337c3-120">Requirements</span></span>



| <span data-ttu-id="337c3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="337c3-121">Requirement</span></span> | <span data-ttu-id="337c3-122">Value</span><span class="sxs-lookup"><span data-stu-id="337c3-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="337c3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="337c3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="337c3-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="337c3-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="337c3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="337c3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="337c3-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="337c3-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="337c3-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="337c3-127">Namespace</span></span><br/>                | <span data-ttu-id="337c3-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="337c3-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="337c3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="337c3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="337c3-130"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="337c3-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="337c3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="337c3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="337c3-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="337c3-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337c3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="337c3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337c3-134">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="337c3-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





