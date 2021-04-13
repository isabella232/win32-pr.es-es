---
title: Propiedad GatewayPreAuthRequirement de IMsRdpClientTransportSettings2
description: Especifica o recupera la configuración de si la característica de contraseña de un solo tiempo (OTP) de Escritorio remoto puerta de enlace de escritorio remoto está habilitada.
ms.assetid: cc8f7ebb-16ba-45ed-ba66-de4a339946d0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayPreAuthRequirement
- Propiedad GatewayPreAuthRequirement Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayPreAuthRequirement
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.get_GatewayPreAuthRequirement
- IMsRdpClientTransportSettings2.put_GatewayPreAuthRequirement
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 058ca92237a4f9729f526030f5f8a836ce1c739c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535326"
---
# <a name="imsrdpclienttransportsettings2gatewaypreauthrequirement-property"></a><span data-ttu-id="2c037-106">IMsRdpClientTransportSettings2:: GatewayPreAuthRequirement (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2c037-106">IMsRdpClientTransportSettings2::GatewayPreAuthRequirement property</span></span>

<span data-ttu-id="2c037-107">Especifica o recupera la configuración de si la característica de contraseña de un solo tiempo (OTP) de Escritorio remoto puerta de enlace de escritorio remoto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2c037-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) one-time password (OTP) feature is enabled.</span></span>

<span data-ttu-id="2c037-108">Cuando OTP está habilitado, **GatewayPreAuthRequirement** intenta consultar la cookie de OTP desde el almacén de cookies de Internet mediante la propiedad [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) .</span><span class="sxs-lookup"><span data-stu-id="2c037-108">When OTP is enabled, **GatewayPreAuthRequirement** tries to query the OTP cookie from the Internet cookie store by using the [**GatewayPreAuthServerAddr**](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md) property.</span></span> <span data-ttu-id="2c037-109">Si se realiza correctamente, **GatewayPreAuthRequirement** envía la cookie de OTP al servidor de Firewall (como Microsoft Internet Security and Acceleration \[ ISA \] Server) para la autenticación previa.</span><span class="sxs-lookup"><span data-stu-id="2c037-109">If successful, **GatewayPreAuthRequirement** sends the OTP cookie to the firewall server (such as Microsoft Internet Security and Acceleration \[ISA\] server) for pre-authentication.</span></span>

<span data-ttu-id="2c037-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2c037-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c037-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c037-111">Syntax</span></span>


```C++
HRESULT put_GatewayPreAuthRequirement(
  [in]  ULONG ulProxyPreAuthRequirement
);

HRESULT get_GatewayPreAuthRequirement(
  [out] ULONG *pulProxyPreAuthRequirement
);
```



## <a name="property-value"></a><span data-ttu-id="2c037-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2c037-112">Property value</span></span>

<span data-ttu-id="2c037-113">Si se establece en 1, la característica OTP está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2c037-113">If set to 1, the OTP feature is enabled.</span></span> <span data-ttu-id="2c037-114">Si se establece en 0, la característica OTP está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="2c037-114">If set to 0, the OTP feature is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2c037-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2c037-115">Error codes</span></span>

<span data-ttu-id="2c037-116">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c037-116">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c037-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c037-117">Requirements</span></span>



| <span data-ttu-id="2c037-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c037-118">Requirement</span></span> | <span data-ttu-id="2c037-119">Value</span><span class="sxs-lookup"><span data-stu-id="2c037-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c037-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c037-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c037-121">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="2c037-121">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="2c037-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c037-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c037-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c037-123">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="2c037-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2c037-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c037-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c037-125"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="2c037-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c037-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c037-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c037-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="2c037-128">IID</span><span class="sxs-lookup"><span data-stu-id="2c037-128">IID</span></span><br/>                      | <span data-ttu-id="2c037-129">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="2c037-129">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c037-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c037-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c037-131">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="2c037-131">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="2c037-132">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="2c037-132">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





