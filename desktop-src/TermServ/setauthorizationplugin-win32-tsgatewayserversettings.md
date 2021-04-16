---
title: Método SetAuthorizationPlugin de la clase Win32_TSGatewayServerSettings
description: Establece el complemento de autorización actual para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 236c9cca-4efc-433a-8f1f-e3044e0588b3
ms.tgt_platform: multiple
keywords:
- Método SetAuthorizationPlugin Servicios de Escritorio remoto
- Método SetAuthorizationPlugin Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetAuthorizationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthorizationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cdb3cb07a7c0a30e84245a2d22e383dea168247
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534558"
---
# <a name="setauthorizationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="cfe69-106">Método SetAuthorizationPlugin de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="cfe69-106">SetAuthorizationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="cfe69-107">Establece el complemento de autorización actual para el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="cfe69-107">Sets the current authorization plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe69-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfe69-108">Syntax</span></span>


```mof
uint32 SetAuthorizationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="cfe69-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfe69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe69-110">*PlugInName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfe69-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe69-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="cfe69-111">Type: **string**</span></span>

<span data-ttu-id="cfe69-112">Nombre del nuevo complemento de autorización actual.</span><span class="sxs-lookup"><span data-stu-id="cfe69-112">The name of the new current authorization plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe69-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfe69-113">Return value</span></span>

<span data-ttu-id="cfe69-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cfe69-114">Type: **uint32**</span></span>

<span data-ttu-id="cfe69-115">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cfe69-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cfe69-116">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="cfe69-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cfe69-117">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cfe69-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfe69-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfe69-118">Remarks</span></span>

<span data-ttu-id="cfe69-119">Debe llamar al método [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) para permitir que el complemento de autorización funcione.</span><span class="sxs-lookup"><span data-stu-id="cfe69-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authorization plug-in to work.</span></span>

<span data-ttu-id="cfe69-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="cfe69-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cfe69-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cfe69-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cfe69-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cfe69-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cfe69-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="cfe69-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cfe69-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cfe69-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfe69-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfe69-125">Requirements</span></span>



| <span data-ttu-id="cfe69-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe69-126">Requirement</span></span> | <span data-ttu-id="cfe69-127">Value</span><span class="sxs-lookup"><span data-stu-id="cfe69-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe69-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfe69-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe69-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cfe69-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cfe69-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfe69-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe69-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfe69-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="cfe69-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cfe69-132">Namespace</span></span><br/>                | <span data-ttu-id="cfe69-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cfe69-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cfe69-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cfe69-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfe69-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfe69-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfe69-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfe69-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfe69-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfe69-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cfe69-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfe69-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe69-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="cfe69-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="cfe69-140">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="cfe69-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 

