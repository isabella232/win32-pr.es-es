---
title: Tipo complejo de DebugDataType
description: Define los datos que se pueden registrar para los eventos de preprocesador de seguimiento de software (WPP) de Windows.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078797"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="f3bbf-104">Tipo complejo de DebugDataType</span><span class="sxs-lookup"><span data-stu-id="f3bbf-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="f3bbf-105">Define los datos que se pueden registrar para los eventos de preprocesador de seguimiento de software (WPP) de Windows.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f3bbf-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3bbf-106">Child elements</span></span>



| <span data-ttu-id="f3bbf-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f3bbf-107">Element</span></span>                                                                    | <span data-ttu-id="f3bbf-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3bbf-108">Type</span></span>        | <span data-ttu-id="f3bbf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3bbf-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3bbf-110">**Componente**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="f3bbf-111">string</span><span class="sxs-lookup"><span data-stu-id="f3bbf-111">string</span></span>      | <span data-ttu-id="f3bbf-112">Nombre del componente que registró el mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="f3bbf-113">**FileLine**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="f3bbf-114">string</span><span class="sxs-lookup"><span data-stu-id="f3bbf-114">string</span></span>      | <span data-ttu-id="f3bbf-115">Nombre del archivo de código fuente y la línea del archivo de código fuente que registró el mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="f3bbf-116">**FlagsName**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="f3bbf-117">string</span><span class="sxs-lookup"><span data-stu-id="f3bbf-117">string</span></span>      | <span data-ttu-id="f3bbf-118">El valor de marca que se pasa al proveedor cuando se habilitó.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="f3bbf-119">**Function**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="f3bbf-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3bbf-120">unsignedInt</span></span> | <span data-ttu-id="f3bbf-121">El nombre de la función que registró el mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="f3bbf-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="f3bbf-123">string</span><span class="sxs-lookup"><span data-stu-id="f3bbf-123">string</span></span>      | <span data-ttu-id="f3bbf-124">Valor de nivel que se pasa al proveedor cuando se habilitó.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="f3bbf-125">**Message**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="f3bbf-126">string</span><span class="sxs-lookup"><span data-stu-id="f3bbf-126">string</span></span>      | <span data-ttu-id="f3bbf-127">Cadena del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-127">The message string.</span></span> <span data-ttu-id="f3bbf-128">El XML contiene este elemento si el evento WPP especificó el campo FormattedString.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="f3bbf-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="f3bbf-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3bbf-130">unsignedInt</span></span> | <span data-ttu-id="f3bbf-131">El número de secuencia local o global del mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="f3bbf-132">**Subcomponente**</span><span class="sxs-lookup"><span data-stu-id="f3bbf-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="f3bbf-133">string</span><span class="sxs-lookup"><span data-stu-id="f3bbf-133">string</span></span>      | <span data-ttu-id="f3bbf-134">Nombre del subcomponente que registró el mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="f3bbf-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3bbf-135">Remarks</span></span>

<span data-ttu-id="f3bbf-136">Los elementos se incluyen solo si el proveedor ha establecido la variable de entorno% TRACE \_ format \_ prefix% para incluirlos.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="f3bbf-137">Para obtener más información sobre estos elementos, consulte prefijo de mensaje de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f3bbf-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3bbf-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3bbf-138">Requirements</span></span>



| <span data-ttu-id="f3bbf-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3bbf-139">Requirement</span></span> | <span data-ttu-id="f3bbf-140">Value</span><span class="sxs-lookup"><span data-stu-id="f3bbf-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3bbf-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3bbf-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f3bbf-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f3bbf-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3bbf-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3bbf-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f3bbf-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f3bbf-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





