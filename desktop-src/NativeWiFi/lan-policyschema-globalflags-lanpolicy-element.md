---
description: Contiene la configuración global para la configuración automática de redes cableadas.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Elemento Indicadores_globales (LANPolicy)
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
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277733"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="eef01-103">Elemento Indicadores_globales (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="eef01-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="eef01-104">El elemento Indicadores_globales (LANPolicy) contiene la configuración global para la configuración automática de redes cableadas.</span><span class="sxs-lookup"><span data-stu-id="eef01-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
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

<span data-ttu-id="eef01-105">El elemento **indicadores_globales** se define mediante el elemento [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="eef01-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="eef01-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eef01-106">Child elements</span></span>



| <span data-ttu-id="eef01-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="eef01-107">Element</span></span>                                                                           | <span data-ttu-id="eef01-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="eef01-108">Type</span></span>    | <span data-ttu-id="eef01-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eef01-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eef01-110">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="eef01-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="eef01-111">boolean</span><span class="sxs-lookup"><span data-stu-id="eef01-111">boolean</span></span> | <span data-ttu-id="eef01-112">Especifica si los equipos usan el servicio de configuración automática integrado para administrar las conexiones a redes cableadas que requieren autenticación de nivel 2 (por ejemplo, 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="eef01-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="eef01-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eef01-113">Requirements</span></span>



| <span data-ttu-id="eef01-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eef01-114">Requirement</span></span> | <span data-ttu-id="eef01-115">Value</span><span class="sxs-lookup"><span data-stu-id="eef01-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eef01-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eef01-116">Minimum supported client</span></span><br/> | <span data-ttu-id="eef01-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eef01-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eef01-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eef01-118">Minimum supported server</span></span><br/> | <span data-ttu-id="eef01-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eef01-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eef01-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="eef01-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="eef01-121">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="eef01-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="eef01-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="eef01-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="eef01-123">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="eef01-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="eef01-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="eef01-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




