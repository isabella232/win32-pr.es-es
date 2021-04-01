---
title: Método InstallLicenseKeyPack de la clase Win32_TSLicenseKeyPack
description: Instala un paquete de claves de licencia Servicios de Escritorio remoto que usa el identificador de licencia que se recibió a través de Internet o el teléfono.
ms.assetid: 1e545186-cc01-4700-857f-9390e1b73923
ms.tgt_platform: multiple
keywords:
- Método InstallLicenseKeyPack Servicios de Escritorio remoto
- Método InstallLicenseKeyPack Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método InstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bee5e03de19783a20eeafa3f652dd60b99e871c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996075"
---
# <a name="installlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="d9a6a-106">Método InstallLicenseKeyPack de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="d9a6a-106">InstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="d9a6a-107">Instala un paquete de claves de licencia Servicios de Escritorio remoto que usa el identificador de licencia que se recibió a través de Internet o el teléfono.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-107">Installs a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a6a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9a6a-108">Syntax</span></span>


```mof
uint32 InstallLicenseKeyPack(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="d9a6a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9a6a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9a6a-110">*sLicenseKeyPackId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9a6a-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a6a-111">Contiene el código de licencia de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-111">Contains the 35-character license code.</span></span> <span data-ttu-id="d9a6a-112">Solo se debe proporcionar como entrada la cadena de caracteres alfanuméricos de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="d9a6a-113">No se deben agregar guiones.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="d9a6a-114">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d9a6a-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9a6a-115">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9a6a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9a6a-116">Return value</span></span>

<span data-ttu-id="d9a6a-117">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d9a6a-118">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d9a6a-119">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d9a6a-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9a6a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9a6a-120">Remarks</span></span>

<span data-ttu-id="d9a6a-121">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d9a6a-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d9a6a-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d9a6a-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d9a6a-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d9a6a-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d9a6a-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d9a6a-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a6a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9a6a-126">Requirements</span></span>



| <span data-ttu-id="d9a6a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9a6a-127">Requirement</span></span> | <span data-ttu-id="d9a6a-128">Value</span><span class="sxs-lookup"><span data-stu-id="d9a6a-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a6a-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9a6a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a6a-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d9a6a-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d9a6a-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9a6a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a6a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9a6a-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d9a6a-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9a6a-133">Namespace</span></span><br/>                | <span data-ttu-id="d9a6a-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d9a6a-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d9a6a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d9a6a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9a6a-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9a6a-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9a6a-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9a6a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a6a-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9a6a-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a6a-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9a6a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a6a-140">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="d9a6a-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

