---
title: Método SetCookieAuthenticationAllowed de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad CookieAuthenticationAllowed.
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- Método SetCookieAuthenticationAllowed Servicios de Escritorio remoto
- Método SetCookieAuthenticationAllowed Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetCookieAuthenticationAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150030"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="708e6-106">Método SetCookieAuthenticationAllowed de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="708e6-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="708e6-107">Establece la propiedad **CookieAuthenticationAllowed** .</span><span class="sxs-lookup"><span data-stu-id="708e6-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="708e6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="708e6-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="708e6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="708e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708e6-110">*Permitido* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="708e6-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708e6-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="708e6-111">Type: **boolean**</span></span>

<span data-ttu-id="708e6-112">Nuevo valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="708e6-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708e6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="708e6-113">Return value</span></span>

<span data-ttu-id="708e6-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="708e6-114">Type: **uint32**</span></span>

<span data-ttu-id="708e6-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="708e6-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="708e6-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="708e6-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="708e6-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="708e6-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="708e6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="708e6-118">Remarks</span></span>

<span data-ttu-id="708e6-119">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="708e6-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="708e6-120">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="708e6-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="708e6-121">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="708e6-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="708e6-122">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="708e6-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="708e6-123">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="708e6-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="708e6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="708e6-124">Requirements</span></span>



| <span data-ttu-id="708e6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="708e6-125">Requirement</span></span> | <span data-ttu-id="708e6-126">Value</span><span class="sxs-lookup"><span data-stu-id="708e6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="708e6-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="708e6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="708e6-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="708e6-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="708e6-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="708e6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="708e6-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="708e6-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="708e6-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="708e6-131">Namespace</span></span><br/>                | <span data-ttu-id="708e6-132">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="708e6-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="708e6-133">MOF</span><span class="sxs-lookup"><span data-stu-id="708e6-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="708e6-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="708e6-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="708e6-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="708e6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="708e6-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="708e6-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="708e6-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="708e6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708e6-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="708e6-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

