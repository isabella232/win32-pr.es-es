---
title: Método DeleteAllServers de la clase Win32_TSGatewayLoadBalancer
description: Elimina Escritorio remoto todos los servidores de equilibrio de carga de puerta de enlace de escritorio remoto que participan en la granja de equilibrio de carga.
ms.assetid: 091ed866-8f2b-47b8-990b-e9a6d7e1194c
ms.tgt_platform: multiple
keywords:
- Método DeleteAllServers Servicios de Escritorio remoto
- Método DeleteAllServers Servicios de Escritorio remoto, clase Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de clase Servicios de Escritorio remoto, método DeleteAllServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteAllServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8004b4cfe811394acb328938775fcc9947bbbd19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533838"
---
# <a name="deleteallservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="fbbb6-106">Método DeleteAllServers de la \_ clase TSGatewayLoadBalancer de Win32</span><span class="sxs-lookup"><span data-stu-id="fbbb6-106">DeleteAllServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="fbbb6-107">Elimina Escritorio remoto todos los servidores de equilibrio de carga de puerta de enlace de escritorio remoto que participan en la granja de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-107">Deletes all Remote Desktop Gateway (RD Gateway) load-balancing servers that are participating in the load-balancing farm.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbbb6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbbb6-108">Syntax</span></span>


```mof
uint32 DeleteAllServers();
```



## <a name="parameters"></a><span data-ttu-id="fbbb6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbbb6-109">Parameters</span></span>

<span data-ttu-id="fbbb6-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fbbb6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbbb6-111">Return value</span></span>

<span data-ttu-id="fbbb6-112">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fbbb6-113">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fbbb6-114">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fbbb6-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fbbb6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbbb6-115">Remarks</span></span>

<span data-ttu-id="fbbb6-116">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fbbb6-117">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fbbb6-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fbbb6-118">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fbbb6-119">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fbbb6-120">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fbbb6-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbbb6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbbb6-121">Requirements</span></span>



| <span data-ttu-id="fbbb6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbbb6-122">Requirement</span></span> | <span data-ttu-id="fbbb6-123">Value</span><span class="sxs-lookup"><span data-stu-id="fbbb6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbb6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbbb6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fbbb6-125">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fbbb6-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fbbb6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbbb6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fbbb6-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbbb6-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fbbb6-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fbbb6-128">Namespace</span></span><br/>                | <span data-ttu-id="fbbb6-129">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fbbb6-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fbbb6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="fbbb6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbbb6-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbbb6-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbbb6-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbbb6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbbb6-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbbb6-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fbbb6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbbb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbb6-135">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="fbbb6-135">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

