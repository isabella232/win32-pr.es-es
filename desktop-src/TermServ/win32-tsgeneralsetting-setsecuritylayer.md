---
title: Método SetSecurityLayer de la clase Win32_TSGeneralSetting
description: El método SetSecurityLayer establece el nivel de seguridad.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Método SetSecurityLayer Servicios de Escritorio remoto
- Método SetSecurityLayer Servicios de Escritorio remoto, clase Win32_TSGeneralSetting
- Win32_TSGeneralSetting de clase Servicios de Escritorio remoto, método SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996491"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="de9b1-106">Método SetSecurityLayer de la \_ clase TSGeneralSetting de Win32</span><span class="sxs-lookup"><span data-stu-id="de9b1-106">SetSecurityLayer method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="de9b1-107">El método **SetSecurityLayer** establece el nivel de seguridad.</span><span class="sxs-lookup"><span data-stu-id="de9b1-107">The **SetSecurityLayer** method sets the security layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9b1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de9b1-108">Syntax</span></span>


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a><span data-ttu-id="de9b1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de9b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de9b1-110">*SecurityLayer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="de9b1-110">*SecurityLayer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de9b1-111">Nivel de seguridad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="de9b1-111">The security layer to set.</span></span> <span data-ttu-id="de9b1-112">Si el nivel de cifrado actual es 1, el valor 2 para *SecurityLayer* no es válido.</span><span class="sxs-lookup"><span data-stu-id="de9b1-112">If the current Encryption Level is 1, then a value of 2 for *SecurityLayer* is not valid.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="de9b1-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Nivel de seguridad de RDP** (0)</span><span class="sxs-lookup"><span data-stu-id="de9b1-113"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (0)</span></span>


</dt> <dd>

<span data-ttu-id="de9b1-114">En las comunicaciones entre servidor y cliente se usará el cifrado RDP nativo.</span><span class="sxs-lookup"><span data-stu-id="de9b1-114">Communication between the server and the client will use native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="de9b1-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span><span class="sxs-lookup"><span data-stu-id="de9b1-115"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="de9b1-116">Se usará la capa más segura que admita el cliente.</span><span class="sxs-lookup"><span data-stu-id="de9b1-116">The most secure layer that is supported by the client will be used.</span></span> <span data-ttu-id="de9b1-117">Si se admite, se usará SSL (TLS 1.0).</span><span class="sxs-lookup"><span data-stu-id="de9b1-117">If supported, SSL (TLS 1.0) will be used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="de9b1-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span><span class="sxs-lookup"><span data-stu-id="de9b1-118"><span id="SSL"></span><span id="ssl"></span>**SSL** (2)</span></span>


</dt> <dd>

<span data-ttu-id="de9b1-119">SSL (TLS 1,0) se usará para la autenticación del servidor, así como para cifrar todos los datos transferidos entre el servidor y el cliente.</span><span class="sxs-lookup"><span data-stu-id="de9b1-119">SSL (TLS 1.0) will be used for server authentication as well as for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="de9b1-120">Esta configuración requiere que el servidor tenga un certificado compatible con SSL.</span><span class="sxs-lookup"><span data-stu-id="de9b1-120">This setting requires the server to have an SSL compatible certificate.</span></span> <span data-ttu-id="de9b1-121">Esta configuración no es compatible con un valor de **MinEncryptionLevel** de 1.</span><span class="sxs-lookup"><span data-stu-id="de9b1-121">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de9b1-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de9b1-122">Return value</span></span>

<span data-ttu-id="de9b1-123">Devuelve SUCCESS si es correcto; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="de9b1-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="de9b1-124">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="de9b1-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="de9b1-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de9b1-125">Remarks</span></span>

<span data-ttu-id="de9b1-126">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="de9b1-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="de9b1-127">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="de9b1-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="de9b1-128">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="de9b1-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="de9b1-129">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="de9b1-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="de9b1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de9b1-130">Requirements</span></span>



| <span data-ttu-id="de9b1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9b1-131">Requirement</span></span> | <span data-ttu-id="de9b1-132">Value</span><span class="sxs-lookup"><span data-stu-id="de9b1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de9b1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de9b1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="de9b1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de9b1-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de9b1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de9b1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="de9b1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de9b1-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de9b1-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="de9b1-137">Namespace</span></span><br/>                | <span data-ttu-id="de9b1-138">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="de9b1-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="de9b1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="de9b1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de9b1-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de9b1-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="de9b1-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de9b1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de9b1-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de9b1-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9b1-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="de9b1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9b1-144">**Win32 \_ TSGeneralSetting**</span><span class="sxs-lookup"><span data-stu-id="de9b1-144">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dt>

[<span data-ttu-id="de9b1-145">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="de9b1-145">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

