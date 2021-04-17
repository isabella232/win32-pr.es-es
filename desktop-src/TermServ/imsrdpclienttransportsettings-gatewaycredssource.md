---
title: Propiedad GatewayCredsSource de IMsRdpClientTransportSettings
description: Especifica o recupera el método de autenticación de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayCredsSource
- Propiedad GatewayCredsSource Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422071"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="239d3-106">IMsRdpClientTransportSettings:: GatewayCredsSource (propiedad)</span><span class="sxs-lookup"><span data-stu-id="239d3-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="239d3-107">Especifica o recupera el método de autenticación de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="239d3-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="239d3-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="239d3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="239d3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="239d3-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="239d3-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="239d3-110">Property value</span></span>

<span data-ttu-id="239d3-111">Variable **ULong** que especifica el método de autenticación de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="239d3-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="239d3-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="239d3-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="239d3-113">\_Modo de credenciales de proxy de TSC \_ \_ \_ USERPASS (0)</span><span class="sxs-lookup"><span data-stu-id="239d3-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="239d3-114">Use una contraseña (NTLM) como método de autenticación para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="239d3-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="239d3-115">\_ \_ Tarjeta inteligente del modo de credenciales de proxy de TSC \_ \_ (1)</span><span class="sxs-lookup"><span data-stu-id="239d3-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="239d3-116">Usar una tarjeta inteligente como método de autenticación para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="239d3-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="239d3-117">\_Modo de \_ credenciales de proxy TSC \_ \_ any (4)</span><span class="sxs-lookup"><span data-stu-id="239d3-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="239d3-118">Use cualquier método de autenticación para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="239d3-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="239d3-119">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="239d3-119">Error codes</span></span>

<span data-ttu-id="239d3-120">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="239d3-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="239d3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="239d3-121">Requirements</span></span>



| <span data-ttu-id="239d3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="239d3-122">Requirement</span></span> | <span data-ttu-id="239d3-123">Value</span><span class="sxs-lookup"><span data-stu-id="239d3-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239d3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="239d3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="239d3-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="239d3-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="239d3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="239d3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="239d3-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="239d3-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="239d3-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="239d3-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="239d3-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="239d3-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="239d3-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="239d3-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="239d3-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="239d3-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="239d3-132">IID</span><span class="sxs-lookup"><span data-stu-id="239d3-132">IID</span></span><br/>                      | <span data-ttu-id="239d3-133">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="239d3-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="239d3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="239d3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239d3-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="239d3-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





