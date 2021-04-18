---
title: Elemento messageTable (EventsType)
description: Contiene una referencia a una cadena en la sección de localización del manifiesto. | Elemento messageTable (EventsType)
ms.assetid: 4dcc1afe-8f2b-4baf-b40b-406f60368575
keywords:
- elemento messageTable EventLog
topic_type:
- apiref
api_name:
- messageTable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85ce478fb30389ba911ef9dd76473a6261974f55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698054"
---
# <a name="messagetable-eventstype-element"></a><span data-ttu-id="6c897-105">Elemento messageTable (EventsType)</span><span class="sxs-lookup"><span data-stu-id="6c897-105">messageTable (EventsType) Element</span></span>

<span data-ttu-id="6c897-106">Contiene una referencia a una cadena en la sección de localización del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="6c897-106">Contains a reference to a string in the localization section of the manifest.</span></span>

``` syntax
<xs:element name="messageTable">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="message"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6c897-107">El elemento **messageTable** se define mediante el tipo complejo de [**EventsType**](eventmanifestschema-eventstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c897-107">The **messageTable** element is defined by the [**EventsType**](eventmanifestschema-eventstype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6c897-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6c897-108">Child elements</span></span>



| <span data-ttu-id="6c897-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="6c897-109">Element</span></span>                                                             | <span data-ttu-id="6c897-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c897-110">Type</span></span> | <span data-ttu-id="6c897-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c897-111">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c897-112">**Mensaje**</span><span class="sxs-lookup"><span data-stu-id="6c897-112">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="6c897-113">Especifica una referencia a una cadena en la sección de localización del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="6c897-113">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="6c897-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="6c897-114">Attributes</span></span>



| <span data-ttu-id="6c897-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c897-115">Name</span></span>    | <span data-ttu-id="6c897-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c897-116">Type</span></span>   | <span data-ttu-id="6c897-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c897-117">Description</span></span>                                                                                        |
|---------|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c897-118">message</span><span class="sxs-lookup"><span data-stu-id="6c897-118">message</span></span> | <span data-ttu-id="6c897-119">string</span><span class="sxs-lookup"><span data-stu-id="6c897-119">string</span></span> | <span data-ttu-id="6c897-120">Referencia a la cadena localizada en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="6c897-120">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="6c897-121">mId</span><span class="sxs-lookup"><span data-stu-id="6c897-121">mid</span></span>     | <span data-ttu-id="6c897-122">string</span><span class="sxs-lookup"><span data-stu-id="6c897-122">string</span></span> | <span data-ttu-id="6c897-123">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6c897-123">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="6c897-124">símbolo</span><span class="sxs-lookup"><span data-stu-id="6c897-124">symbol</span></span>  | <span data-ttu-id="6c897-125">string</span><span class="sxs-lookup"><span data-stu-id="6c897-125">string</span></span> | <span data-ttu-id="6c897-126">Nombre simbólico que desea que cree el compilador de mensajes para esta cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6c897-126">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="6c897-127">value</span><span class="sxs-lookup"><span data-stu-id="6c897-127">value</span></span>   | <span data-ttu-id="6c897-128">string</span><span class="sxs-lookup"><span data-stu-id="6c897-128">string</span></span> | <span data-ttu-id="6c897-129">Número que se va a usar como identificador de mensaje para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="6c897-129">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="requirements"></a><span data-ttu-id="6c897-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c897-130">Requirements</span></span>



| <span data-ttu-id="6c897-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c897-131">Requirement</span></span> | <span data-ttu-id="6c897-132">Value</span><span class="sxs-lookup"><span data-stu-id="6c897-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6c897-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c897-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6c897-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6c897-134">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6c897-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c897-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6c897-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c897-136">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c897-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c897-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c897-138">**Elementos primarios**</span><span class="sxs-lookup"><span data-stu-id="6c897-138">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="6c897-139">**Elemento Events (InstrumentationType)**</span><span class="sxs-lookup"><span data-stu-id="6c897-139">**events (InstrumentationType) Element**</span></span>](eventmanifestschema-events-instrumentationtype-element.md)
</dt> </dl>

 

 





