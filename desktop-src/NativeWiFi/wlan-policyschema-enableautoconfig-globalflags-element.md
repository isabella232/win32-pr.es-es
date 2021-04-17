---
description: Especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: Elemento enableAutoConfig (Indicadores_globales) (LAN_policy) para WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106188042"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="48cef-103">Elemento enableAutoConfig (Indicadores_globales) (LAN_policy) para WLAN</span><span class="sxs-lookup"><span data-stu-id="48cef-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="48cef-104">El elemento **enableAutoConfig** (indicadores_globales) especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="48cef-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="48cef-105">Cuando **enableAutoConfig** tiene un valor de false, los equipos no deben usar AutoConfig para administrar las conexiones inalámbricas y el servicio de configuración automática solo responde a las solicitudes para habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="48cef-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="48cef-106">Cuando **enableAutoConfig** tiene un valor de true, los equipos pueden usar el servicio de configuración automática.</span><span class="sxs-lookup"><span data-stu-id="48cef-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="48cef-107">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48cef-107">This element is mandatory.</span></span> <span data-ttu-id="48cef-108">Cuando el servicio de configuración automática crea un perfil, este elemento tendrá el valor predeterminado TRUE.</span><span class="sxs-lookup"><span data-stu-id="48cef-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="48cef-109">El elemento **enableAutoConfig** se define mediante el elemento [**indicadores_globales**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48cef-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="48cef-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48cef-110">Requirements</span></span>



| <span data-ttu-id="48cef-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="48cef-111">Requirement</span></span> | <span data-ttu-id="48cef-112">Value</span><span class="sxs-lookup"><span data-stu-id="48cef-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48cef-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48cef-113">Minimum supported client</span></span><br/> | <span data-ttu-id="48cef-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="48cef-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48cef-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48cef-115">Minimum supported server</span></span><br/> | <span data-ttu-id="48cef-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="48cef-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48cef-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48cef-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="48cef-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="48cef-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="48cef-119">**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="48cef-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="48cef-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="48cef-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="48cef-121">**Indicadores_globales (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="48cef-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




