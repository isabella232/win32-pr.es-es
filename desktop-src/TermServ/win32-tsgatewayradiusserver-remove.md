---
title: Método Remove de la clase Win32_TSGatewayRADIUSServer
description: Quita el servidor de Servicio de autenticación remota telefónica de usuario (RADIUS) actual.
ms.assetid: 915f6d38-ba6a-4994-8bb9-bfddb9aa6ff8
ms.tgt_platform: multiple
keywords:
- Quitar método Servicios de Escritorio remoto
- Quitar Servicios de Escritorio remoto de método, Win32_TSGatewayRADIUSServer interfaz
- Win32_TSGatewayRADIUSServer Servicios de Escritorio remoto de interfaz, Remove (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Remove
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a91fc4a3ba8bf638dcffd76e3bf3517795674fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359819"
---
# <a name="remove-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="e64e0-106">Método Remove de la \_ clase Win32 TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="e64e0-106">Remove method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="e64e0-107">Quita el servidor de Servicio de autenticación remota telefónica de usuario (RADIUS) actual.</span><span class="sxs-lookup"><span data-stu-id="e64e0-107">Removes the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64e0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e64e0-108">Syntax</span></span>


```mof
uint32 Remove();
```



## <a name="parameters"></a><span data-ttu-id="e64e0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e64e0-109">Parameters</span></span>

<span data-ttu-id="e64e0-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e64e0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e64e0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e64e0-111">Return value</span></span>

<span data-ttu-id="e64e0-112">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e64e0-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e64e0-113">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="e64e0-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e64e0-114">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e64e0-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e64e0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e64e0-115">Remarks</span></span>

<span data-ttu-id="e64e0-116">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="e64e0-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e64e0-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e64e0-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e64e0-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e64e0-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e64e0-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="e64e0-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e64e0-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e64e0-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e64e0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e64e0-121">Requirements</span></span>



| <span data-ttu-id="e64e0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e64e0-122">Requirement</span></span> | <span data-ttu-id="e64e0-123">Value</span><span class="sxs-lookup"><span data-stu-id="e64e0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e64e0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e64e0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e64e0-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e64e0-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e64e0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e64e0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e64e0-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e64e0-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e64e0-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e64e0-128">Namespace</span></span><br/>                | <span data-ttu-id="e64e0-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e64e0-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e64e0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e64e0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e64e0-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e64e0-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e64e0-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e64e0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e64e0-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e64e0-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e64e0-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e64e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64e0-135">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="e64e0-135">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 

