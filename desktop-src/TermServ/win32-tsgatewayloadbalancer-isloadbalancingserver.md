---
title: Método IsLoadBalancingServer de la clase Win32_TSGatewayLoadBalancer
description: Determina si el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) puede realizar el equilibrio de carga.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Método IsLoadBalancingServer Servicios de Escritorio remoto
- Método IsLoadBalancingServer Servicios de Escritorio remoto, clase Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer de clase Servicios de Escritorio remoto, método IsLoadBalancingServer
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686052"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="2e6b3-106">Método IsLoadBalancingServer de la \_ clase TSGatewayLoadBalancer de Win32</span><span class="sxs-lookup"><span data-stu-id="2e6b3-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="2e6b3-107">Determina si el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto) puede realizar el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6b3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e6b3-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="2e6b3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e6b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e6b3-110">*Equilibrio* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e6b3-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e6b3-111">**True** si el servidor puede realizar el equilibrio de carga y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e6b3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e6b3-112">Return value</span></span>

<span data-ttu-id="2e6b3-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2e6b3-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2e6b3-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2e6b3-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e6b3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e6b3-116">Remarks</span></span>

<span data-ttu-id="2e6b3-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2e6b3-118">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2e6b3-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2e6b3-119">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2e6b3-120">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2e6b3-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2e6b3-121">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2e6b3-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e6b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e6b3-122">Requirements</span></span>



| <span data-ttu-id="2e6b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6b3-123">Requirement</span></span> | <span data-ttu-id="2e6b3-124">Value</span><span class="sxs-lookup"><span data-stu-id="2e6b3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6b3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6b3-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e6b3-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2e6b3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e6b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6b3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e6b3-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2e6b3-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e6b3-129">Namespace</span></span><br/>                | <span data-ttu-id="2e6b3-130">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2e6b3-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2e6b3-131">MOF</span><span class="sxs-lookup"><span data-stu-id="2e6b3-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e6b3-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e6b3-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e6b3-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e6b3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e6b3-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e6b3-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2e6b3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e6b3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6b3-136">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="2e6b3-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

