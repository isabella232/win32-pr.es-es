---
title: Propiedad GatewayProfileUsageMethod de IMsRdpClientTransportSettings
description: Especifica si se va a usar la configuración predeterminada de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayProfileUsageMethod
- Propiedad GatewayProfileUsageMethod Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayProfileUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a12a9836e89348d1eb7ccdf680b23e2695c938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422276"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a><span data-ttu-id="d4667-106">IMsRdpClientTransportSettings:: GatewayProfileUsageMethod (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d4667-106">IMsRdpClientTransportSettings::GatewayProfileUsageMethod property</span></span>

<span data-ttu-id="d4667-107">Especifica si se va a usar la configuración predeterminada de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="d4667-107">Specifies whether to use default Remote Desktop Gateway (RD Gateway) settings.</span></span>

<span data-ttu-id="d4667-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d4667-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4667-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4667-109">Syntax</span></span>


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="d4667-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d4667-110">Property value</span></span>

<span data-ttu-id="d4667-111">Método de uso del perfil de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d4667-111">The RD Gateway profile usage method.</span></span> <span data-ttu-id="d4667-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d4667-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span data-ttu-id="d4667-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC \_ \_ \_ Modo \_ predeterminado de Perfil de proxy** (0 (0X0))</span><span class="sxs-lookup"><span data-stu-id="d4667-113"><span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**TSC\_PROXY\_PROFILE\_MODE\_DEFAULT** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d4667-114">Usar el modo de perfil predeterminado, tal como lo especifica el administrador.</span><span class="sxs-lookup"><span data-stu-id="d4667-114">Use the default profile mode, as specified by the administrator.</span></span>

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span data-ttu-id="d4667-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC \_ Modo de Perfil de PROXY \_ \_ \_ explícito** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d4667-115"><span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**TSC\_PROXY\_PROFILE\_MODE\_EXPLICIT** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d4667-116">Utilice la configuración explícita, especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d4667-116">Use explicit settings, as specified by the user.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="d4667-117">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d4667-117">Error codes</span></span>

<span data-ttu-id="d4667-118">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4667-118">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4667-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4667-119">Requirements</span></span>



| <span data-ttu-id="d4667-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4667-120">Requirement</span></span> | <span data-ttu-id="d4667-121">Value</span><span class="sxs-lookup"><span data-stu-id="d4667-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4667-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4667-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4667-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4667-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="d4667-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4667-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4667-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4667-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="d4667-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d4667-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4667-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4667-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d4667-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4667-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4667-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4667-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d4667-130">IID</span><span class="sxs-lookup"><span data-stu-id="d4667-130">IID</span></span><br/>                      | <span data-ttu-id="d4667-131">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="d4667-131">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4667-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4667-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4667-133">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="d4667-133">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





