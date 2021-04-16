---
title: Método ImportLicenseKeyPackOffline de la clase Win32_TSLicenseKeyPack
description: Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que utiliza un identificador de licencia recibido a través de Internet o del teléfono.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Método ImportLicenseKeyPackOffline Servicios de Escritorio remoto
- Método ImportLicenseKeyPackOffline Servicios de Escritorio remoto, clase Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack de clase Servicios de Escritorio remoto, método ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534257"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e3ba6-106">Método ImportLicenseKeyPackOffline de la \_ clase TSLicenseKeyPack de Win32</span><span class="sxs-lookup"><span data-stu-id="e3ba6-106">ImportLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e3ba6-107">Importa, desde otro servidor de licencias de Escritorio remoto, un paquete de claves de licencia de Servicios de Escritorio remoto que utiliza un identificador de licencia recibido a través de Internet o del teléfono.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ba6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3ba6-108">Syntax</span></span>


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="e3ba6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3ba6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ba6-110">*sLicenseKeyPackId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3ba6-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ba6-111">Contiene el código de licencia de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-111">Contains the 35-character license code.</span></span> <span data-ttu-id="e3ba6-112">Solo se debe proporcionar como entrada la cadena de caracteres alfanuméricos de 35 caracteres.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="e3ba6-113">No se deben agregar guiones.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="e3ba6-114">*sSourceLSName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3ba6-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ba6-115">Nombre del servidor de licencias de origen Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="e3ba6-116">Este es el nombre completo completo o la dirección IP del servidor.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="e3ba6-117">*sSourceLSProductId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3ba6-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ba6-118">Identificador del servidor de licencias Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="e3ba6-119">Es una cadena alfanumérica de 35 caracteres que no puede incluir guiones.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="e3ba6-120">*KeyPackId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3ba6-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ba6-121">Recibe el identificador del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ba6-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3ba6-122">Return value</span></span>

<span data-ttu-id="e3ba6-123">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e3ba6-124">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e3ba6-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e3ba6-125">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e3ba6-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ba6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3ba6-126">Requirements</span></span>



| <span data-ttu-id="e3ba6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ba6-127">Requirement</span></span> | <span data-ttu-id="e3ba6-128">Value</span><span class="sxs-lookup"><span data-stu-id="e3ba6-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ba6-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3ba6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ba6-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e3ba6-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e3ba6-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3ba6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ba6-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3ba6-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e3ba6-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e3ba6-133">Namespace</span></span><br/>                | <span data-ttu-id="e3ba6-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e3ba6-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e3ba6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e3ba6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3ba6-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3ba6-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3ba6-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3ba6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3ba6-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3ba6-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ba6-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3ba6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ba6-140">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="e3ba6-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





