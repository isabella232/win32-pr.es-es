---
description: Identifica el nodo raíz de la sección de contadores de un manifiesto de instrumentación.
ms.assetid: f16f432b-466f-4a3c-bc1b-e80b876a2511
title: counters (elemento)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11ced77890dba6d47f713642adf9b41d4b30f6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909725"
---
# <a name="counters-element"></a><span data-ttu-id="ee2e1-103">counters (elemento)</span><span class="sxs-lookup"><span data-stu-id="ee2e1-103">counters Element</span></span>

<span data-ttu-id="ee2e1-104">Identifica el nodo raíz de la sección de contadores de un manifiesto de instrumentación.</span><span class="sxs-lookup"><span data-stu-id="ee2e1-104">Identifies the root node of the counters section of an instrumentation manifest.</span></span>

``` syntax
<xs:element name="counters"
    type="man:counters"
>
    <xs:key name="uniqueprovGUID">
        <xs:selector
            xpath="./man:provider"
         />
        <xs:field
            xpath="@providerGuid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetGUID">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@guid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetURI">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetName">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@name"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:key>
    <xs:unique name="uniqueCounterSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:unique>
    <xs:key name="uniqueCounterURI">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
</xs:element>
```

## <a name="remarks"></a><span data-ttu-id="ee2e1-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee2e1-105">Remarks</span></span>

<span data-ttu-id="ee2e1-106">El nodo primario de este elemento es el elemento de [**instrumentación**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="ee2e1-106">This element's parent node is the [**instrumentation**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) element of the manifest.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee2e1-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee2e1-107">Requirements</span></span>



| <span data-ttu-id="ee2e1-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee2e1-108">Requirement</span></span> | <span data-ttu-id="ee2e1-109">Value</span><span class="sxs-lookup"><span data-stu-id="ee2e1-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ee2e1-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2e1-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ee2e1-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ee2e1-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ee2e1-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee2e1-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ee2e1-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ee2e1-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

