---
description: Especifica el nombre y el tipo de una red inalámbrica.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Tipo complejo de networkItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678310"
---
# <a name="networkitemtype-complex-type"></a><span data-ttu-id="7815d-103">Tipo complejo de networkItemType</span><span class="sxs-lookup"><span data-stu-id="7815d-103">networkItemType Complex Type</span></span>

<span data-ttu-id="7815d-104">El tipo complejo de networkItemType especifica el nombre y el tipo de una red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="7815d-104">The networkItemType complex type specifies the name and type of a wireless network.</span></span>

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="7815d-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7815d-105">Child elements</span></span>



| <span data-ttu-id="7815d-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="7815d-106">Element</span></span>                                                                      | <span data-ttu-id="7815d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7815d-107">Type</span></span>                                                                    | <span data-ttu-id="7815d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7815d-108">Description</span></span>                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="7815d-109">**networkName**</span><span class="sxs-lookup"><span data-stu-id="7815d-109">**networkName**</span></span>](wlan-policyschema-networkname-networkitemtype-element.md) | [<span data-ttu-id="7815d-110">**networkNameType**</span><span class="sxs-lookup"><span data-stu-id="7815d-110">**networkNameType**</span></span>](wlan-policyschema-networknametype-simpletype.md) | <span data-ttu-id="7815d-111">El identificador del conjunto de servicios (SSID) de la red.</span><span class="sxs-lookup"><span data-stu-id="7815d-111">The service set identifier (SSID) of the network.</span></span> <br/> |
| [<span data-ttu-id="7815d-112">**networkType**</span><span class="sxs-lookup"><span data-stu-id="7815d-112">**networkType**</span></span>](wlan-policyschema-networktype-networkitemtype-element.md) | [<span data-ttu-id="7815d-113">**networkTypeType**</span><span class="sxs-lookup"><span data-stu-id="7815d-113">**networkTypeType**</span></span>](wlan-policyschema-networktypetype-simpletype.md) | <span data-ttu-id="7815d-114">El tipo de red.</span><span class="sxs-lookup"><span data-stu-id="7815d-114">The network type.</span></span> <br/>                                 |



## <a name="requirements"></a><span data-ttu-id="7815d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7815d-115">Requirements</span></span>



| <span data-ttu-id="7815d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7815d-116">Requirement</span></span> | <span data-ttu-id="7815d-117">Value</span><span class="sxs-lookup"><span data-stu-id="7815d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7815d-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7815d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7815d-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7815d-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7815d-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7815d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7815d-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7815d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




