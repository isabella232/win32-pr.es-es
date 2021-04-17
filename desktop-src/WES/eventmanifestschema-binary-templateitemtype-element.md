---
title: Elemento binario (TemplateItemType)
description: Contiene los datos binarios proporcionados por la API del registro de eventos.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- EventLog del elemento binario
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696002"
---
# <a name="binary-templateitemtype-element"></a><span data-ttu-id="2a428-104">Elemento binario (TemplateItemType)</span><span class="sxs-lookup"><span data-stu-id="2a428-104">binary (TemplateItemType) Element</span></span>

<span data-ttu-id="2a428-105">Contiene los datos binarios proporcionados por la API del [registro de eventos](/windows/desktop/EventLog/event-logging) .</span><span class="sxs-lookup"><span data-stu-id="2a428-105">Contains the binary data that is supplied by the [Event Log](/windows/desktop/EventLog/event-logging) API.</span></span>

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2a428-106">El elemento **binario** se define mediante el tipo complejo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2a428-106">The **binary** element is defined by the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="2a428-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a428-107">Attributes</span></span>



| <span data-ttu-id="2a428-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a428-108">Name</span></span> | <span data-ttu-id="2a428-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a428-109">Type</span></span>   | <span data-ttu-id="2a428-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a428-110">Description</span></span>                                          |
|------|--------|------------------------------------------------------|
| <span data-ttu-id="2a428-111">name</span><span class="sxs-lookup"><span data-stu-id="2a428-111">name</span></span> | <span data-ttu-id="2a428-112">string</span><span class="sxs-lookup"><span data-stu-id="2a428-112">string</span></span> | <span data-ttu-id="2a428-113">Nombre asociado a los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="2a428-113">The name associated with the binary data.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2a428-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a428-114">Requirements</span></span>



| <span data-ttu-id="2a428-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a428-115">Requirement</span></span> | <span data-ttu-id="2a428-116">Value</span><span class="sxs-lookup"><span data-stu-id="2a428-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a428-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a428-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a428-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a428-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a428-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a428-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a428-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a428-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a428-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a428-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a428-122">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="2a428-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="2a428-123">**plantilla (TemplateListType)**</span><span class="sxs-lookup"><span data-stu-id="2a428-123">**template (TemplateListType)**</span></span>](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

