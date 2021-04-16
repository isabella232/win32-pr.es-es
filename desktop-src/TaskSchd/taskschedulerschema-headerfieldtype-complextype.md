---
title: Tipo complejo de headerFieldType
description: Define los elementos que se usan para crear un campo de encabezado en un mensaje de correo electrónico.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- tipo complejo de headerFieldType Programador de tareas
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676683"
---
# <a name="headerfieldtype-complex-type"></a><span data-ttu-id="eaef9-104">Tipo complejo de headerFieldType</span><span class="sxs-lookup"><span data-stu-id="eaef9-104">headerFieldType Complex Type</span></span>

<span data-ttu-id="eaef9-105">Define los elementos que se usan para crear un campo de encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="eaef9-105">Defines the elements that are used to create a header field in an email message.</span></span>

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="eaef9-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eaef9-106">Child elements</span></span>



| <span data-ttu-id="eaef9-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="eaef9-107">Element</span></span>                                                            | <span data-ttu-id="eaef9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="eaef9-108">Type</span></span>                                                                    | <span data-ttu-id="eaef9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaef9-109">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="eaef9-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="eaef9-110">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="eaef9-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="eaef9-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="eaef9-112">Especifica el nombre del campo de encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="eaef9-112">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="eaef9-113">**Value**</span><span class="sxs-lookup"><span data-stu-id="eaef9-113">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="eaef9-114">**string**</span><span class="sxs-lookup"><span data-stu-id="eaef9-114">**string**</span></span>                                                              | <span data-ttu-id="eaef9-115">Especifica el valor de un campo de encabezado en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="eaef9-115">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="eaef9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eaef9-116">Requirements</span></span>



| <span data-ttu-id="eaef9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaef9-117">Requirement</span></span> | <span data-ttu-id="eaef9-118">Value</span><span class="sxs-lookup"><span data-stu-id="eaef9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eaef9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaef9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eaef9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="eaef9-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eaef9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eaef9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eaef9-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="eaef9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





