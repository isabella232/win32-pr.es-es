---
title: Elemento Provider (SystemPropertiesType)
description: Identifica el proveedor que registró el evento.
ms.assetid: 4560c938-4e2a-40d5-97f9-85a38141ac8f
keywords:
- EventLog (elemento del proveedor)
topic_type:
- apiref
api_name:
- Provider
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3dc6ae072ed6491915067bea4395a1a84369b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079025"
---
# <a name="provider-systempropertiestype-element"></a><span data-ttu-id="a7a8b-104">Elemento Provider (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="a7a8b-104">Provider (SystemPropertiesType) Element</span></span>

<span data-ttu-id="a7a8b-105">Identifica el proveedor que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="a7a8b-105">Identifies the provider that logged the event.</span></span>

``` syntax
<xs:element name="Provider">
    <xs:complexType>
        <xs:attribute name="Name"
            type="anyURI"
            use="optional"
         />
        <xs:attribute name="Guid"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="EventSourceName"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a7a8b-106">El elemento de **proveedor** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a7a8b-106">The **Provider** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="a7a8b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="a7a8b-107">Attributes</span></span>



| <span data-ttu-id="a7a8b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7a8b-108">Name</span></span>            | <span data-ttu-id="a7a8b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7a8b-109">Type</span></span>                                                | <span data-ttu-id="a7a8b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7a8b-110">Description</span></span>                                                                                                                                        |
|-----------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7a8b-111">EventSourceName</span><span class="sxs-lookup"><span data-stu-id="a7a8b-111">EventSourceName</span></span> | <span data-ttu-id="a7a8b-112">string</span><span class="sxs-lookup"><span data-stu-id="a7a8b-112">string</span></span>                                              | <span data-ttu-id="a7a8b-113">Nombre del origen de eventos que publicó el evento (si el origen del evento es de la API de [registro de eventos](/windows/desktop/EventLog/event-logging) heredada).</span><span class="sxs-lookup"><span data-stu-id="a7a8b-113">The name of the event source that published the event (if the event source is from the legacy [Event Logging](/windows/desktop/EventLog/event-logging) API).</span></span><br/> |
| <span data-ttu-id="a7a8b-114">Guid</span><span class="sxs-lookup"><span data-stu-id="a7a8b-114">Guid</span></span>            | [<span data-ttu-id="a7a8b-115">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="a7a8b-115">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="a7a8b-116">Identificador único global que identifica de forma única el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a7a8b-116">The globally unique identifier that uniquely identifies the provider.</span></span><br/>                                                                   |
| <span data-ttu-id="a7a8b-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7a8b-117">Name</span></span>            | <span data-ttu-id="a7a8b-118">anyURI</span><span class="sxs-lookup"><span data-stu-id="a7a8b-118">anyURI</span></span>                                              | <span data-ttu-id="a7a8b-119">Nombre del proveedor de eventos que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="a7a8b-119">The name of the event provider that logged the event.</span></span><br/>                                                                                   |



## <a name="requirements"></a><span data-ttu-id="a7a8b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7a8b-120">Requirements</span></span>



| <span data-ttu-id="a7a8b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7a8b-121">Requirement</span></span> | <span data-ttu-id="a7a8b-122">Value</span><span class="sxs-lookup"><span data-stu-id="a7a8b-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a7a8b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7a8b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7a8b-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a7a8b-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a7a8b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7a8b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7a8b-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7a8b-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a7a8b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7a8b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a7a8b-128">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="a7a8b-128">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a7a8b-129">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="a7a8b-129">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

