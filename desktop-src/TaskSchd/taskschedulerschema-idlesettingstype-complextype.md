---
title: Tipo complejo de idleSettingsType
description: Define los elementos secundarios y la información de secuenciación para el elemento IdleSettings (settingsType).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- tipo complejo de idleSettingsType Programador de tareas
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685940"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="6be62-104">Tipo complejo de idleSettingsType</span><span class="sxs-lookup"><span data-stu-id="6be62-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="6be62-105">Define los elementos secundarios y la información de secuenciación para el elemento [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6be62-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6be62-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6be62-106">Child elements</span></span>



| <span data-ttu-id="6be62-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6be62-107">Element</span></span>                                                                                  | <span data-ttu-id="6be62-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6be62-108">Type</span></span>    | <span data-ttu-id="6be62-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6be62-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6be62-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="6be62-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="6be62-111">Especifica la cantidad de tiempo que se permite iniciar la tarea en una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6be62-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="6be62-112">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="6be62-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="6be62-113">boolean</span><span class="sxs-lookup"><span data-stu-id="6be62-113">boolean</span></span> | <span data-ttu-id="6be62-114">La tarea se reinicia en cuanto se inicia una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6be62-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="6be62-115">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="6be62-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="6be62-116">boolean</span><span class="sxs-lookup"><span data-stu-id="6be62-116">boolean</span></span> | <span data-ttu-id="6be62-117">Especifica que la tarea se termina si la condición de inactividad finaliza antes de que se supere la duración de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6be62-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="6be62-118">**WaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="6be62-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="6be62-119">Especifica la cantidad de tiempo que hay que esperar a que se inicie una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6be62-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="6be62-120">Si no se especifica ningún valor para este elemento, el servicio Programador de tareas esperará indefinidamente a que se produzca una condición de inactividad.</span><span class="sxs-lookup"><span data-stu-id="6be62-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6be62-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6be62-121">Requirements</span></span>



| <span data-ttu-id="6be62-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be62-122">Requirement</span></span> | <span data-ttu-id="6be62-123">Value</span><span class="sxs-lookup"><span data-stu-id="6be62-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6be62-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6be62-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6be62-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6be62-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6be62-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6be62-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6be62-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6be62-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6be62-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6be62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be62-129">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6be62-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="6be62-130">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="6be62-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





