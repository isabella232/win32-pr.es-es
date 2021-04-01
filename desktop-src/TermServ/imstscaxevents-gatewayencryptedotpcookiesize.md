---
title: Propiedad GatewayEncryptedOtpCookieSize de IMsRdpClientTransportSettings2
description: Especifica o recupera el tamaño de la cookie de contraseña de un solo tiempo cifrada (OTP).
ms.assetid: a4fdcd06-59ae-407f-9ac6-dfe4b52fb5d7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayEncryptedOtpCookieSize
- Propiedad GatewayEncryptedOtpCookieSize Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayEncryptedOtpCookieSize
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookieSize
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e714b7c03e898b29b1ae02e3b19d65fde8dfcb91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802155"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookiesize-property"></a><span data-ttu-id="f406e-106">IMsRdpClientTransportSettings2:: GatewayEncryptedOtpCookieSize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f406e-106">IMsRdpClientTransportSettings2::GatewayEncryptedOtpCookieSize property</span></span>

<span data-ttu-id="f406e-107">Especifica o recupera el tamaño de la cookie de contraseña de un solo tiempo cifrada (OTP).</span><span class="sxs-lookup"><span data-stu-id="f406e-107">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

<span data-ttu-id="f406e-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f406e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f406e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f406e-109">Syntax</span></span>


```C++
HRESULT put_GatewayEncryptedOtpCookieSize(
  [in]  ULONG ulEncryptedOtpCookieSize
);

HRESULT get_GatewayEncryptedOtpCookieSize(
  [out] ULONG *pulEncryptedOtpCookieSize
);
```



## <a name="property-value"></a><span data-ttu-id="f406e-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f406e-110">Property value</span></span>

<span data-ttu-id="f406e-111">Especifica o recupera el tamaño de la cookie de contraseña de un solo tiempo cifrada (OTP).</span><span class="sxs-lookup"><span data-stu-id="f406e-111">Specifies or retrieves the size of the encrypted one-time password (OTP) cookie.</span></span>

## <a name="requirements"></a><span data-ttu-id="f406e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f406e-112">Requirements</span></span>



| <span data-ttu-id="f406e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f406e-113">Requirement</span></span> | <span data-ttu-id="f406e-114">Value</span><span class="sxs-lookup"><span data-stu-id="f406e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f406e-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f406e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f406e-116">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="f406e-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="f406e-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f406e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f406e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f406e-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="f406e-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f406e-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f406e-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f406e-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="f406e-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f406e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f406e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f406e-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="f406e-123">IID</span><span class="sxs-lookup"><span data-stu-id="f406e-123">IID</span></span><br/>                      | <span data-ttu-id="f406e-124">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="f406e-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f406e-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f406e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f406e-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="f406e-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="f406e-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="f406e-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





