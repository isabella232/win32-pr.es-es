---
title: Tipo complejo de showMessageType
description: Define los elementos que representan una acción que muestra un cuadro de mensaje.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- tipo complejo de showMessageType Programador de tareas
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996684"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="4b69d-104">Tipo complejo de showMessageType</span><span class="sxs-lookup"><span data-stu-id="4b69d-104">showMessageType Complex Type</span></span>

<span data-ttu-id="4b69d-105">Define los elementos que representan una acción que muestra un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b69d-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4b69d-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4b69d-106">Child elements</span></span>



| <span data-ttu-id="4b69d-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="4b69d-107">Element</span></span>                                                            | <span data-ttu-id="4b69d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b69d-108">Type</span></span>           | <span data-ttu-id="4b69d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b69d-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="4b69d-110">**Principal**</span><span class="sxs-lookup"><span data-stu-id="4b69d-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="4b69d-111">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="4b69d-111">nonEmptyString</span></span> | <span data-ttu-id="4b69d-112">Especifica el texto que se va a mostrar en el cuerpo del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b69d-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="4b69d-113">**Title**</span><span class="sxs-lookup"><span data-stu-id="4b69d-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="4b69d-114">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="4b69d-114">nonEmptyString</span></span> | <span data-ttu-id="4b69d-115">Especifica el título del cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4b69d-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="4b69d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b69d-116">Requirements</span></span>



| <span data-ttu-id="4b69d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b69d-117">Requirement</span></span> | <span data-ttu-id="4b69d-118">Value</span><span class="sxs-lookup"><span data-stu-id="4b69d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4b69d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b69d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4b69d-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4b69d-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4b69d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b69d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4b69d-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b69d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





