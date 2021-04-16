---
description: Contiene la configuración global del módulo de configuración automática (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Elemento Indicadores_globales (WLANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546814"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="cf924-103">Elemento Indicadores_globales (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="cf924-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="cf924-104">El elemento Indicadores_globales (WLANPolicy) contiene la configuración global para el módulo de configuración automática (ACM).</span><span class="sxs-lookup"><span data-stu-id="cf924-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="cf924-105">Este elemento es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cf924-105">This element is mandatory.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="cf924-106">El elemento **indicadores_globales** se define mediante el elemento [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cf924-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="cf924-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cf924-107">Child elements</span></span>



| <span data-ttu-id="cf924-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="cf924-108">Element</span></span>                                                                                                                    | <span data-ttu-id="cf924-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf924-109">Type</span></span>    | <span data-ttu-id="cf924-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf924-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf924-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="cf924-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="cf924-112">boolean</span><span class="sxs-lookup"><span data-stu-id="cf924-112">boolean</span></span> | <span data-ttu-id="cf924-113">Especifica si un usuario puede crear un perfil de todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="cf924-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="cf924-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="cf924-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="cf924-115">boolean</span><span class="sxs-lookup"><span data-stu-id="cf924-115">boolean</span></span> | <span data-ttu-id="cf924-116">Especifica si los equipos usan el servicio de configuración automática (AutoConfig) integrado para administrar las conexiones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="cf924-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="cf924-117">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="cf924-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="cf924-118">boolean</span><span class="sxs-lookup"><span data-stu-id="cf924-118">boolean</span></span> | <span data-ttu-id="cf924-119">Especifica si las redes denegadas aparecen en el Asistente para **conectarse a una red** .</span><span class="sxs-lookup"><span data-stu-id="cf924-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="cf924-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf924-120">Requirements</span></span>



| <span data-ttu-id="cf924-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf924-121">Requirement</span></span> | <span data-ttu-id="cf924-122">Value</span><span class="sxs-lookup"><span data-stu-id="cf924-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf924-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf924-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cf924-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cf924-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf924-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf924-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cf924-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cf924-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf924-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf924-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf924-128">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="cf924-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cf924-129">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="cf924-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="cf924-130">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="cf924-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cf924-131">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="cf924-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




