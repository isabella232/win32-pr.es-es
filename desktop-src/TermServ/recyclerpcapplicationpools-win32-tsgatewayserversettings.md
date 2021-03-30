---
title: Método RecycleRpcApplicationPools de la clase Win32_TSGatewayServerSettings
description: Recicla los grupos de aplicaciones RPC en IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- Método RecycleRpcApplicationPools Servicios de Escritorio remoto
- Método RecycleRpcApplicationPools Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método RecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490318"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="123b1-106">Método RecycleRpcApplicationPools de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="123b1-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="123b1-107">Recicla los grupos de aplicaciones RPC en IIS.</span><span class="sxs-lookup"><span data-stu-id="123b1-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="123b1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="123b1-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="123b1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="123b1-109">Parameters</span></span>

<span data-ttu-id="123b1-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="123b1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="123b1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="123b1-111">Return value</span></span>

<span data-ttu-id="123b1-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="123b1-112">Type: **uint32**</span></span>

<span data-ttu-id="123b1-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="123b1-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="123b1-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="123b1-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="123b1-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="123b1-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="123b1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="123b1-116">Remarks</span></span>

<span data-ttu-id="123b1-117">Al llamar a este método, se desconectan todas las conexiones existentes.</span><span class="sxs-lookup"><span data-stu-id="123b1-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="123b1-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="123b1-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="123b1-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="123b1-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="123b1-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="123b1-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="123b1-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="123b1-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="123b1-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="123b1-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="123b1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="123b1-123">Requirements</span></span>



| <span data-ttu-id="123b1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="123b1-124">Requirement</span></span> | <span data-ttu-id="123b1-125">Value</span><span class="sxs-lookup"><span data-stu-id="123b1-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="123b1-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123b1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="123b1-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="123b1-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="123b1-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123b1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="123b1-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="123b1-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="123b1-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="123b1-130">Namespace</span></span><br/>                | <span data-ttu-id="123b1-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="123b1-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="123b1-132">MOF</span><span class="sxs-lookup"><span data-stu-id="123b1-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="123b1-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="123b1-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="123b1-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="123b1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123b1-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123b1-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="123b1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="123b1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123b1-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="123b1-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="123b1-138">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="123b1-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 

