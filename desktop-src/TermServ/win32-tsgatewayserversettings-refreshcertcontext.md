---
title: Método RefreshCertContext de la clase Win32_TSGatewayServerSettings
description: Actualiza el certificado usado por el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: caefeb85-1c7a-4868-9ee8-10ab09354595
ms.tgt_platform: multiple
keywords:
- Método RefreshCertContext Servicios de Escritorio remoto
- Método RefreshCertContext Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método RefreshCertContext
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RefreshCertContext
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b03d77fff9574b0aff577d8ff45b54f57758f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422249"
---
# <a name="refreshcertcontext-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="07de5-106">Método RefreshCertContext de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="07de5-106">RefreshCertContext method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="07de5-107">Actualiza el certificado usado por el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="07de5-107">Refreshes the certificate that is used by the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="07de5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07de5-108">Syntax</span></span>


```mof
uint32 RefreshCertContext(
  [in] uint8 CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="07de5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07de5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07de5-110">*CertHash* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="07de5-110">*CertHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07de5-111">Hash del certificado utilizado por el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="07de5-111">Hash of the certificate that is used by the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07de5-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07de5-112">Return value</span></span>

<span data-ttu-id="07de5-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="07de5-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="07de5-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="07de5-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="07de5-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="07de5-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07de5-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07de5-116">Remarks</span></span>

<span data-ttu-id="07de5-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="07de5-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="07de5-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="07de5-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="07de5-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="07de5-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="07de5-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="07de5-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="07de5-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="07de5-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="07de5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07de5-122">Requirements</span></span>



| <span data-ttu-id="07de5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="07de5-123">Requirement</span></span> | <span data-ttu-id="07de5-124">Value</span><span class="sxs-lookup"><span data-stu-id="07de5-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07de5-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07de5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="07de5-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="07de5-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="07de5-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07de5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="07de5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07de5-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="07de5-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="07de5-129">Namespace</span></span><br/>                | <span data-ttu-id="07de5-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="07de5-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="07de5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="07de5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07de5-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07de5-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="07de5-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07de5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07de5-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07de5-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="07de5-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="07de5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07de5-136">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="07de5-136">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

