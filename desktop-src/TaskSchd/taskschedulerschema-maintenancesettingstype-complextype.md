---
title: Tipo complejo de maintenanceSettingsType
description: Define los elementos secundarios y la información de secuenciación para el elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- tipo complejo de maintenanceSettingsType Programador de tareas
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803223"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="07b84-104">Tipo complejo de maintenanceSettingsType</span><span class="sxs-lookup"><span data-stu-id="07b84-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="07b84-105">Define los elementos secundarios y la información de secuenciación para el elemento [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="07b84-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="07b84-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07b84-106">Child elements</span></span>



| <span data-ttu-id="07b84-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="07b84-107">Element</span></span>                                                                        | <span data-ttu-id="07b84-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="07b84-108">Type</span></span>    | <span data-ttu-id="07b84-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="07b84-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07b84-110">**Fecha límite**</span><span class="sxs-lookup"><span data-stu-id="07b84-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="07b84-111">Especifica la cantidad de tiempo después de la cual el programador de tareas intentará iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento normal.</span><span class="sxs-lookup"><span data-stu-id="07b84-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="07b84-112">**Exclusivo**</span><span class="sxs-lookup"><span data-stu-id="07b84-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="07b84-113">boolean</span><span class="sxs-lookup"><span data-stu-id="07b84-113">boolean</span></span> | <span data-ttu-id="07b84-114">Si se establece en true, la tarea se iniciará exclusivamente entre otras tareas de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="07b84-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="07b84-115">**Período**</span><span class="sxs-lookup"><span data-stu-id="07b84-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="07b84-116">Especifica la frecuencia con que se debe iniciar la tarea durante el mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="07b84-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="07b84-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07b84-117">Requirements</span></span>



| <span data-ttu-id="07b84-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b84-118">Requirement</span></span> | <span data-ttu-id="07b84-119">Value</span><span class="sxs-lookup"><span data-stu-id="07b84-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07b84-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07b84-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="07b84-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="07b84-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07b84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07b84-123">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="07b84-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07b84-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="07b84-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b84-125">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="07b84-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="07b84-126">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="07b84-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





