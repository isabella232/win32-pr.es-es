---
title: Propiedad GatewayCredSourceCookie de IMsRdpClientTransportSettings3
description: Especifica si el origen de credenciales está basado en cookies.
ms.assetid: 039459a3-7a83-444c-a0b4-46ef0dc5ddd0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayCredSourceCookie
- Propiedad GatewayCredSourceCookie Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings3, propiedad GatewayCredSourceCookie
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.get_GatewayCredSourceCookie
- IMsRdpClientTransportSettings3.put_GatewayCredSourceCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9547df10ce9f528a4b52c526c970a82d0bd098c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676959"
---
# <a name="imsrdpclienttransportsettings3gatewaycredsourcecookie-property"></a><span data-ttu-id="ebd93-106">IMsRdpClientTransportSettings3:: GatewayCredSourceCookie (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ebd93-106">IMsRdpClientTransportSettings3::GatewayCredSourceCookie property</span></span>

<span data-ttu-id="ebd93-107">Especifica si el origen de credenciales está basado en cookies.</span><span class="sxs-lookup"><span data-stu-id="ebd93-107">Specifies if the credential source is cookie based.</span></span> <span data-ttu-id="ebd93-108">Contiene una si el origen de la credencial está basado en cookies o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="ebd93-108">Contains one if the credential source is cookie-based or zero otherwise.</span></span>

<span data-ttu-id="ebd93-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ebd93-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd93-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebd93-110">Syntax</span></span>


```C++
HRESULT put_GatewayCredSourceCookie(
  [in]          ULONG ulProxyCredSourceCookie
);

HRESULT get_GatewayCredSourceCookie(
  [out, retval] ULONG *pulProxyCredSourceCookie
);
```



## <a name="property-value"></a><span data-ttu-id="ebd93-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ebd93-111">Property value</span></span>

<span data-ttu-id="ebd93-112">Valor **ULong** que especifica si el origen de credenciales está basado en cookies.</span><span class="sxs-lookup"><span data-stu-id="ebd93-112">A **ULONG** value that specifies if the credential source is cookie based.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd93-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebd93-113">Requirements</span></span>



| <span data-ttu-id="ebd93-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebd93-114">Requirement</span></span> | <span data-ttu-id="ebd93-115">Value</span><span class="sxs-lookup"><span data-stu-id="ebd93-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd93-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebd93-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd93-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebd93-117">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="ebd93-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebd93-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd93-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebd93-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ebd93-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ebd93-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebd93-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd93-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebd93-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebd93-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebd93-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebd93-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd93-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebd93-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd93-125">**IMsRdpClientTransportSettings3**</span><span class="sxs-lookup"><span data-stu-id="ebd93-125">**IMsRdpClientTransportSettings3**</span></span>](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





