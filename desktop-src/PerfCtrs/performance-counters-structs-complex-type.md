---
description: Define una lista de estructuras que contienen valores de contador.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Structs (tipo complejo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667269"
---
# <a name="structs-complex-type"></a><span data-ttu-id="f8399-103">Structs (tipo complejo)</span><span class="sxs-lookup"><span data-stu-id="f8399-103">structs Complex Type</span></span>

<span data-ttu-id="f8399-104">Define una lista de estructuras que contienen valores de contador.</span><span class="sxs-lookup"><span data-stu-id="f8399-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f8399-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8399-105">Child elements</span></span>



| <span data-ttu-id="f8399-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f8399-106">Element</span></span>    | <span data-ttu-id="f8399-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8399-107">Type</span></span>                                                           | <span data-ttu-id="f8399-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8399-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f8399-109">**struct**</span><span class="sxs-lookup"><span data-stu-id="f8399-109">**struct**</span></span> | [<span data-ttu-id="f8399-110">**Man: struct**</span><span class="sxs-lookup"><span data-stu-id="f8399-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="f8399-111">Nombre de una estructura que contiene los valores del contador.</span><span class="sxs-lookup"><span data-stu-id="f8399-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="f8399-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8399-112">Requirements</span></span>



| <span data-ttu-id="f8399-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8399-113">Requirement</span></span> | <span data-ttu-id="f8399-114">Value</span><span class="sxs-lookup"><span data-stu-id="f8399-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f8399-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8399-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f8399-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8399-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f8399-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8399-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f8399-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8399-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




