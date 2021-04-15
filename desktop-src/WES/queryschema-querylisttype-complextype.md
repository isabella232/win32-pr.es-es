---
title: Tipo complejo de QueryListType
description: Define una lista de consultas que pueden contener un conjunto de selectores e supresors que se usan para incluir eventos en el conjunto de resultados o para excluir eventos del mismo.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- QueryListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695916"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="61c63-104">Tipo complejo de QueryListType</span><span class="sxs-lookup"><span data-stu-id="61c63-104">QueryListType Complex Type</span></span>

<span data-ttu-id="61c63-105">Define una lista de consultas que pueden contener un conjunto de selectores e supresors que se usan para incluir eventos en el conjunto de resultados o para excluir eventos del mismo.</span><span class="sxs-lookup"><span data-stu-id="61c63-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="61c63-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61c63-106">Child elements</span></span>



| <span data-ttu-id="61c63-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="61c63-107">Element</span></span>                                                  | <span data-ttu-id="61c63-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="61c63-108">Type</span></span>                                                   | <span data-ttu-id="61c63-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="61c63-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61c63-110">**Consulta**</span><span class="sxs-lookup"><span data-stu-id="61c63-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="61c63-111">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="61c63-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="61c63-112">Define un conjunto de selectores y suprimidores que se usan para incluir eventos en o excluir eventos del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="61c63-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="61c63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c63-113">Requirements</span></span>



| <span data-ttu-id="61c63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61c63-114">Requirement</span></span> | <span data-ttu-id="61c63-115">Value</span><span class="sxs-lookup"><span data-stu-id="61c63-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61c63-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c63-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61c63-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="61c63-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61c63-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61c63-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61c63-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="61c63-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





