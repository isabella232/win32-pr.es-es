---
title: Tipo complejo de comHandlerType
description: Define los elementos secundarios y la información de secuenciación para el elemento comhandler.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- tipo complejo de comHandlerType Programador de tareas
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079160"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="cb5d9-104">Tipo complejo de comHandlerType</span><span class="sxs-lookup"><span data-stu-id="cb5d9-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="cb5d9-105">Define los elementos secundarios y la información de secuenciación para el elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="cb5d9-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cb5d9-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb5d9-106">Child elements</span></span>



| <span data-ttu-id="cb5d9-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cb5d9-107">Element</span></span>                                                               | <span data-ttu-id="cb5d9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb5d9-108">Type</span></span>                                                         | <span data-ttu-id="cb5d9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb5d9-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="cb5d9-110">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="cb5d9-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="cb5d9-111">**guidType**</span><span class="sxs-lookup"><span data-stu-id="cb5d9-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="cb5d9-112">Especifica el identificador de la clase de controlador.</span><span class="sxs-lookup"><span data-stu-id="cb5d9-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="cb5d9-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="cb5d9-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="cb5d9-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cb5d9-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="cb5d9-115">Especifica datos adicionales asociados al controlador.</span><span class="sxs-lookup"><span data-stu-id="cb5d9-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cb5d9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb5d9-116">Requirements</span></span>



| <span data-ttu-id="cb5d9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5d9-117">Requirement</span></span> | <span data-ttu-id="cb5d9-118">Value</span><span class="sxs-lookup"><span data-stu-id="cb5d9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb5d9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb5d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5d9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb5d9-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb5d9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb5d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5d9-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb5d9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb5d9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb5d9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5d9-124">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="cb5d9-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="cb5d9-125">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="cb5d9-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





