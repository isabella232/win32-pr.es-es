---
title: Propiedad GatewayAuthLoginPage de IMsRdpClientTransportSettings3
description: Dirección de la Página Web de inicio de sesión que se va a usar para autenticar a un usuario.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayAuthLoginPage
- Propiedad GatewayAuthLoginPage Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3, propiedad GatewayAuthLoginPage
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5be535dea0a89f1cf6e7c238029e53f38f58b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151089"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a><span data-ttu-id="6e1bc-106">IMsRdpClientTransportSettings3:: GatewayAuthLoginPage (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6e1bc-106">IMsRdpClientTransportSettings3::GatewayAuthLoginPage property</span></span>

<span data-ttu-id="6e1bc-107">Dirección de la Página Web de inicio de sesión que se va a usar para autenticar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="6e1bc-107">The address of the login webpage to use to authenticate a user.</span></span>

<span data-ttu-id="6e1bc-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6e1bc-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1bc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e1bc-109">Syntax</span></span>


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a><span data-ttu-id="6e1bc-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6e1bc-110">Property value</span></span>

<span data-ttu-id="6e1bc-111">La nueva dirección de página web de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="6e1bc-111">The new login webpage address.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1bc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e1bc-112">Requirements</span></span>



| <span data-ttu-id="6e1bc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e1bc-113">Requirement</span></span> | <span data-ttu-id="6e1bc-114">Value</span><span class="sxs-lookup"><span data-stu-id="6e1bc-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1bc-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e1bc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1bc-116">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6e1bc-116">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="6e1bc-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e1bc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1bc-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e1bc-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6e1bc-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6e1bc-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="6e1bc-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1bc-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6e1bc-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e1bc-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1bc-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e1bc-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1bc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e1bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1bc-124">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="6e1bc-124">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





