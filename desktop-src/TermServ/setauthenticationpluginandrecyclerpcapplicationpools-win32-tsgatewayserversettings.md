---
title: Método SetAuthenticationPluginAndRecycleRpcApplicationPools de la clase Win32_TSGatewayServerSettings
description: Establece el complemento de autenticación actual para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) y recicla los grupos de aplicaciones RPC en IIS.
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- Método SetAuthenticationPluginAndRecycleRpcApplicationPools Servicios de Escritorio remoto
- Método SetAuthenticationPluginAndRecycleRpcApplicationPools Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetAuthenticationPluginAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801688"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="18ca2-106">Método SetAuthenticationPluginAndRecycleRpcApplicationPools de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="18ca2-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="18ca2-107">Establece el complemento de autenticación actual para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) y recicla los grupos de aplicaciones RPC en IIS.</span><span class="sxs-lookup"><span data-stu-id="18ca2-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="18ca2-108">Este método es equivalente a llamar a los métodos [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) y [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) en secuencia.</span><span class="sxs-lookup"><span data-stu-id="18ca2-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ca2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18ca2-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="18ca2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18ca2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ca2-111">*PlugInName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18ca2-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18ca2-112">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="18ca2-112">Type: **string**</span></span>

<span data-ttu-id="18ca2-113">Nombre del complemento de autenticación</span><span class="sxs-lookup"><span data-stu-id="18ca2-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ca2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="18ca2-114">Return value</span></span>

<span data-ttu-id="18ca2-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18ca2-115">Type: **uint32**</span></span>

<span data-ttu-id="18ca2-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="18ca2-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="18ca2-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="18ca2-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="18ca2-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="18ca2-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18ca2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18ca2-119">Remarks</span></span>

<span data-ttu-id="18ca2-120">Al llamar a este método, se desconectan todas las conexiones existentes.</span><span class="sxs-lookup"><span data-stu-id="18ca2-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="18ca2-121">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="18ca2-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="18ca2-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="18ca2-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="18ca2-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="18ca2-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="18ca2-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="18ca2-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="18ca2-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="18ca2-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="18ca2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18ca2-126">Requirements</span></span>



| <span data-ttu-id="18ca2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ca2-127">Requirement</span></span> | <span data-ttu-id="18ca2-128">Value</span><span class="sxs-lookup"><span data-stu-id="18ca2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ca2-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18ca2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="18ca2-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="18ca2-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="18ca2-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18ca2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="18ca2-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18ca2-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="18ca2-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="18ca2-133">Namespace</span></span><br/>                | <span data-ttu-id="18ca2-134">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="18ca2-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="18ca2-135">MOF</span><span class="sxs-lookup"><span data-stu-id="18ca2-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18ca2-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18ca2-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="18ca2-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18ca2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ca2-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ca2-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="18ca2-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="18ca2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ca2-140">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="18ca2-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="18ca2-141">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="18ca2-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="18ca2-142">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="18ca2-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

