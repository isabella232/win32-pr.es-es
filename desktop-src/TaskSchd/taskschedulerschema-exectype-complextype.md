---
title: Tipo complejo de execType
description: Define los elementos secundarios y la información de secuenciación del elemento exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- tipo complejo de execType Programador de tareas
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489544"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="8b4ab-104">Tipo complejo de execType</span><span class="sxs-lookup"><span data-stu-id="8b4ab-104">execType Complex Type</span></span>

<span data-ttu-id="8b4ab-105">Define los elementos secundarios y la información de secuenciación del elemento [**exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8b4ab-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="8b4ab-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b4ab-106">Child elements</span></span>



| <span data-ttu-id="8b4ab-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8b4ab-107">Element</span></span>                                                                           | <span data-ttu-id="8b4ab-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b4ab-108">Type</span></span>                                                        | <span data-ttu-id="8b4ab-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b4ab-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b4ab-110">**Argumentos**</span><span class="sxs-lookup"><span data-stu-id="8b4ab-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="8b4ab-111">**string**</span><span class="sxs-lookup"><span data-stu-id="8b4ab-111">**string**</span></span>                                                  | <span data-ttu-id="8b4ab-112">Especifica los argumentos asociados con la operación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8b4ab-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="8b4ab-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="8b4ab-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="8b4ab-114">**pathType**</span><span class="sxs-lookup"><span data-stu-id="8b4ab-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="8b4ab-115">Especifica el archivo ejecutable o el documento que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="8b4ab-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="8b4ab-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="8b4ab-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="8b4ab-117">**pathType**</span><span class="sxs-lookup"><span data-stu-id="8b4ab-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="8b4ab-118">Especifica el directorio donde existe el archivo ejecutable o los archivos utilizados por el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="8b4ab-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8b4ab-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b4ab-119">Requirements</span></span>



| <span data-ttu-id="8b4ab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b4ab-120">Requirement</span></span> | <span data-ttu-id="8b4ab-121">Value</span><span class="sxs-lookup"><span data-stu-id="8b4ab-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b4ab-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b4ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b4ab-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8b4ab-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8b4ab-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b4ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b4ab-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b4ab-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8b4ab-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b4ab-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b4ab-127">Tipos complejos de esquema Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8b4ab-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="8b4ab-128">Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8b4ab-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





