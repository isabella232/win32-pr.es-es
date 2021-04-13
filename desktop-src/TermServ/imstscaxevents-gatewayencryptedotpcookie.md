---
title: Propiedad GatewayEncryptedOtpCookie de IMsRdpClientTransportSettings2
description: Especifica o recupera la cookie de contraseña de un solo tiempo cifrada (OTP).
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayEncryptedOtpCookie
- Propiedad GatewayEncryptedOtpCookie Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayEncryptedOtpCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535566"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a><span data-ttu-id="05fd1-106">IMsRdpClientTransportSettings2:: GatewayEncryptedOtpCookie (propiedad)</span><span class="sxs-lookup"><span data-stu-id="05fd1-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookie property</span></span>

<span data-ttu-id="05fd1-107">Especifica o recupera la cookie de contraseña de un solo tiempo cifrada (OTP).</span><span class="sxs-lookup"><span data-stu-id="05fd1-107">Specifies or retrieves the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="05fd1-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="05fd1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="05fd1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05fd1-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a><span data-ttu-id="05fd1-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="05fd1-110">Property value</span></span>

<span data-ttu-id="05fd1-111">Especifica o recupera la cookie de OTP cifrada.</span><span class="sxs-lookup"><span data-stu-id="05fd1-111">Specifies or retrieves the encrypted OTP cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="05fd1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05fd1-112">Requirements</span></span>



| <span data-ttu-id="05fd1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="05fd1-113">Requirement</span></span> | <span data-ttu-id="05fd1-114">Value</span><span class="sxs-lookup"><span data-stu-id="05fd1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05fd1-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05fd1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="05fd1-116">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="05fd1-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="05fd1-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="05fd1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="05fd1-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05fd1-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="05fd1-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="05fd1-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="05fd1-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05fd1-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="05fd1-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="05fd1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05fd1-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05fd1-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="05fd1-123">IID</span><span class="sxs-lookup"><span data-stu-id="05fd1-123">IID</span></span><br/>                      | <span data-ttu-id="05fd1-124">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="05fd1-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05fd1-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="05fd1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05fd1-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="05fd1-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="05fd1-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="05fd1-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





