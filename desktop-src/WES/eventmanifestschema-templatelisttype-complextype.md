---
title: Tipo complejo de TemplateListType
description: Define una lista de plantillas que especifican los datos que se van a incluir con los eventos. | Tipo complejo de TemplateListType
ms.assetid: 7f676746-6773-4ae2-8330-60d432c29e3a
keywords:
- TemplateListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TemplateListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60b31fd88d05f00229f27a616a29483a29bd49d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820727"
---
# <a name="templatelisttype-complex-type"></a><span data-ttu-id="4a023-105">Tipo complejo de TemplateListType</span><span class="sxs-lookup"><span data-stu-id="4a023-105">TemplateListType Complex Type</span></span>

<span data-ttu-id="4a023-106">Define una lista de plantillas que especifican los datos que se van a incluir con los eventos.</span><span class="sxs-lookup"><span data-stu-id="4a023-106">Defines a list of templates that specify the data to include with the events.</span></span>

``` syntax
<xs:complexType name="TemplateListType">
    <xs:sequence>
        <xs:element name="template"
            type="TemplateItemType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4a023-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a023-107">Child elements</span></span>



| <span data-ttu-id="4a023-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="4a023-108">Element</span></span>                                                                   | <span data-ttu-id="4a023-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a023-109">Type</span></span>                                                                         | <span data-ttu-id="4a023-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a023-110">Description</span></span>                                                           |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="4a023-111">**plantillas**</span><span class="sxs-lookup"><span data-stu-id="4a023-111">**template**</span></span>](eventmanifestschema-template-templatelisttype-element.md) | [<span data-ttu-id="4a023-112">**TemplateItemType**</span><span class="sxs-lookup"><span data-stu-id="4a023-112">**TemplateItemType**</span></span>](eventmanifestschema-templateitemtype-complextype.md) | <span data-ttu-id="4a023-113">Plantilla que define los datos que se van a incluir con un evento.</span><span class="sxs-lookup"><span data-stu-id="4a023-113">A template that defines the data to include with an event.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4a023-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a023-114">Requirements</span></span>



| <span data-ttu-id="4a023-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a023-115">Requirement</span></span> | <span data-ttu-id="4a023-116">Value</span><span class="sxs-lookup"><span data-stu-id="4a023-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a023-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a023-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a023-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4a023-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a023-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a023-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a023-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4a023-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





