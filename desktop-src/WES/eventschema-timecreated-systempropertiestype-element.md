---
title: Elemento TimeCreated (SystemPropertiesType)
description: Marca de tiempo que identifica Cuándo se registró el evento.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- Elemento TimeCreated EventLog
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996578"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="ae027-104">Elemento TimeCreated (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="ae027-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="ae027-105">Marca de tiempo que identifica Cuándo se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="ae027-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ae027-106">El elemento **TimeCreated** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae027-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="ae027-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae027-107">Attributes</span></span>



| <span data-ttu-id="ae027-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae027-108">Name</span></span>       | <span data-ttu-id="ae027-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae027-109">Type</span></span>     | <span data-ttu-id="ae027-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae027-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="ae027-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="ae027-111">SystemTime</span></span> | <span data-ttu-id="ae027-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="ae027-112">dateTime</span></span> | <span data-ttu-id="ae027-113">Hora del sistema en la que se registró el evento.</span><span class="sxs-lookup"><span data-stu-id="ae027-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ae027-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae027-114">Requirements</span></span>



| <span data-ttu-id="ae027-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae027-115">Requirement</span></span> | <span data-ttu-id="ae027-116">Value</span><span class="sxs-lookup"><span data-stu-id="ae027-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae027-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae027-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ae027-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ae027-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae027-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae027-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ae027-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae027-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae027-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae027-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae027-122">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="ae027-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ae027-123">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="ae027-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





