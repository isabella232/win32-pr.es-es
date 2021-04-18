---
title: Método SetPasswordAllowed de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad PasswordAllowed, que habilita o deshabilita la compatibilidad con el uso de una contraseña para conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- Método SetPasswordAllowed Servicios de Escritorio remoto
- Método SetPasswordAllowed Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetPasswordAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422567"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="4bfd0-106">Método SetPasswordAllowed de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="4bfd0-106">SetPasswordAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="4bfd0-107">Establece la propiedad **PasswordAllowed** , que habilita o deshabilita la compatibilidad con el uso de una contraseña para conectarse al servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-107">Sets the **PasswordAllowed** property, which enables or disables support for using a password to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bfd0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bfd0-108">Syntax</span></span>


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="4bfd0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bfd0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bfd0-110">*Permitido* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4bfd0-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bfd0-111">Nuevo valor de **PasswordAllowed** .</span><span class="sxs-lookup"><span data-stu-id="4bfd0-111">New **PasswordAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bfd0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bfd0-112">Return value</span></span>

<span data-ttu-id="4bfd0-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4bfd0-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4bfd0-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4bfd0-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bfd0-116">Remarks</span></span>

<span data-ttu-id="4bfd0-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4bfd0-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4bfd0-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4bfd0-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="4bfd0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4bfd0-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4bfd0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfd0-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bfd0-122">Requirements</span></span>



| <span data-ttu-id="4bfd0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bfd0-123">Requirement</span></span> | <span data-ttu-id="4bfd0-124">Value</span><span class="sxs-lookup"><span data-stu-id="4bfd0-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfd0-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bfd0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfd0-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4bfd0-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4bfd0-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bfd0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfd0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bfd0-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4bfd0-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4bfd0-129">Namespace</span></span><br/>                | <span data-ttu-id="4bfd0-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4bfd0-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4bfd0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4bfd0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bfd0-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bfd0-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bfd0-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bfd0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bfd0-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bfd0-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4bfd0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bfd0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfd0-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="4bfd0-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

