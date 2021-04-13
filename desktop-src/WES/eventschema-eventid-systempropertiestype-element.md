---
title: EventID (SystemPropertiesType), elemento
description: Identificador que el proveedor usó para identificar el evento.
ms.assetid: 2d5ac44b-4157-4b87-bd8f-e992e85dd0b1
keywords:
- Elemento EventID EventLog
topic_type:
- apiref
api_name:
- EventID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac1b2edd671f06d88c8c51b49c16f759fd05e087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489490"
---
# <a name="eventid-systempropertiestype-element"></a><span data-ttu-id="75469-104">EventID (SystemPropertiesType), elemento</span><span class="sxs-lookup"><span data-stu-id="75469-104">EventID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="75469-105">Identificador que el proveedor usó para identificar el evento.</span><span class="sxs-lookup"><span data-stu-id="75469-105">The identifier that the provider used to identify the event.</span></span>

``` syntax
<xs:element name="EventID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedInt"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="75469-106">El elemento **EventID** se define mediante el tipo complejo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75469-106">The **EventID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="75469-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75469-107">Requirements</span></span>



| <span data-ttu-id="75469-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="75469-108">Requirement</span></span> | <span data-ttu-id="75469-109">Value</span><span class="sxs-lookup"><span data-stu-id="75469-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75469-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75469-110">Minimum supported client</span></span><br/> | <span data-ttu-id="75469-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="75469-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75469-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75469-112">Minimum supported server</span></span><br/> | <span data-ttu-id="75469-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="75469-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75469-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="75469-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="75469-115">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="75469-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="75469-116">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="75469-116">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





