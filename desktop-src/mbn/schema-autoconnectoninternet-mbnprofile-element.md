---
description: Especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Elemento AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275505"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="5b838-103">Elemento AutoConnectOnInternet (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="5b838-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="5b838-104">El elemento **AutoConnectOnInternet (MBNProfile)** especifica si el dispositivo de banda ancha móvil se conectará automáticamente a una red.</span><span class="sxs-lookup"><span data-stu-id="5b838-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="5b838-105">Si se establece en **false**, la lógica de conexión automática del servicio de banda ancha móvil no se utilizará si hay otra conectividad de red disponible para el sistema.</span><span class="sxs-lookup"><span data-stu-id="5b838-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="5b838-106">Si se establece en **true**, el servicio de banda ancha móvil intentará conectar automáticamente el dispositivo a la red según la configuración de conexión automática definida en el elemento [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5b838-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="5b838-107">**Windows 8 y versiones posteriores:** Este elemento está en desuso.</span><span class="sxs-lookup"><span data-stu-id="5b838-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="5b838-108">Use el método [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) con el parámetro *Property* establecido en **WCM \_ global \_ Property \_ miniMIZE \_** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5b838-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="5b838-109">El elemento **AutoConnectOnInternet** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5b838-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b838-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b838-110">Requirements</span></span>



| <span data-ttu-id="5b838-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b838-111">Requirement</span></span> | <span data-ttu-id="5b838-112">Value</span><span class="sxs-lookup"><span data-stu-id="5b838-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="5b838-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b838-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5b838-114">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="5b838-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5b838-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b838-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5b838-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5b838-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="5b838-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b838-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="5b838-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="5b838-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5b838-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="5b838-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="5b838-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="5b838-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5b838-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="5b838-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

