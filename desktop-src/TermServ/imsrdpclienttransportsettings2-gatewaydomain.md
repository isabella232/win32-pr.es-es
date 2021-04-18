---
title: Propiedad GatewayDomain de IMsRdpClientTransportSettings2
description: Especifica o recupera el nombre de dominio de un usuario que se proporciona al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayDomain
- Propiedad GatewayDomain Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayDomain
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422067"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="df972-106">IMsRdpClientTransportSettings2:: GatewayDomain (propiedad)</span><span class="sxs-lookup"><span data-stu-id="df972-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="df972-107">Especifica o recupera el nombre de dominio de un usuario que se proporciona al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="df972-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="df972-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="df972-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="df972-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df972-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="df972-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="df972-110">Property value</span></span>

<span data-ttu-id="df972-111">El nombre de dominio que se proporciona para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="df972-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df972-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="df972-112">Error codes</span></span>

<span data-ttu-id="df972-113">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="df972-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="df972-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df972-114">Requirements</span></span>



| <span data-ttu-id="df972-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="df972-115">Requirement</span></span> | <span data-ttu-id="df972-116">Value</span><span class="sxs-lookup"><span data-stu-id="df972-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df972-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df972-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df972-118">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="df972-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="df972-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df972-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df972-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df972-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="df972-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="df972-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="df972-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df972-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="df972-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df972-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df972-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df972-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="df972-125">IID</span><span class="sxs-lookup"><span data-stu-id="df972-125">IID</span></span><br/>                      | <span data-ttu-id="df972-126">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="df972-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df972-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="df972-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df972-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="df972-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="df972-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="df972-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





