---
title: Método InstallRetailPurchaseLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta al por menor.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- Método InstallRetailPurchaseLicenseKeyPack Servicios de Escritorio remoto
- Método InstallRetailPurchaseLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método InstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676632"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="8ffe9-106">Método InstallRetailPurchaseLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="8ffe9-106">InstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="8ffe9-107">Instala un paquete de claves de licencia Servicios de Escritorio remoto adquirido a través de un canal de venta al por menor.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-107">Installs a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffe9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ffe9-108">Syntax</span></span>


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="8ffe9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ffe9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffe9-110">*sLicenseCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8ffe9-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffe9-111">Contiene el código de licencia de 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-111">Contains the 25-character license code.</span></span> <span data-ttu-id="8ffe9-112">Solo se debe proporcionar como entrada la cadena de caracteres alfanuméricos de 25 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="8ffe9-113">No se deben agregar guiones.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="8ffe9-114">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ffe9-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffe9-115">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffe9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ffe9-116">Return value</span></span>

<span data-ttu-id="8ffe9-117">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8ffe9-118">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8ffe9-119">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8ffe9-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffe9-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ffe9-120">Remarks</span></span>

<span data-ttu-id="8ffe9-121">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8ffe9-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8ffe9-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8ffe9-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8ffe9-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8ffe9-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8ffe9-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8ffe9-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffe9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ffe9-126">Requirements</span></span>



| <span data-ttu-id="8ffe9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ffe9-127">Requirement</span></span> | <span data-ttu-id="8ffe9-128">Value</span><span class="sxs-lookup"><span data-stu-id="8ffe9-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffe9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ffe9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffe9-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8ffe9-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8ffe9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ffe9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffe9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ffe9-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8ffe9-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ffe9-133">Namespace</span></span><br/>                | <span data-ttu-id="8ffe9-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8ffe9-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8ffe9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8ffe9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ffe9-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ffe9-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ffe9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ffe9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ffe9-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ffe9-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffe9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ffe9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffe9-140">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="8ffe9-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

