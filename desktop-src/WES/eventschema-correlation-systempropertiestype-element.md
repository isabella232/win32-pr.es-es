---
title: Elemento Correlation (SystemPropertiesType)
description: Los identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Elemento de correlación EventLog
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996841"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="e85ba-104">Elemento Correlation (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="e85ba-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="e85ba-105">Los identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.</span><span class="sxs-lookup"><span data-stu-id="e85ba-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="e85ba-106">El elemento de **correlación** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e85ba-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="e85ba-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="e85ba-107">Attributes</span></span>



| <span data-ttu-id="e85ba-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e85ba-108">Name</span></span>              | <span data-ttu-id="e85ba-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e85ba-109">Type</span></span>                                                | <span data-ttu-id="e85ba-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e85ba-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85ba-111">Identificador de actividad</span><span class="sxs-lookup"><span data-stu-id="e85ba-111">ActivityID</span></span>        | [<span data-ttu-id="e85ba-112">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="e85ba-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="e85ba-113">Identificador único global que identifica la actividad actual.</span><span class="sxs-lookup"><span data-stu-id="e85ba-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="e85ba-114">Los eventos que se publican con este identificador forman parte de la misma actividad.</span><span class="sxs-lookup"><span data-stu-id="e85ba-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="e85ba-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="e85ba-115">RelatedActivityID</span></span> | [<span data-ttu-id="e85ba-116">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="e85ba-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="e85ba-117">Identificador único global que identifica la actividad a la que se transfirió el control.</span><span class="sxs-lookup"><span data-stu-id="e85ba-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="e85ba-118">Los eventos relacionados tendrían este identificador como su identificador ActivityID.</span><span class="sxs-lookup"><span data-stu-id="e85ba-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e85ba-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e85ba-119">Requirements</span></span>



| <span data-ttu-id="e85ba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e85ba-120">Requirement</span></span> | <span data-ttu-id="e85ba-121">Value</span><span class="sxs-lookup"><span data-stu-id="e85ba-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e85ba-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e85ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e85ba-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e85ba-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e85ba-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e85ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e85ba-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e85ba-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e85ba-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e85ba-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="e85ba-127">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="e85ba-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="e85ba-128">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="e85ba-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





