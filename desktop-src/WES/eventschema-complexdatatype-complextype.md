---
title: Tipo complejo de ComplexDataType
description: Define una estructura que contiene uno o más elementos de datos.
ms.assetid: 1495daef-1dfd-4f62-9543-569cc74102f4
keywords:
- ComplexDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- ComplexDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 598f2cc02f1e3675ff0c8fd6eae7f9a5e02b9407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695992"
---
# <a name="complexdatatype-complex-type"></a><span data-ttu-id="feb7a-104">Tipo complejo de ComplexDataType</span><span class="sxs-lookup"><span data-stu-id="feb7a-104">ComplexDataType Complex Type</span></span>

<span data-ttu-id="feb7a-105">Define una estructura que contiene uno o más elementos de datos.</span><span class="sxs-lookup"><span data-stu-id="feb7a-105">Defines a structure that contains one or more data items.</span></span>

``` syntax
<xs:complexType name="ComplexDataType">
    <xs:sequence>
        <xs:element name="Data"
            type="DataType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="Name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="feb7a-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="feb7a-106">Child elements</span></span>



| <span data-ttu-id="feb7a-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="feb7a-107">Element</span></span>                                                  | <span data-ttu-id="feb7a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="feb7a-108">Type</span></span>                                                      | <span data-ttu-id="feb7a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb7a-109">Description</span></span>                                                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feb7a-110">**Data**</span><span class="sxs-lookup"><span data-stu-id="feb7a-110">**Data**</span></span>](eventschema-data-complexdatatype-element.md) | [<span data-ttu-id="feb7a-111">**DataType**</span><span class="sxs-lookup"><span data-stu-id="feb7a-111">**DataType**</span></span>](eventschema-datafieldtype-complextype.md) | <span data-ttu-id="feb7a-112">Lista de elementos de datos de la estructura.</span><span class="sxs-lookup"><span data-stu-id="feb7a-112">The list of data items in the structure.</span></span> <span data-ttu-id="feb7a-113">La lista de elementos está en el mismo orden que se define en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="feb7a-113">The list of items are in the same order as defined in the template.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="feb7a-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="feb7a-114">Attributes</span></span>



| <span data-ttu-id="feb7a-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="feb7a-115">Name</span></span> | <span data-ttu-id="feb7a-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="feb7a-116">Type</span></span>   | <span data-ttu-id="feb7a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="feb7a-117">Description</span></span>                                                                                                                                                                                                                  |
|------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb7a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="feb7a-118">Name</span></span> | <span data-ttu-id="feb7a-119">string</span><span class="sxs-lookup"><span data-stu-id="feb7a-119">string</span></span> | <span data-ttu-id="feb7a-120">Nombre de la estructura.</span><span class="sxs-lookup"><span data-stu-id="feb7a-120">The name of the structure.</span></span> <span data-ttu-id="feb7a-121">Este es el nombre que se especifica cuando se define la estructura en la plantilla (vea el tipo complejo de [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="feb7a-121">This is the name that is specified when you defined the structure in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="feb7a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="feb7a-122">Remarks</span></span>

<span data-ttu-id="feb7a-123">La función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) representa el contenido de una estructura como un BLOB binario; la función no representa los elementos de datos individuales de la estructura.</span><span class="sxs-lookup"><span data-stu-id="feb7a-123">The [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function renders the contents of a structure as a binary blob; the function does not render the individual data items of the structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb7a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb7a-124">Requirements</span></span>



| <span data-ttu-id="feb7a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb7a-125">Requirement</span></span> | <span data-ttu-id="feb7a-126">Value</span><span class="sxs-lookup"><span data-stu-id="feb7a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="feb7a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feb7a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="feb7a-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="feb7a-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="feb7a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="feb7a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="feb7a-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="feb7a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





