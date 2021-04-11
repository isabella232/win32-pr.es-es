---
title: Método SetCertificate de la clase Win32_TSGatewayServerSettings
description: Establece el hash del certificado para el enlace HTTPS en el puerto 443 en IIS.
ms.assetid: b5f794bc-17b1-401a-92d8-c9bbe5d0d05f
ms.tgt_platform: multiple
keywords:
- Método SetCertificate Servicios de Escritorio remoto
- Método SetCertificate Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1da7e3abcca671b0c8bf70461c77d56e68cf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151008"
---
# <a name="setcertificate-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d6fbf-106">Método SetCertificate de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="d6fbf-106">SetCertificate method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d6fbf-107">Establece el hash del certificado para el enlace HTTPS en el puerto 443 en IIS.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-107">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fbf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6fbf-108">Syntax</span></span>


```mof
uint32 SetCertificate(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="d6fbf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6fbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6fbf-110">*CertHash* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d6fbf-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fbf-111">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d6fbf-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="d6fbf-112">Nuevo hash de certificado.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-112">The new certificate hash.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6fbf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d6fbf-113">Return value</span></span>

<span data-ttu-id="d6fbf-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6fbf-114">Type: **uint32**</span></span>

<span data-ttu-id="d6fbf-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d6fbf-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d6fbf-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d6fbf-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6fbf-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6fbf-118">Remarks</span></span>

<span data-ttu-id="d6fbf-119">Una vez establecido el hash del certificado con este método, debe llamar al método [**Configure**](configure-win32-tsgatewayserversettings.md) para completar el proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-119">After the certificate hash has been set with this method, you must call the [**Configure**](configure-win32-tsgatewayserversettings.md) method to complete the configuration process.</span></span>

<span data-ttu-id="d6fbf-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d6fbf-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6fbf-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6fbf-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d6fbf-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d6fbf-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6fbf-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d6fbf-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6fbf-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6fbf-125">Requirements</span></span>



| <span data-ttu-id="d6fbf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6fbf-126">Requirement</span></span> | <span data-ttu-id="d6fbf-127">Value</span><span class="sxs-lookup"><span data-stu-id="d6fbf-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fbf-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6fbf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d6fbf-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d6fbf-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d6fbf-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6fbf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d6fbf-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d6fbf-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="d6fbf-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6fbf-132">Namespace</span></span><br/>                | <span data-ttu-id="d6fbf-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d6fbf-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d6fbf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d6fbf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6fbf-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6fbf-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6fbf-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6fbf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6fbf-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6fbf-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d6fbf-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6fbf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fbf-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="d6fbf-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

