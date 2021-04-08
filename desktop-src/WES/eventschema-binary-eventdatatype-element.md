---
title: Elemento binario (EventDataType)
description: Un BLOB de datos binarios para los eventos que se escriben mediante el registro de eventos.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- EventLog del elemento binario
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078882"
---
# <a name="binary-eventdatatype-element"></a><span data-ttu-id="95e2e-104">Elemento binario (EventDataType)</span><span class="sxs-lookup"><span data-stu-id="95e2e-104">Binary (EventDataType) Element</span></span>

<span data-ttu-id="95e2e-105">Un BLOB de datos binarios para los eventos que se escriben mediante el [registro de eventos](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="95e2e-105">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

<span data-ttu-id="95e2e-106">El elemento **binario** se define mediante el tipo complejo [**EventDataType**](eventschema-eventdatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="95e2e-106">The **Binary** element is defined by the [**EventDataType**](eventschema-eventdatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="95e2e-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95e2e-107">Requirements</span></span>



| <span data-ttu-id="95e2e-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="95e2e-108">Requirement</span></span> | <span data-ttu-id="95e2e-109">Value</span><span class="sxs-lookup"><span data-stu-id="95e2e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95e2e-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95e2e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="95e2e-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95e2e-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95e2e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="95e2e-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="95e2e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95e2e-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="95e2e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="95e2e-115">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="95e2e-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="95e2e-116">**EventData (EventType)**</span><span class="sxs-lookup"><span data-stu-id="95e2e-116">**EventData (EventType)**</span></span>](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

