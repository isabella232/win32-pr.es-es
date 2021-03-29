---
title: Propiedad GatewayHostname de IMsRdpClientTransportSettings
description: Especifica el nombre de host del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 34c4b3b7-3768-4d98-b1e8-7fcb8f9c758d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayHostname
- Propiedad GatewayHostname Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayHostname
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayHostname
- IMsRdpClientTransportSettings.get_GatewayHostname
- IMsRdpClientTransportSettings.put_GatewayHostname
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03835faf48fa8aba557f82da158fdba827a84831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359687"
---
# <a name="imsrdpclienttransportsettingsgatewayhostname-property"></a><span data-ttu-id="0ad9f-106">IMsRdpClientTransportSettings:: GatewayHostname (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0ad9f-106">IMsRdpClientTransportSettings::GatewayHostname property</span></span>

<span data-ttu-id="0ad9f-107">Especifica el nombre de host del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="0ad9f-107">Specifies the host name of the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="0ad9f-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0ad9f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad9f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ad9f-109">Syntax</span></span>


```C++
HRESULT put_GatewayHostname(
  [in]  BSTR newVal
);

HRESULT get_GatewayHostname(
  [out] BSTR *pProxyHostname
);
```



## <a name="property-value"></a><span data-ttu-id="0ad9f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0ad9f-110">Property value</span></span>

<span data-ttu-id="0ad9f-111">Cadena que contiene el nombre de host del servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="0ad9f-111">A string that contains the RD Gateway server host name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0ad9f-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0ad9f-112">Error codes</span></span>

<span data-ttu-id="0ad9f-113">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="0ad9f-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ad9f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ad9f-114">Requirements</span></span>



| <span data-ttu-id="0ad9f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad9f-115">Requirement</span></span> | <span data-ttu-id="0ad9f-116">Value</span><span class="sxs-lookup"><span data-stu-id="0ad9f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad9f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ad9f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad9f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ad9f-118">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="0ad9f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ad9f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad9f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ad9f-120">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="0ad9f-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0ad9f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="0ad9f-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9f-122"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0ad9f-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ad9f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ad9f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ad9f-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0ad9f-125">IID</span><span class="sxs-lookup"><span data-stu-id="0ad9f-125">IID</span></span><br/>                      | <span data-ttu-id="0ad9f-126">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="0ad9f-126">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ad9f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ad9f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ad9f-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="0ad9f-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





