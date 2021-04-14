---
title: Propiedad GatewayPassword de IMsRdpClientTransportSettings2
description: Especifica la contraseña que un usuario proporciona para conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayPassword
- Propiedad GatewayPassword Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings2, propiedad GatewayPassword
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533873"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="bd846-106">IMsRdpClientTransportSettings2:: GatewayPassword (propiedad)</span><span class="sxs-lookup"><span data-stu-id="bd846-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="bd846-107">Especifica la contraseña que un usuario proporciona para conectarse al servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="bd846-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="bd846-108">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="bd846-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd846-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd846-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="bd846-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bd846-110">Property value</span></span>

<span data-ttu-id="bd846-111">La contraseña que un usuario proporciona para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="bd846-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bd846-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bd846-112">Error codes</span></span>

<span data-ttu-id="bd846-113">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd846-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd846-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd846-114">Requirements</span></span>



| <span data-ttu-id="bd846-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd846-115">Requirement</span></span> | <span data-ttu-id="bd846-116">Value</span><span class="sxs-lookup"><span data-stu-id="bd846-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd846-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd846-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd846-118">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="bd846-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="bd846-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd846-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd846-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd846-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="bd846-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bd846-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd846-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd846-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bd846-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd846-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd846-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd846-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="bd846-125">IID</span><span class="sxs-lookup"><span data-stu-id="bd846-125">IID</span></span><br/>                      | <span data-ttu-id="bd846-126">IID \_ IMsRdpClientTransportSettings2 se define como 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="bd846-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd846-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd846-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd846-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="bd846-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="bd846-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="bd846-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





