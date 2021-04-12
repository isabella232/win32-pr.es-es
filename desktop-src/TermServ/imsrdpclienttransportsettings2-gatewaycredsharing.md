---
title: Propiedad GatewayCredSharing de IMsRdpClientTransportSettings2
description: Especifica o recupera la configuración de si está habilitada la característica de uso compartido de credenciales de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayCredSharing
- Propiedad GatewayCredSharing Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayCredSharing
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489520"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a><span data-ttu-id="4cdd9-106">IMsRdpClientTransportSettings2:: GatewayCredSharing (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4cdd9-106">IMsRdpClientTransportSettings2::GatewayCredSharing property</span></span>

<span data-ttu-id="4cdd9-107">Especifica o recupera la configuración de si está habilitada la característica de uso compartido de credenciales de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="4cdd9-107">Specifies or retrieves the setting for whether the Remote Desktop Gateway (RD Gateway) credential sharing feature is enabled.</span></span> <span data-ttu-id="4cdd9-108">Cuando la característica está habilitada, el control ActiveX Escritorio remoto intenta usar las mismas credenciales para autenticarse en el servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto) y en el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-108">When the feature is enabled, the Remote Desktop ActiveX control tries to use the same credentials to authenticate to the Remote Desktop Session Host (RD Session Host) server and to the RD Gateway server.</span></span>

<span data-ttu-id="4cdd9-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cdd9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cdd9-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a><span data-ttu-id="4cdd9-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4cdd9-111">Property value</span></span>

<span data-ttu-id="4cdd9-112">Si se establece en uno, se habilita el uso compartido de credenciales.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-112">If set to one, credential sharing is enabled.</span></span> <span data-ttu-id="4cdd9-113">Si se establece en cero, el uso compartido de credenciales está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-113">If set to zero, credential sharing is disabled.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cdd9-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4cdd9-114">Error codes</span></span>

<span data-ttu-id="4cdd9-115">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cdd9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cdd9-116">Remarks</span></span>

<span data-ttu-id="4cdd9-117">El control ActiveX utiliza esta propiedad para implementar un único aviso para el uso compartido de credenciales entre el servidor host de sesión de escritorio remoto y el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="4cdd9-117">This property is used by the ActiveX control to implement a single prompt for credential sharing between the RD Session Host server and the RD Gateway server.</span></span> <span data-ttu-id="4cdd9-118">El uso compartido de credenciales no admite el uso compartido de contraseñas basado en Web con [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) o [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span><span class="sxs-lookup"><span data-stu-id="4cdd9-118">Credential sharing does not support web-based password sharing with [**GatewayPassword**](imsrdpclienttransportsettings2-gatewaypassword.md) or [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4cdd9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cdd9-119">Requirements</span></span>



| <span data-ttu-id="4cdd9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cdd9-120">Requirement</span></span> | <span data-ttu-id="4cdd9-121">Value</span><span class="sxs-lookup"><span data-stu-id="4cdd9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cdd9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cdd9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cdd9-123">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="4cdd9-123">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="4cdd9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4cdd9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cdd9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cdd9-125">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="4cdd9-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4cdd9-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cdd9-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cdd9-127"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4cdd9-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4cdd9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cdd9-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cdd9-129"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4cdd9-130">IID</span><span class="sxs-lookup"><span data-stu-id="4cdd9-130">IID</span></span><br/>                      | <span data-ttu-id="4cdd9-131">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="4cdd9-131">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cdd9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cdd9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cdd9-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="4cdd9-134">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="4cdd9-134">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





