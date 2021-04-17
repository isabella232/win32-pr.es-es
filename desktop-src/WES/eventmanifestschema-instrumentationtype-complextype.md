---
title: Tipo complejo InstrumentationType
description: Define el contenido de la sección de instrumentación del manifiesto.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Registro de eventos de tipo complejo InstrumentationType
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696030"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="dc2e0-104">Tipo complejo InstrumentationType</span><span class="sxs-lookup"><span data-stu-id="dc2e0-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="dc2e0-105">Define el contenido de la sección de instrumentación del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="dc2e0-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="dc2e0-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc2e0-106">Child elements</span></span>



| <span data-ttu-id="dc2e0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="dc2e0-107">Element</span></span>                                                                  | <span data-ttu-id="dc2e0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc2e0-108">Type</span></span>                                                             | <span data-ttu-id="dc2e0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc2e0-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="dc2e0-110">**events**</span><span class="sxs-lookup"><span data-stu-id="dc2e0-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="dc2e0-111">**EventsType**</span><span class="sxs-lookup"><span data-stu-id="dc2e0-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="dc2e0-112">Contiene una lista de proveedores que el manifiesto define.</span><span class="sxs-lookup"><span data-stu-id="dc2e0-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dc2e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc2e0-113">Requirements</span></span>



| <span data-ttu-id="dc2e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc2e0-114">Requirement</span></span> | <span data-ttu-id="dc2e0-115">Value</span><span class="sxs-lookup"><span data-stu-id="dc2e0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dc2e0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc2e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dc2e0-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dc2e0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dc2e0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc2e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dc2e0-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc2e0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





