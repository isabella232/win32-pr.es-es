---
title: Propiedad GatewayIsSupported de IMsRdpClientTransportSettings
description: Especifica si se admite la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 31edd35b-251d-404d-bec8-e082bb2427b3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayIsSupported
- Propiedad GatewayIsSupported Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayIsSupported
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayIsSupported
- IMsRdpClientTransportSettings.get_GatewayIsSupported
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de79033c2ab9bae73aae4213e72a54590170a184
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421926"
---
# <a name="imsrdpclienttransportsettingsgatewayissupported-property"></a><span data-ttu-id="f72be-106">IMsRdpClientTransportSettings:: GatewayIsSupported (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f72be-106">IMsRdpClientTransportSettings::GatewayIsSupported property</span></span>

<span data-ttu-id="f72be-107">Especifica si se admite la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="f72be-107">Specifies whether Remote Desktop Gateway (RD Gateway) is supported.</span></span>

<span data-ttu-id="f72be-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f72be-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72be-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f72be-109">Syntax</span></span>


```C++
HRESULT get_GatewayIsSupported(
  [out] BOOL *pfProxyIsSupported
);
```



## <a name="property-value"></a><span data-ttu-id="f72be-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f72be-110">Property value</span></span>

<span data-ttu-id="f72be-111">Especifica si se admite la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="f72be-111">Specifies whether RD Gateway is supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f72be-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f72be-112">Error codes</span></span>

<span data-ttu-id="f72be-113">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f72be-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f72be-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f72be-114">Requirements</span></span>



| <span data-ttu-id="f72be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72be-115">Requirement</span></span> | <span data-ttu-id="f72be-116">Value</span><span class="sxs-lookup"><span data-stu-id="f72be-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72be-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f72be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f72be-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f72be-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="f72be-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f72be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f72be-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f72be-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="f72be-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f72be-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="f72be-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f72be-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f72be-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f72be-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f72be-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f72be-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f72be-125">IID</span><span class="sxs-lookup"><span data-stu-id="f72be-125">IID</span></span><br/>                      | <span data-ttu-id="f72be-126">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="f72be-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f72be-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f72be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72be-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="f72be-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





