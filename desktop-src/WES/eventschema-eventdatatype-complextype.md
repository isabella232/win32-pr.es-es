---
title: Tipo complejo de EventDataType
description: Define los elementos de datos de evento y las estructuras que contienen los datos de evento.
ms.assetid: 9531163f-34ce-4673-b2d8-636042915c73
keywords:
- EventDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- EventDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a93695db477ebb0c7b5652419198f8f5c6370dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801430"
---
# <a name="eventdatatype-complex-type"></a><span data-ttu-id="d9fa4-104">Tipo complejo de EventDataType</span><span class="sxs-lookup"><span data-stu-id="d9fa4-104">EventDataType Complex Type</span></span>

<span data-ttu-id="d9fa4-105">Define los elementos de datos de evento y las estructuras que contienen los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="d9fa4-105">Defines the event data items and structures that contains the event data.</span></span>

``` syntax
<xs:complexType name="EventDataType">
    <xs:sequence>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="Data"
                type="DataType"
             />
            <xs:element name="ComplexData"
                type="ComplexDataType"
             />
        </xs:choice>
        <xs:element name="Binary"
            type="hexBinary"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d9fa4-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d9fa4-106">Child elements</span></span>



| <span data-ttu-id="d9fa4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d9fa4-107">Element</span></span>                                                              | <span data-ttu-id="d9fa4-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9fa4-108">Type</span></span>                                                               | <span data-ttu-id="d9fa4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9fa4-109">Description</span></span>                                                                                          |
|----------------------------------------------------------------------|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9fa4-110">**Binary**</span><span class="sxs-lookup"><span data-stu-id="d9fa4-110">**Binary**</span></span>](eventschema-binary-eventdatatype-element.md)           | <span data-ttu-id="d9fa4-111">hexBinary</span><span class="sxs-lookup"><span data-stu-id="d9fa4-111">hexBinary</span></span>                                                          | <span data-ttu-id="d9fa4-112">Un BLOB de datos binarios para los eventos que se escriben mediante el [registro de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="d9fa4-112">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span><br/> |
| [<span data-ttu-id="d9fa4-113">**ComplexData**</span><span class="sxs-lookup"><span data-stu-id="d9fa4-113">**ComplexData**</span></span>](eventschema-complexdata-eventdatatype-element.md) | [<span data-ttu-id="d9fa4-114">**ComplexDataType**</span><span class="sxs-lookup"><span data-stu-id="d9fa4-114">**ComplexDataType**</span></span>](eventschema-complexdatatype-complextype.md) | <span data-ttu-id="d9fa4-115">Estructura que se define en la plantilla para el evento.</span><span class="sxs-lookup"><span data-stu-id="d9fa4-115">A structure that is defined in the template for the event.</span></span><br/>                                |
| [<span data-ttu-id="d9fa4-116">**Data**</span><span class="sxs-lookup"><span data-stu-id="d9fa4-116">**Data**</span></span>](eventschema-data-eventdatatype-element.md)               | [<span data-ttu-id="d9fa4-117">**DataType**</span><span class="sxs-lookup"><span data-stu-id="d9fa4-117">**DataType**</span></span>](eventschema-datafieldtype-complextype.md)          | <span data-ttu-id="d9fa4-118">Un elemento de datos de nivel superior que se define en la plantilla para el evento.</span><span class="sxs-lookup"><span data-stu-id="d9fa4-118">A top-level data item that is defined in the template for the event.</span></span><br/>                      |



## <a name="attributes"></a><span data-ttu-id="d9fa4-119">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9fa4-119">Attributes</span></span>



| <span data-ttu-id="d9fa4-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9fa4-120">Name</span></span> | <span data-ttu-id="d9fa4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9fa4-121">Type</span></span>   | <span data-ttu-id="d9fa4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9fa4-122">Description</span></span>                                                       |
|------|--------|-------------------------------------------------------------------|
| <span data-ttu-id="d9fa4-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9fa4-123">Name</span></span> | <span data-ttu-id="d9fa4-124">string</span><span class="sxs-lookup"><span data-stu-id="d9fa4-124">string</span></span> | <span data-ttu-id="d9fa4-125">Nombre de la plantilla que contiene los elementos de datos.</span><span class="sxs-lookup"><span data-stu-id="d9fa4-125">The name of the template that contains the data items.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d9fa4-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9fa4-126">Remarks</span></span>

<span data-ttu-id="d9fa4-127">La función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa matrices y estructuras como blobs binarios.</span><span class="sxs-lookup"><span data-stu-id="d9fa4-127">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders arrays and structures as binary blobs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9fa4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9fa4-128">Requirements</span></span>



| <span data-ttu-id="d9fa4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9fa4-129">Requirement</span></span> | <span data-ttu-id="d9fa4-130">Value</span><span class="sxs-lookup"><span data-stu-id="d9fa4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9fa4-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9fa4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d9fa4-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9fa4-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9fa4-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9fa4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d9fa4-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9fa4-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

