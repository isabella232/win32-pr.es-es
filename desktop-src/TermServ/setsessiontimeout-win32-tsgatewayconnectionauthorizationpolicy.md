---
title: Método SetSessionTimeout de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Establece las propiedades SessionTimeout y SessionTimeoutAction.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Método SetSessionTimeout Servicios de Escritorio remoto
- Método SetSessionTimeout Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetSessionTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e544b59ae4fe0b74d0c120e6884ab81743cac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534546"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="f04a0-106">Método SetSessionTimeout de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="f04a0-106">SetSessionTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="f04a0-107">Establece las propiedades **SessionTimeout** y **SessionTimeoutAction** .</span><span class="sxs-lookup"><span data-stu-id="f04a0-107">Sets the **SessionTimeout** and **SessionTimeoutAction** properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04a0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f04a0-108">Syntax</span></span>


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a><span data-ttu-id="f04a0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f04a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04a0-110">*SessionTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f04a0-110">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04a0-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f04a0-111">Type: **uint32**</span></span>

<span data-ttu-id="f04a0-112">Nuevo valor de tiempo de espera, en minutos.</span><span class="sxs-lookup"><span data-stu-id="f04a0-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="f04a0-113">Un valor de 0 significa que no hay tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f04a0-113">A value of 0 means there is no timeout.</span></span>

</dd> <dt>

<span data-ttu-id="f04a0-114">*SessionTimeoutAction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f04a0-114">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f04a0-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f04a0-115">Type: **uint32**</span></span>

<span data-ttu-id="f04a0-116">Especifica la acción que se realizará en caso de que se agote el tiempo de espera de una sesión.</span><span class="sxs-lookup"><span data-stu-id="f04a0-116">Specifies the action to be taken in case of a session timeout.</span></span> <span data-ttu-id="f04a0-117">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="f04a0-117">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="f04a0-118">0</span><span class="sxs-lookup"><span data-stu-id="f04a0-118">0</span></span>
</dt> <dd>

<span data-ttu-id="f04a0-119">Desconecte la sesión.</span><span class="sxs-lookup"><span data-stu-id="f04a0-119">Disconnect the session.</span></span>

</dd> <dt>

<span data-ttu-id="f04a0-120">1</span><span class="sxs-lookup"><span data-stu-id="f04a0-120">1</span></span>
</dt> <dd>

<span data-ttu-id="f04a0-121">Intente volver a autorizar la sesión.</span><span class="sxs-lookup"><span data-stu-id="f04a0-121">Attempt to re-authorize the session.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f04a0-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f04a0-122">Return value</span></span>

<span data-ttu-id="f04a0-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f04a0-123">Type: **uint32**</span></span>

<span data-ttu-id="f04a0-124">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="f04a0-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f04a0-125">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="f04a0-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f04a0-126">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f04a0-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f04a0-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f04a0-127">Remarks</span></span>

<span data-ttu-id="f04a0-128">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="f04a0-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f04a0-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f04a0-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f04a0-130">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f04a0-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f04a0-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="f04a0-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f04a0-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f04a0-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f04a0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f04a0-133">Requirements</span></span>



| <span data-ttu-id="f04a0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f04a0-134">Requirement</span></span> | <span data-ttu-id="f04a0-135">Value</span><span class="sxs-lookup"><span data-stu-id="f04a0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04a0-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f04a0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f04a0-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f04a0-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f04a0-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f04a0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f04a0-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f04a0-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="f04a0-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f04a0-140">Namespace</span></span><br/>                | <span data-ttu-id="f04a0-141">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f04a0-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f04a0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f04a0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f04a0-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f04a0-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f04a0-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f04a0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f04a0-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f04a0-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f04a0-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f04a0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f04a0-147">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="f04a0-147">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

