---
title: Propiedad GatewayDefaultUsageMethod de IMsRdpClientTransportSettings
description: El método de uso predeterminado para la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GatewayDefaultUsageMethod
- Propiedad GatewayDefaultUsageMethod Servicios de Escritorio remoto, interfaz IMsRdpClientTransportSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientTransportSettings, propiedad GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685898"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="cbb80-106">IMsRdpClientTransportSettings:: GatewayDefaultUsageMethod (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cbb80-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="cbb80-107">El método de uso predeterminado para la puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="cbb80-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="cbb80-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cbb80-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbb80-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbb80-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="cbb80-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cbb80-110">Property value</span></span>

<span data-ttu-id="cbb80-111">Un puntero al método de uso predeterminado para la puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cbb80-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="cbb80-112">Devuelve una Unión de la configuración de usuario establecida por [**Put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)y la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="cbb80-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="cbb80-113">Si no se estableció ninguna configuración de usuario en **Put \_ GatewayUsageMethod ()**, **Get \_ GatewayDefaultUsageMethod ()** devolverá el valor predeterminado de la **\_ \_ \_ detección del modo proxy de TSC**.</span><span class="sxs-lookup"><span data-stu-id="cbb80-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cbb80-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cbb80-114">Error codes</span></span>

<span data-ttu-id="cbb80-115">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="cbb80-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbb80-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbb80-116">Requirements</span></span>



| <span data-ttu-id="cbb80-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbb80-117">Requirement</span></span> | <span data-ttu-id="cbb80-118">Value</span><span class="sxs-lookup"><span data-stu-id="cbb80-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbb80-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbb80-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cbb80-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbb80-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="cbb80-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbb80-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cbb80-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbb80-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="cbb80-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cbb80-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="cbb80-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbb80-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cbb80-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbb80-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbb80-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbb80-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cbb80-127">IID</span><span class="sxs-lookup"><span data-stu-id="cbb80-127">IID</span></span><br/>                      | <span data-ttu-id="cbb80-128">IID \_ IMsRdpClientTransportSettings se define como 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="cbb80-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbb80-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbb80-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbb80-130">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="cbb80-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





