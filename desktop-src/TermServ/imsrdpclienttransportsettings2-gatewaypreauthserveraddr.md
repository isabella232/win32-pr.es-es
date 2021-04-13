---
title: Propiedad GatewayPreAuthServerAddr de IMsRdpClientTransportSettings2
description: Especifica o recupera la dirección web del servidor de autenticación previa, que se usa para la característica de contraseña de un solo uso (OTP) de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 14edad82-ab19-46fe-b878-d34298763c56
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayPreAuthServerAddr
- Propiedad GatewayPreAuthServerAddr Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayPreAuthServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.get_GatewayPreAuthServerAddr
- IMsRdpClientTransportSettings2.put_GatewayPreAuthServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d6fe2f397b0d445a6300d68a89b210debd449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422066"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthserveraddr-property"></a><span data-ttu-id="8a9d5-106">IMsRdpClientTransportSettings2:: GatewayPreAuthServerAddr (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8a9d5-106">IMsRdpClientTransportSettings2::GatewayPreAuthServerAddr property</span></span>

<span data-ttu-id="8a9d5-107">Especifica o recupera la dirección web del servidor de autenticación previa, que se usa para la característica de contraseña de un solo uso (OTP) de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="8a9d5-107">Specifies or retrieves the web address of the pre-authentication server, which is used for the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature.</span></span>

<span data-ttu-id="8a9d5-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8a9d5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a9d5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a9d5-109">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthServerAddr(
  [in]  BSTR bstrProxyPreAuthServerAddr
);

HRESULT get_GatewayPreAuthServerAddr(
  [out] BSTR *pbstrProxyPreAuthServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="8a9d5-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a9d5-110">Property value</span></span>

<span data-ttu-id="8a9d5-111">Dirección web del servidor de autenticación previa; por ejemplo, la dirección web del servidor Microsoft Internet Security and Acceleration (ISA).</span><span class="sxs-lookup"><span data-stu-id="8a9d5-111">The web address of the pre-authentication server; for example, the web address of the Microsoft Internet Security and Acceleration (ISA) server.</span></span> <span data-ttu-id="8a9d5-112">Especifique la dirección web con el formato "https://*hostname*. *Domainname*. com/*WebsiteName*"o" https://*hostname*. *Domainname*. com/*WebsiteName*".</span><span class="sxs-lookup"><span data-stu-id="8a9d5-112">Specify the web address by using the format "https://*HostName*.*DomainName*.com/*WebsiteName*" or "https://*HostName*.*DomainName*.com/*WebsiteName*".</span></span>

## <a name="error-codes"></a><span data-ttu-id="8a9d5-113">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8a9d5-113">Error codes</span></span>

<span data-ttu-id="8a9d5-114">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a9d5-114">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a9d5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a9d5-115">Requirements</span></span>



| <span data-ttu-id="8a9d5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a9d5-116">Requirement</span></span> | <span data-ttu-id="8a9d5-117">Value</span><span class="sxs-lookup"><span data-stu-id="8a9d5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9d5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a9d5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8a9d5-119">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="8a9d5-119">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="8a9d5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a9d5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8a9d5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a9d5-121">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="8a9d5-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8a9d5-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a9d5-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a9d5-123"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8a9d5-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a9d5-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a9d5-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a9d5-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8a9d5-126">IID</span><span class="sxs-lookup"><span data-stu-id="8a9d5-126">IID</span></span><br/>                      | <span data-ttu-id="8a9d5-127">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="8a9d5-127">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a9d5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a9d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a9d5-129">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="8a9d5-129">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="8a9d5-130">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="8a9d5-130">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





