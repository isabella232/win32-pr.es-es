---
title: Elemento message (messageTable)
description: Contiene una referencia a una cadena en la sección de localización del manifiesto. | Elemento message (messageTable)
ms.assetid: 0988cf99-c7e1-446b-869e-9ac4a0976ac5
keywords:
- EventLog del elemento de mensaje
topic_type:
- apiref
api_name:
- message
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e1165e3a613434fb76befb87cd1a83ed3af95d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698055"
---
# <a name="message-messagetable-element"></a><span data-ttu-id="14f20-105">Elemento message (messageTable)</span><span class="sxs-lookup"><span data-stu-id="14f20-105">message (messageTable) Element</span></span>

<span data-ttu-id="14f20-106">Contiene una referencia a una cadena en la sección de localización del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="14f20-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="message">
    <xs:complexType>
        <xs:attribute name="value"
            type="string"
            use="required"
         />
        <xs:attribute name="mid"
            type="string"
            use="optional"
         />
        <xs:attribute name="message"
            type="string"
            use="required"
         />
        <xs:attribute name="symbol"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="14f20-107">El elemento de **mensaje** se define mediante el elemento [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="14f20-107">The **message** element is defined by the [**messageTable**](eventmanifestschema-messagetable-instrumentationtype-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="14f20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="14f20-108">Attributes</span></span>



| <span data-ttu-id="14f20-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="14f20-109">Name</span></span>    | <span data-ttu-id="14f20-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="14f20-110">Type</span></span>   | <span data-ttu-id="14f20-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="14f20-111">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f20-112">message</span><span class="sxs-lookup"><span data-stu-id="14f20-112">message</span></span> | <span data-ttu-id="14f20-113">string</span><span class="sxs-lookup"><span data-stu-id="14f20-113">string</span></span> | <span data-ttu-id="14f20-114">Referencia a la cadena localizada en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="14f20-114">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="14f20-115">mId</span><span class="sxs-lookup"><span data-stu-id="14f20-115">mid</span></span>     | <span data-ttu-id="14f20-116">string</span><span class="sxs-lookup"><span data-stu-id="14f20-116">string</span></span> | <span data-ttu-id="14f20-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="14f20-117">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="14f20-118">símbolo</span><span class="sxs-lookup"><span data-stu-id="14f20-118">symbol</span></span>  | <span data-ttu-id="14f20-119">string</span><span class="sxs-lookup"><span data-stu-id="14f20-119">string</span></span> | <span data-ttu-id="14f20-120">Nombre simbólico que desea que cree el compilador de mensajes para esta cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="14f20-120">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="14f20-121">value</span><span class="sxs-lookup"><span data-stu-id="14f20-121">value</span></span>   | <span data-ttu-id="14f20-122">string</span><span class="sxs-lookup"><span data-stu-id="14f20-122">string</span></span> | <span data-ttu-id="14f20-123">Número que se va a usar como identificador de mensaje para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="14f20-123">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="14f20-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14f20-124">Requirements</span></span>



| <span data-ttu-id="14f20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f20-125">Requirement</span></span> | <span data-ttu-id="14f20-126">Value</span><span class="sxs-lookup"><span data-stu-id="14f20-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14f20-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14f20-127">Minimum supported client</span></span><br/> | <span data-ttu-id="14f20-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="14f20-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="14f20-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14f20-129">Minimum supported server</span></span><br/> | <span data-ttu-id="14f20-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="14f20-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14f20-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="14f20-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="14f20-132">**Elementos primarios**</span><span class="sxs-lookup"><span data-stu-id="14f20-132">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="14f20-133">**messageTable (EventsType)**</span><span class="sxs-lookup"><span data-stu-id="14f20-133">**messageTable (EventsType)**</span></span>](eventmanifestschema-messagetable-instrumentationtype-element.md)
</dt> <dt>

[<span data-ttu-id="14f20-134">**messageTable (MetadataType)**</span><span class="sxs-lookup"><span data-stu-id="14f20-134">**messageTable (MetadataType)**</span></span>](eventmanifestschema-messagetable-metadatatype-element.md)
</dt> </dl>

 

 





