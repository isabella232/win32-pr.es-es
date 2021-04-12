---
title: Propiedad GatewayAuthCookieServerAddr de IMsRdpClientTransportSettings3
description: Dirección del servidor para la autenticación basada en cookies.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayAuthCookieServerAddr
- Propiedad GatewayAuthCookieServerAddr Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3, propiedad GatewayAuthCookieServerAddr
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc238129d0bb9f698e90fc5e1de85e7257a4d16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492934"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a><span data-ttu-id="4a8ce-106">IMsRdpClientTransportSettings3:: GatewayAuthCookieServerAddr (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4a8ce-106">IMsRdpClientTransportSettings3::GatewayAuthCookieServerAddr property</span></span>

<span data-ttu-id="4a8ce-107">Dirección del servidor para la autenticación basada en cookies.</span><span class="sxs-lookup"><span data-stu-id="4a8ce-107">The server address for cookie-based authentication.</span></span>

<span data-ttu-id="4a8ce-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4a8ce-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8ce-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a8ce-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a><span data-ttu-id="4a8ce-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4a8ce-110">Property value</span></span>

<span data-ttu-id="4a8ce-111">La nueva dirección del servidor para la autenticación basada en cookies.</span><span class="sxs-lookup"><span data-stu-id="4a8ce-111">The new server address for cookie-based authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8ce-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a8ce-112">Requirements</span></span>



| <span data-ttu-id="4a8ce-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a8ce-113">Requirement</span></span> | <span data-ttu-id="4a8ce-114">Value</span><span class="sxs-lookup"><span data-stu-id="4a8ce-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8ce-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a8ce-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8ce-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a8ce-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="4a8ce-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a8ce-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8ce-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a8ce-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4a8ce-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4a8ce-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="4a8ce-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a8ce-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a8ce-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4a8ce-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a8ce-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a8ce-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a8ce-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a8ce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8ce-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="4a8ce-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





