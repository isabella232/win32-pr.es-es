---
title: Método SetSecureIdAllowed de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Este método está reservado para un uso futuro.
ms.assetid: 9f49e69a-c004-4e3e-b238-69865e3bf00b
ms.tgt_platform: multiple
keywords:
- Método SetSecureIdAllowed Servicios de Escritorio remoto
- Método SetSecureIdAllowed Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetSecureIdAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSecureIdAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e61c158a7dfcafb6d1d5ac66833e42284b818d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686058"
---
# <a name="setsecureidallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="97734-106">Método SetSecureIdAllowed de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="97734-106">SetSecureIdAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="97734-107">Este método está reservado para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="97734-107">This method is reserved for future use.</span></span>

<span data-ttu-id="97734-108">Establece la propiedad **SecureIdAllowed** , que se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="97734-108">Sets the **SecureIdAllowed** property, which is reserved for future use.</span></span>

## <a name="syntax"></a><span data-ttu-id="97734-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97734-109">Syntax</span></span>


```mof
uint32 SetSecureIdAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="97734-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97734-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97734-111">*Permitido* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97734-111">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97734-112">Nuevo valor de **SecureIdAllowed** .</span><span class="sxs-lookup"><span data-stu-id="97734-112">New **SecureIdAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97734-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97734-113">Return value</span></span>

<span data-ttu-id="97734-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="97734-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="97734-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="97734-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="97734-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="97734-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97734-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97734-117">Remarks</span></span>

<span data-ttu-id="97734-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="97734-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="97734-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="97734-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="97734-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="97734-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="97734-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="97734-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="97734-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="97734-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="97734-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97734-123">Requirements</span></span>



| <span data-ttu-id="97734-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="97734-124">Requirement</span></span> | <span data-ttu-id="97734-125">Value</span><span class="sxs-lookup"><span data-stu-id="97734-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97734-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97734-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97734-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="97734-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="97734-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97734-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97734-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97734-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="97734-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="97734-130">Namespace</span></span><br/>                | <span data-ttu-id="97734-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="97734-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="97734-132">MOF</span><span class="sxs-lookup"><span data-stu-id="97734-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97734-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97734-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="97734-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97734-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97734-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97734-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="97734-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="97734-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97734-137">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="97734-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

