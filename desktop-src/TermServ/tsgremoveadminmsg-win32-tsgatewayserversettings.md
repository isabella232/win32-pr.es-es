---
title: Método TSGRemoveAdminMsg de la clase Win32_TSGatewayServerSettings
description: Quita el mensaje administrativo del servidor de puerta de enlace. | Método TSGRemoveAdminMsg de la clase Win32_TSGatewayServerSettings
ms.assetid: 36b157de-80ee-46f8-9803-5012cf1d6f5f
ms.tgt_platform: multiple
keywords:
- Método TSGRemoveAdminMsg Servicios de Escritorio remoto
- Método TSGRemoveAdminMsg Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método TSGRemoveAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba9877b9e8704c92eb482876ab69107e116207b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678737"
---
# <a name="tsgremoveadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="5ab4e-107">Método TSGRemoveAdminMsg de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="5ab4e-107">TSGRemoveAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="5ab4e-108">Quita el mensaje administrativo del servidor de puerta de enlace.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab4e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ab4e-109">Syntax</span></span>


```mof
uint32 TSGRemoveAdminMsg();
```



## <a name="parameters"></a><span data-ttu-id="5ab4e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ab4e-110">Parameters</span></span>

<span data-ttu-id="5ab4e-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ab4e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ab4e-112">Return value</span></span>

<span data-ttu-id="5ab4e-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ab4e-113">Type: **uint32**</span></span>

<span data-ttu-id="5ab4e-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5ab4e-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5ab4e-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5ab4e-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab4e-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ab4e-117">Remarks</span></span>

<span data-ttu-id="5ab4e-118">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5ab4e-119">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5ab4e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ab4e-120">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5ab4e-121">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="5ab4e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5ab4e-122">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5ab4e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab4e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ab4e-123">Requirements</span></span>



| <span data-ttu-id="5ab4e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ab4e-124">Requirement</span></span> | <span data-ttu-id="5ab4e-125">Value</span><span class="sxs-lookup"><span data-stu-id="5ab4e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab4e-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ab4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab4e-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ab4e-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5ab4e-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ab4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab4e-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ab4e-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="5ab4e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5ab4e-130">Namespace</span></span><br/>                | <span data-ttu-id="5ab4e-131">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5ab4e-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5ab4e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5ab4e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ab4e-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ab4e-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ab4e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ab4e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ab4e-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ab4e-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5ab4e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ab4e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab4e-137">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="5ab4e-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

