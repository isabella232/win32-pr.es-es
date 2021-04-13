---
title: Elemento EventRecordID (SystemPropertiesType)
description: Número de registro asignado al evento cuando se registró.
ms.assetid: d042de4d-e532-432e-bba2-1876a26860a4
keywords:
- Elemento EventRecordID EventLog
topic_type:
- apiref
api_name:
- EventRecordID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb937d075bc0ff5fc1cf8bf1335d1274aee4fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421988"
---
# <a name="eventrecordid-systempropertiestype-element"></a><span data-ttu-id="5e976-104">Elemento EventRecordID (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="5e976-104">EventRecordID (SystemPropertiesType) Element</span></span>

<span data-ttu-id="5e976-105">Número de registro asignado al evento cuando se registró.</span><span class="sxs-lookup"><span data-stu-id="5e976-105">The record number assigned to the event when it was logged.</span></span>

``` syntax
<xs:element name="EventRecordID">
    <xs:complexType>
        <xs:simpleContent>
            <xs:extension
                base="unsignedLong"
             />
        </xs:simpleContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="5e976-106">El elemento **EventRecordID** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5e976-106">The **EventRecordID** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e976-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e976-107">Requirements</span></span>



| <span data-ttu-id="5e976-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e976-108">Requirement</span></span> | <span data-ttu-id="5e976-109">Value</span><span class="sxs-lookup"><span data-stu-id="5e976-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e976-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e976-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5e976-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e976-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e976-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e976-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5e976-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e976-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





