---
title: Elemento messageTable (MetadataType)
description: Contiene referencias a cadenas que se usan en la sección de metadatos del manifiesto de instrumentación de eventos. Las cadenas se almacenan en un grupo de elementos de mensaje e identificadores combinados.
ms.assetid: 868af191-0f9c-435b-878f-ef0584e097d1
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
ms.openlocfilehash: eb5efc261a2c055a95f71ba556c9acbc0ad45373
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149994"
---
# <a name="messagetable-metadatatype-element"></a><span data-ttu-id="11c5d-105">Elemento messageTable (MetadataType)</span><span class="sxs-lookup"><span data-stu-id="11c5d-105">messageTable (MetadataType) Element</span></span>

<span data-ttu-id="11c5d-106">Contiene referencias a cadenas que se usan en la sección de metadatos del manifiesto de instrumentación de eventos.</span><span class="sxs-lookup"><span data-stu-id="11c5d-106">Contains references to strings that are used in the event instrumentation manifest metadata section.</span></span> <span data-ttu-id="11c5d-107">Las cadenas se almacenan en un grupo de elementos de [**mensaje**](eventmanifestschema-message-messagetable-element.md) e identificadores combinados.</span><span class="sxs-lookup"><span data-stu-id="11c5d-107">The strings are stored in a group of [**message**](eventmanifestschema-message-messagetable-element.md) elements and IDs paired together.</span></span>

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

<span data-ttu-id="11c5d-108">El elemento **messageTable** se define mediante el tipo complejo de [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="11c5d-108">The **messageTable** element is defined by the [**MetadataType**](eventmanifestschema-metadatatype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="11c5d-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="11c5d-109">Child elements</span></span>



| <span data-ttu-id="11c5d-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="11c5d-110">Element</span></span>                                                             | <span data-ttu-id="11c5d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="11c5d-111">Type</span></span> | <span data-ttu-id="11c5d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="11c5d-112">Description</span></span>                                                                               |
|---------------------------------------------------------------------|------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11c5d-113">**Mensaje**</span><span class="sxs-lookup"><span data-stu-id="11c5d-113">**message**</span></span>](eventmanifestschema-message-messagetable-element.md) |      | <span data-ttu-id="11c5d-114">Especifica una referencia a una cadena en la sección de localización del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="11c5d-114">Specifies a reference to a string in the localization section of the manifest.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="11c5d-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="11c5d-115">Attributes</span></span>



| <span data-ttu-id="11c5d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="11c5d-116">Name</span></span>    | <span data-ttu-id="11c5d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="11c5d-117">Type</span></span>   | <span data-ttu-id="11c5d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="11c5d-118">Description</span></span>                                                              |
|---------|--------|--------------------------------------------------------------------------|
| <span data-ttu-id="11c5d-119">message</span><span class="sxs-lookup"><span data-stu-id="11c5d-119">message</span></span> | <span data-ttu-id="11c5d-120">string</span><span class="sxs-lookup"><span data-stu-id="11c5d-120">string</span></span> | <span data-ttu-id="11c5d-121">Referencia a la cadena localizada en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="11c5d-121">A reference to the localized string in the string table.</span></span><br/>      |
| <span data-ttu-id="11c5d-122">mId</span><span class="sxs-lookup"><span data-stu-id="11c5d-122">mid</span></span>     | <span data-ttu-id="11c5d-123">string</span><span class="sxs-lookup"><span data-stu-id="11c5d-123">string</span></span> | <span data-ttu-id="11c5d-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="11c5d-124">Not used.</span></span><br/>                                                     |
| <span data-ttu-id="11c5d-125">símbolo</span><span class="sxs-lookup"><span data-stu-id="11c5d-125">symbol</span></span>  | <span data-ttu-id="11c5d-126">string</span><span class="sxs-lookup"><span data-stu-id="11c5d-126">string</span></span> | <span data-ttu-id="11c5d-127">Símbolo que se usa para hacer referencia al mensaje.</span><span class="sxs-lookup"><span data-stu-id="11c5d-127">The symbol used to reference the message.</span></span><br/>                     |
| <span data-ttu-id="11c5d-128">value</span><span class="sxs-lookup"><span data-stu-id="11c5d-128">value</span></span>   | <span data-ttu-id="11c5d-129">string</span><span class="sxs-lookup"><span data-stu-id="11c5d-129">string</span></span> | <span data-ttu-id="11c5d-130">Número que se va a usar como identificador de mensaje para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="11c5d-130">The number to use as the message identifier for this message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="11c5d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c5d-131">Requirements</span></span>



| <span data-ttu-id="11c5d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c5d-132">Requirement</span></span> | <span data-ttu-id="11c5d-133">Value</span><span class="sxs-lookup"><span data-stu-id="11c5d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="11c5d-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11c5d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="11c5d-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="11c5d-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="11c5d-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11c5d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="11c5d-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="11c5d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11c5d-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="11c5d-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="11c5d-139">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="11c5d-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="11c5d-140">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="11c5d-140">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)
</dt> <dt>

<span data-ttu-id="11c5d-141">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="11c5d-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="11c5d-142">**metadatos (instrumentationManifest)**</span><span class="sxs-lookup"><span data-stu-id="11c5d-142">**metadata (instrumentationManifest)**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)
</dt> </dl>

 

 





