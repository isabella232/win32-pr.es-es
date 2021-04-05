---
title: Tipo complejo de registrationInfoType
description: Define los elementos secundarios y la información de secuenciación para el elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- tipo complejo de registrationInfoType Programador de tareas
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996685"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="b785b-104">Tipo complejo de registrationInfoType</span><span class="sxs-lookup"><span data-stu-id="b785b-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="b785b-105">Define los elementos secundarios y la información de secuenciación para el elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b785b-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b785b-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b785b-106">Child elements</span></span>



| <span data-ttu-id="b785b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="b785b-107">Element</span></span>                                                                                           | <span data-ttu-id="b785b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b785b-108">Type</span></span>     | <span data-ttu-id="b785b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b785b-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b785b-110">**Autor**</span><span class="sxs-lookup"><span data-stu-id="b785b-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="b785b-111">string</span><span class="sxs-lookup"><span data-stu-id="b785b-111">string</span></span>   | <span data-ttu-id="b785b-112">Especifica el autor de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="b785b-113">**Posteriormente**</span><span class="sxs-lookup"><span data-stu-id="b785b-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="b785b-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="b785b-114">dateTime</span></span> | <span data-ttu-id="b785b-115">Especifica la fecha y hora en que se registra la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="b785b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b785b-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="b785b-117">string</span><span class="sxs-lookup"><span data-stu-id="b785b-117">string</span></span>   | <span data-ttu-id="b785b-118">Especifica la descripción de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="b785b-119">**Documentación**</span><span class="sxs-lookup"><span data-stu-id="b785b-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="b785b-120">string</span><span class="sxs-lookup"><span data-stu-id="b785b-120">string</span></span>   | <span data-ttu-id="b785b-121">Especifica cualquier documentación adicional para la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="b785b-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b785b-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="b785b-123">string</span><span class="sxs-lookup"><span data-stu-id="b785b-123">string</span></span>   | <span data-ttu-id="b785b-124">Especifica el descriptor de seguridad de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="b785b-125">**Fuentes**</span><span class="sxs-lookup"><span data-stu-id="b785b-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="b785b-126">string</span><span class="sxs-lookup"><span data-stu-id="b785b-126">string</span></span>   | <span data-ttu-id="b785b-127">Especifica el origen desde el que se originó la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-127">Specifies where the task originated from.</span></span> <span data-ttu-id="b785b-128">Por ejemplo, de un componente, servicio, aplicación o usuario.</span><span class="sxs-lookup"><span data-stu-id="b785b-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="b785b-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="b785b-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="b785b-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="b785b-130">anyURI</span></span>   | <span data-ttu-id="b785b-131">Especifica el URI de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="b785b-132">**Versión**</span><span class="sxs-lookup"><span data-stu-id="b785b-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="b785b-133">string</span><span class="sxs-lookup"><span data-stu-id="b785b-133">string</span></span>   | <span data-ttu-id="b785b-134">Especifica el número de versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="b785b-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="b785b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b785b-135">Requirements</span></span>



| <span data-ttu-id="b785b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b785b-136">Requirement</span></span> | <span data-ttu-id="b785b-137">Value</span><span class="sxs-lookup"><span data-stu-id="b785b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b785b-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b785b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b785b-139">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b785b-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b785b-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b785b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b785b-141">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b785b-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b785b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b785b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b785b-143">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b785b-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b785b-144">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="b785b-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





