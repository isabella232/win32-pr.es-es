---
title: Propiedad GatewaySupportUrl de IMsRdpClientTransportSettings2
description: Especifica o recupera la dirección web del sitio que proporciona soporte técnico para este servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewaySupportUrl
- Propiedad GatewaySupportUrl Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewaySupportUrl
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4212dd03d5fb217753e14c2869973bda87476367
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422065"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a><span data-ttu-id="47626-106">IMsRdpClientTransportSettings2:: GatewaySupportUrl (propiedad)</span><span class="sxs-lookup"><span data-stu-id="47626-106">IMsRdpClientTransportSettings2::GatewaySupportUrl property</span></span>

<span data-ttu-id="47626-107">Especifica o recupera la dirección web del sitio que proporciona soporte técnico para este servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="47626-107">Specifies or retrieves the web address of the site that provides technical support for this Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="47626-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="47626-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47626-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47626-109">Syntax</span></span>


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a><span data-ttu-id="47626-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="47626-110">Property value</span></span>

<span data-ttu-id="47626-111">Especifica o recupera la dirección web del sitio que proporciona soporte técnico para este servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="47626-111">Specifies or retrieves the web address of the site that provides technical support for this RD Gateway server.</span></span>

## <a name="requirements"></a><span data-ttu-id="47626-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47626-112">Requirements</span></span>



| <span data-ttu-id="47626-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="47626-113">Requirement</span></span> | <span data-ttu-id="47626-114">Value</span><span class="sxs-lookup"><span data-stu-id="47626-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47626-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47626-115">Minimum supported client</span></span><br/> | <span data-ttu-id="47626-116">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="47626-116">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="47626-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47626-117">Minimum supported server</span></span><br/> | <span data-ttu-id="47626-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47626-118">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="47626-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="47626-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="47626-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47626-120"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="47626-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47626-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47626-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47626-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="47626-123">IID</span><span class="sxs-lookup"><span data-stu-id="47626-123">IID</span></span><br/>                      | <span data-ttu-id="47626-124">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="47626-124">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47626-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="47626-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47626-126">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="47626-126">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="47626-127">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="47626-127">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





