---
description: Especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1 X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: Elemento enableAutoConfig (Indicadores_globales) (LAN_policy)
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
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815422"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="461c5-103">Elemento enableAutoConfig (Indicadores_globales) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="461c5-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="461c5-104">El elemento **enableAutoConfig** (indicadores_globales) especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (como 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="461c5-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="461c5-105">Cuando **enableAutoConfig** tiene un valor de false, los equipos no deben usar el servicio de configuración automática integrado para administrar las conexiones que requieren la autenticación de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="461c5-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="461c5-106">En su lugar, la red especificada en el elemento [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) es la única red disponible para la conexión.</span><span class="sxs-lookup"><span data-stu-id="461c5-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="461c5-107">El servicio de configuración automática solo responderá a las solicitudes para habilitar el servicio.</span><span class="sxs-lookup"><span data-stu-id="461c5-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="461c5-108">Cuando **enableAutoConfig** tiene un valor true, los equipos pueden usar el servicio de configuración automática integrado para conectarse a redes cableadas que requieran autenticación de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="461c5-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="461c5-109">El elemento **enableAutoConfig** se define mediante el elemento [**indicadores_globales**](lan-policyschema-globalflags-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="461c5-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="461c5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="461c5-110">Requirements</span></span>



| <span data-ttu-id="461c5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="461c5-111">Requirement</span></span> | <span data-ttu-id="461c5-112">Value</span><span class="sxs-lookup"><span data-stu-id="461c5-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="461c5-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="461c5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="461c5-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="461c5-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="461c5-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="461c5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="461c5-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="461c5-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="461c5-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="461c5-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="461c5-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="461c5-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="461c5-119">**Indicadores**</span><span class="sxs-lookup"><span data-stu-id="461c5-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="461c5-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="461c5-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="461c5-121">**Indicadores_globales (LANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="461c5-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




