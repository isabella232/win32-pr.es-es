---
title: Tipo complejo de InputTypeListType
description: Define una lista de tipos de entrada.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- InputTypeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151071"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="dc242-104">Tipo complejo de InputTypeListType</span><span class="sxs-lookup"><span data-stu-id="dc242-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="dc242-105">Define una lista de tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc242-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="dc242-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc242-106">Child elements</span></span>



| <span data-ttu-id="dc242-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="dc242-107">Element</span></span>                                                                | <span data-ttu-id="dc242-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc242-108">Type</span></span>                                                           | <span data-ttu-id="dc242-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc242-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="dc242-110">**Intype**</span><span class="sxs-lookup"><span data-stu-id="dc242-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="dc242-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="dc242-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="dc242-112">Define un tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc242-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dc242-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc242-113">Requirements</span></span>



| <span data-ttu-id="dc242-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc242-114">Requirement</span></span> | <span data-ttu-id="dc242-115">Value</span><span class="sxs-lookup"><span data-stu-id="dc242-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc242-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc242-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc242-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dc242-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc242-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc242-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc242-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc242-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





