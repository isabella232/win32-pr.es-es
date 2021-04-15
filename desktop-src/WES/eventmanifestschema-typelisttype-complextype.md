---
title: Tipo complejo de TypeListType
description: Define los tipos que se usan en el manifiesto.
ms.assetid: e7ce0ecf-3bd0-49ab-82c7-dc28fd0e59a2
keywords:
- TypeListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- TypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61cec902684d7426a5951c12c4b319ae1ce29923
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695993"
---
# <a name="typelisttype-complex-type"></a><span data-ttu-id="bb221-104">Tipo complejo de TypeListType</span><span class="sxs-lookup"><span data-stu-id="bb221-104">TypeListType Complex Type</span></span>

<span data-ttu-id="bb221-105">Define los tipos que se usan en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="bb221-105">Defines the types that are used in the manifest.</span></span>

``` syntax
<xs:complexType name="TypeListType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="xmlTypes"
            type="XmlTypeListType"
         />
        <xs:element name="inTypes"
            type="InputTypeListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bb221-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb221-106">Child elements</span></span>



| <span data-ttu-id="bb221-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="bb221-107">Element</span></span>                                                               | <span data-ttu-id="bb221-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb221-108">Type</span></span>                                                                           | <span data-ttu-id="bb221-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb221-109">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb221-110">**Intypes**</span><span class="sxs-lookup"><span data-stu-id="bb221-110">**inTypes**</span></span>](eventmanifestschema-intypes-typelisttype-element.md)   | [<span data-ttu-id="bb221-111">**InputTypeListType**</span><span class="sxs-lookup"><span data-stu-id="bb221-111">**InputTypeListType**</span></span>](eventmanifestschema-inputtypelisttype-complextype.md) | <span data-ttu-id="bb221-112">Define una lista de tipos de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb221-112">Defines a list of input data types.</span></span><br/>                                                              |
| [<span data-ttu-id="bb221-113">**xmlTypes**</span><span class="sxs-lookup"><span data-stu-id="bb221-113">**xmlTypes**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md) | [<span data-ttu-id="bb221-114">**XmlTypeListType**</span><span class="sxs-lookup"><span data-stu-id="bb221-114">**XmlTypeListType**</span></span>](eventmanifestschema-xmltypelisttype-complextype.md)     | <span data-ttu-id="bb221-115">Define una lista de tipos de salida que el servicio usa para determinar cómo se representa un tipo de datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="bb221-115">Defines a list output types that the service uses to determine how to render an input data type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bb221-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb221-116">Requirements</span></span>



| <span data-ttu-id="bb221-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb221-117">Requirement</span></span> | <span data-ttu-id="bb221-118">Value</span><span class="sxs-lookup"><span data-stu-id="bb221-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb221-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb221-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb221-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb221-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb221-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb221-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb221-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb221-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





