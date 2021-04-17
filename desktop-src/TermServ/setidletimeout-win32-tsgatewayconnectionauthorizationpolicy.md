---
title: Método SetIdleTimeout de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece la propiedad IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- Método SetIdleTimeout Servicios de Escritorio remoto
- Método SetIdleTimeout Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetIdleTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676955"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="69f98-106">Método SetIdleTimeout de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="69f98-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="69f98-107">Establece la propiedad **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="69f98-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f98-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69f98-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="69f98-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69f98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f98-110">*IdleTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69f98-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f98-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69f98-111">Type: **uint32**</span></span>

<span data-ttu-id="69f98-112">Nuevo valor de tiempo de espera, en minutos.</span><span class="sxs-lookup"><span data-stu-id="69f98-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="69f98-113">Un valor de 0 significa que no hay tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="69f98-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69f98-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69f98-114">Return value</span></span>

<span data-ttu-id="69f98-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69f98-115">Type: **uint32**</span></span>

<span data-ttu-id="69f98-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="69f98-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="69f98-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="69f98-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="69f98-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="69f98-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69f98-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69f98-119">Remarks</span></span>

<span data-ttu-id="69f98-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="69f98-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="69f98-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="69f98-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="69f98-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="69f98-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="69f98-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="69f98-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="69f98-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="69f98-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="69f98-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69f98-125">Requirements</span></span>



| <span data-ttu-id="69f98-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f98-126">Requirement</span></span> | <span data-ttu-id="69f98-127">Value</span><span class="sxs-lookup"><span data-stu-id="69f98-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f98-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69f98-128">Minimum supported client</span></span><br/> | <span data-ttu-id="69f98-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="69f98-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="69f98-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69f98-130">Minimum supported server</span></span><br/> | <span data-ttu-id="69f98-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69f98-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="69f98-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69f98-132">Namespace</span></span><br/>                | <span data-ttu-id="69f98-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="69f98-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="69f98-134">MOF</span><span class="sxs-lookup"><span data-stu-id="69f98-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69f98-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69f98-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="69f98-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69f98-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69f98-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69f98-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="69f98-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="69f98-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f98-139">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="69f98-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

