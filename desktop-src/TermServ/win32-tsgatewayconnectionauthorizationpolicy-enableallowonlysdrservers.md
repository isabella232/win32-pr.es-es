---
title: Método EnableAllowOnlySDRServers de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Se usa para alternar la propiedad AllowOnlySDRServers.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Método EnableAllowOnlySDRServers Servicios de Escritorio remoto
- Método EnableAllowOnlySDRServers Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy de clase Servicios de Escritorio remoto, método EnableAllowOnlySDRServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802090"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="771c9-106">Método EnableAllowOnlySDRServers de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32</span><span class="sxs-lookup"><span data-stu-id="771c9-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="771c9-107">Se usa para alternar la propiedad **AllowOnlySDRServers** .</span><span class="sxs-lookup"><span data-stu-id="771c9-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="771c9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="771c9-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="771c9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="771c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771c9-110">*AllowOnlySDRServers* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="771c9-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="771c9-111">Si se establece en **true**, solo se permitirán las conexiones a los servidores RDS de redirección de dispositivos (SDR).</span><span class="sxs-lookup"><span data-stu-id="771c9-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="771c9-112">Si se establece en **false**, se permitirán las conexiones a los servidores RDS anteriores también</span><span class="sxs-lookup"><span data-stu-id="771c9-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771c9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="771c9-113">Return value</span></span>

<span data-ttu-id="771c9-114">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="771c9-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="771c9-115">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="771c9-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="771c9-116">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="771c9-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="771c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="771c9-117">Requirements</span></span>



| <span data-ttu-id="771c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="771c9-118">Requirement</span></span> | <span data-ttu-id="771c9-119">Value</span><span class="sxs-lookup"><span data-stu-id="771c9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="771c9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="771c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="771c9-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="771c9-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="771c9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="771c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="771c9-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="771c9-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="771c9-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="771c9-124">Namespace</span></span><br/>                | <span data-ttu-id="771c9-125">RAÍZ de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="771c9-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="771c9-126">MOF</span><span class="sxs-lookup"><span data-stu-id="771c9-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="771c9-127"><dt>TsGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="771c9-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="771c9-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="771c9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="771c9-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="771c9-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="771c9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="771c9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771c9-131">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="771c9-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





