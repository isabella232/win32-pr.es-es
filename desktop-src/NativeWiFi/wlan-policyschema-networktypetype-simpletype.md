---
description: Define los tipos de red inalámbrica.
ms.assetid: 03236db9-4f58-4fe3-82ff-d4b3a387490a
title: Tipo simple de networkTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d0acb998c879e718a0e201418610bb0aa6db8c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688324"
---
# <a name="networktypetype-simple-type"></a><span data-ttu-id="3b54a-103">Tipo simple de networkTypeType</span><span class="sxs-lookup"><span data-stu-id="3b54a-103">networkTypeType Simple Type</span></span>

<span data-ttu-id="3b54a-104">El tipo simple networkTypeType define los tipos de red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="3b54a-104">The networkTypeType simple type defines the wireless network types.</span></span> <span data-ttu-id="3b54a-105">Hay dos tipos de redes: redes de infraestructura (ESS) y redes ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="3b54a-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:simpleType name="networkTypeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="IBSS"
         />
        <xs:enumeration
            value="ESS"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="3b54a-106">Valores de enumeración</span><span class="sxs-lookup"><span data-stu-id="3b54a-106">Enumeration values</span></span>

<span data-ttu-id="3b54a-107">El tipo simple **networkTypeType** define los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="3b54a-107">The **networkTypeType** simple type defines the following values.</span></span>



| <span data-ttu-id="3b54a-108">Value</span><span class="sxs-lookup"><span data-stu-id="3b54a-108">Value</span></span> | <span data-ttu-id="3b54a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b54a-109">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="3b54a-110">IBSS</span><span class="sxs-lookup"><span data-stu-id="3b54a-110">IBSS</span></span>  |             |
| <span data-ttu-id="3b54a-111">ESS</span><span class="sxs-lookup"><span data-stu-id="3b54a-111">ESS</span></span>   |             |



## <a name="requirements"></a><span data-ttu-id="3b54a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b54a-112">Requirements</span></span>



| <span data-ttu-id="3b54a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b54a-113">Requirement</span></span> | <span data-ttu-id="3b54a-114">Value</span><span class="sxs-lookup"><span data-stu-id="3b54a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b54a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b54a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b54a-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b54a-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b54a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b54a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b54a-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b54a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




