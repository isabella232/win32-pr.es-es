---
title: Tipo complejo de KeywordListType
description: Define una lista de palabras clave que clasifican eventos. | Tipo complejo de KeywordListType
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- KeywordListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698091"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="9fdf3-105">Tipo complejo de KeywordListType</span><span class="sxs-lookup"><span data-stu-id="9fdf3-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="9fdf3-106">Define una lista de palabras clave que clasifican eventos.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9fdf3-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9fdf3-107">Child elements</span></span>



| <span data-ttu-id="9fdf3-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9fdf3-108">Element</span></span>                                                                | <span data-ttu-id="9fdf3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fdf3-109">Type</span></span>                                                               | <span data-ttu-id="9fdf3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fdf3-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fdf3-111">**palabra clave**</span><span class="sxs-lookup"><span data-stu-id="9fdf3-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="9fdf3-112">**KeywordType**</span><span class="sxs-lookup"><span data-stu-id="9fdf3-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="9fdf3-113">Define una palabra clave que identifica una categoría de eventos.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="9fdf3-114">Puede especificar un máximo de 48 palabras clave.</span><span class="sxs-lookup"><span data-stu-id="9fdf3-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9fdf3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fdf3-115">Requirements</span></span>



| <span data-ttu-id="9fdf3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fdf3-116">Requirement</span></span> | <span data-ttu-id="9fdf3-117">Value</span><span class="sxs-lookup"><span data-stu-id="9fdf3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9fdf3-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fdf3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9fdf3-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9fdf3-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9fdf3-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fdf3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9fdf3-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fdf3-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





