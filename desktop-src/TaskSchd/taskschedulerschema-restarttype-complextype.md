---
title: Tipo complejo de restartType
description: Define los elementos secundarios y la información de secuencia para el elemento RestartOnFailure.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- tipo complejo de restartType Programador de tareas
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535494"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="f33a5-104">Tipo complejo de restartType</span><span class="sxs-lookup"><span data-stu-id="f33a5-104">restartType Complex Type</span></span>

<span data-ttu-id="f33a5-105">Define los elementos secundarios y la información de secuencia para el elemento [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f33a5-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f33a5-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f33a5-106">Child elements</span></span>



| <span data-ttu-id="f33a5-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f33a5-107">Element</span></span>                                                              | <span data-ttu-id="f33a5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f33a5-108">Type</span></span> | <span data-ttu-id="f33a5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f33a5-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="f33a5-110">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="f33a5-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="f33a5-111">Número de intentos de reinicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="f33a5-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="f33a5-112">**Interval**</span><span class="sxs-lookup"><span data-stu-id="f33a5-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="f33a5-113">Cuánto tiempo se intentará iniciar la tarea.</span><span class="sxs-lookup"><span data-stu-id="f33a5-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="f33a5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f33a5-114">Requirements</span></span>



| <span data-ttu-id="f33a5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f33a5-115">Requirement</span></span> | <span data-ttu-id="f33a5-116">Value</span><span class="sxs-lookup"><span data-stu-id="f33a5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f33a5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f33a5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f33a5-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f33a5-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f33a5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f33a5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f33a5-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f33a5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f33a5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f33a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33a5-122">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f33a5-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f33a5-123">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="f33a5-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





