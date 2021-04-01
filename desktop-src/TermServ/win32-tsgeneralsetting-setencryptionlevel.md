---
title: SetEncryptionLevel method of the Win32_TSGeneralSetting class (Establecer el método SetEncryptionLevel de la clase Win32_TSGeneralSetting)
description: El método SetEncryptionLevel establece el nivel de cifrado.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Método SetEncryptionLevel Servicios de Escritorio remoto
- Método SetEncryptionLevel Servicios de Escritorio remoto, clase Win32_TSGeneralSetting
- Win32_TSGeneralSetting de clase Servicios de Escritorio remoto, método SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150591"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="d0904-106">Método SetEncryptionLevel de la \_ clase TSGeneralSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="d0904-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="d0904-107">El método **SetEncryptionLevel** establece el nivel de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d0904-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0904-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0904-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="d0904-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0904-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0904-110">*MinEncryptionLevel* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d0904-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0904-111">Nivel mínimo de cifrado que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="d0904-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="d0904-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="d0904-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="d0904-113">Bajo nivel de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d0904-113">Low level of encryption.</span></span> <span data-ttu-id="d0904-114">Solo los datos enviados desde el cliente al servidor se cifran mediante el cifrado de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="d0904-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="d0904-115">Tenga en cuenta que no se cifran los datos enviados desde el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="d0904-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="d0904-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="d0904-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="d0904-117">Nivel de cifrado compatible con el cliente.</span><span class="sxs-lookup"><span data-stu-id="d0904-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="d0904-118">Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran con el nivel de clave máximo admitido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d0904-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="d0904-119"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="d0904-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="d0904-120">Alto nivel de cifrado.</span><span class="sxs-lookup"><span data-stu-id="d0904-120">High level of encryption.</span></span> <span data-ttu-id="d0904-121">Todos los datos enviados del cliente al servidor y del servidor al cliente se cifran mediante cifrado de 128 bits seguro.</span><span class="sxs-lookup"><span data-stu-id="d0904-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="d0904-122">Los clientes que no admiten este nivel de cifrado no se pueden conectar.</span><span class="sxs-lookup"><span data-stu-id="d0904-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="d0904-123"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="d0904-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="d0904-124">Cifrado compatible con FIPS.</span><span class="sxs-lookup"><span data-stu-id="d0904-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="d0904-125">Todos los datos enviados del cliente al servidor y del servidor al cliente están cifrados y descifrados con los algoritmos de cifrado de Estándar federal de procesamiento de información (FIPS) mediante los módulos criptográficos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d0904-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="d0904-126">FIPS es un estándar titulado "requisitos de seguridad para los módulos criptográficos".</span><span class="sxs-lookup"><span data-stu-id="d0904-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="d0904-127">FIPS 140-1 (1994) y FIPS 140-2 (2001) describen los requisitos gubernamentales para los módulos criptográficos de hardware y software que se usan en el gobierno de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="d0904-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0904-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0904-128">Return value</span></span>

<span data-ttu-id="d0904-129">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="d0904-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d0904-130">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="d0904-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0904-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0904-131">Remarks</span></span>

<span data-ttu-id="d0904-132">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d0904-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d0904-133">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d0904-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d0904-134">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d0904-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d0904-135">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d0904-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0904-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0904-136">Requirements</span></span>



| <span data-ttu-id="d0904-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0904-137">Requirement</span></span> | <span data-ttu-id="d0904-138">Value</span><span class="sxs-lookup"><span data-stu-id="d0904-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0904-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0904-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d0904-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0904-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0904-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0904-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d0904-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0904-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0904-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0904-143">Namespace</span></span><br/>                | <span data-ttu-id="d0904-144">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d0904-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d0904-145">MOF</span><span class="sxs-lookup"><span data-stu-id="d0904-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0904-146"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0904-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0904-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0904-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0904-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0904-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0904-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0904-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0904-150">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="d0904-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

