---
title: Elemento System (EventType)
description: Contiene información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- EventLog (elemento del sistema)
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695864"
---
# <a name="system-eventtype-element"></a><span data-ttu-id="42d49-104">Elemento System (EventType)</span><span class="sxs-lookup"><span data-stu-id="42d49-104">System (EventType) Element</span></span>

<span data-ttu-id="42d49-105">Contiene información que identifica al proveedor y cómo se habilitó, el evento, el canal en el que se escribió el evento e información del sistema, como los identificadores de proceso y de subproceso.</span><span class="sxs-lookup"><span data-stu-id="42d49-105">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

<span data-ttu-id="42d49-106">El elemento **System** se define mediante el tipo complejo de [**EventType**](eventschema-eventtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="42d49-106">The **System** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d49-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d49-107">Requirements</span></span>



| <span data-ttu-id="42d49-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d49-108">Requirement</span></span> | <span data-ttu-id="42d49-109">Value</span><span class="sxs-lookup"><span data-stu-id="42d49-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42d49-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42d49-110">Minimum supported client</span></span><br/> | <span data-ttu-id="42d49-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="42d49-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42d49-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42d49-112">Minimum supported server</span></span><br/> | <span data-ttu-id="42d49-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="42d49-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42d49-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="42d49-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="42d49-115">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="42d49-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="42d49-116">**evento**</span><span class="sxs-lookup"><span data-stu-id="42d49-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





