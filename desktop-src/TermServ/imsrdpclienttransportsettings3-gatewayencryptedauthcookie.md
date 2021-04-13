---
title: Propiedad GatewayEncryptedAuthCookie de IMsRdpClientTransportSettings3
description: Cookie de autenticación cifrada.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayEncryptedAuthCookie
- Propiedad GatewayEncryptedAuthCookie Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3, propiedad GatewayEncryptedAuthCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359735"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a><span data-ttu-id="a44e8-106">IMsRdpClientTransportSettings3:: GatewayEncryptedAuthCookie (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a44e8-106">IMsRdpClientTransportSettings3::GatewayEncryptedAuthCookie property</span></span>

<span data-ttu-id="a44e8-107">Cookie de autenticación cifrada.</span><span class="sxs-lookup"><span data-stu-id="a44e8-107">The encrypted authentication cookie.</span></span> <span data-ttu-id="a44e8-108">El tamaño de la propiedad se especifica mediante la propiedad [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .</span><span class="sxs-lookup"><span data-stu-id="a44e8-108">The size of the property is specified by the [**GatewayEncryptedAuthCookieSize**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) property.</span></span>

<span data-ttu-id="a44e8-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a44e8-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a44e8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a44e8-110">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a><span data-ttu-id="a44e8-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a44e8-111">Property value</span></span>

<span data-ttu-id="a44e8-112">La nueva cookie de autenticación cifrada.</span><span class="sxs-lookup"><span data-stu-id="a44e8-112">The new encrypted authentication cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="a44e8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a44e8-113">Requirements</span></span>



| <span data-ttu-id="a44e8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a44e8-114">Requirement</span></span> | <span data-ttu-id="a44e8-115">Value</span><span class="sxs-lookup"><span data-stu-id="a44e8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a44e8-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a44e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a44e8-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a44e8-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="a44e8-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a44e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a44e8-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a44e8-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a44e8-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a44e8-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="a44e8-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44e8-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a44e8-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a44e8-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a44e8-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a44e8-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a44e8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a44e8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a44e8-125">**GatewayEncryptedAuthCookieSize**</span><span class="sxs-lookup"><span data-stu-id="a44e8-125">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[<span data-ttu-id="a44e8-126">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="a44e8-126">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





