---
title: Tipo complejo de tipo de archivo (registro de eventos de Windows)
description: Define un elemento de datos.
ms.assetid: f3b7de63-1ac1-429d-9e36-1f13c26c9618
keywords:
- EventLog (tipo complejo de tipo de texto)
topic_type:
- apiref
api_name:
- DataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d3ac6e545cbe8567bbe041568c442f762743ad0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359809"
---
# <a name="datatype-complex-type"></a><span data-ttu-id="bb28f-104">Tipo complejo DataType</span><span class="sxs-lookup"><span data-stu-id="bb28f-104">DataType Complex Type</span></span>

<span data-ttu-id="bb28f-105">Define un elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="bb28f-105">Defines a data item.</span></span>

``` syntax
<xs:complexType name="DataType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="Name"
                type="string"
                use="optional"
             />
            <xs:attribute name="Type"
                type="QName"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="bb28f-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb28f-106">Attributes</span></span>



| <span data-ttu-id="bb28f-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb28f-107">Name</span></span> | <span data-ttu-id="bb28f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb28f-108">Type</span></span>   | <span data-ttu-id="bb28f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb28f-109">Description</span></span>                                                                                                                                                              |
|------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb28f-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb28f-110">Name</span></span> | <span data-ttu-id="bb28f-111">string</span><span class="sxs-lookup"><span data-stu-id="bb28f-111">string</span></span> | <span data-ttu-id="bb28f-112">El nombre de un elemento de datos que se definió en la plantilla (vea el tipo complejo de [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="bb28f-112">The name of a data item that was defined in the template (see the [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) complex type).</span></span><br/> |
| <span data-ttu-id="bb28f-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb28f-113">Type</span></span> | <span data-ttu-id="bb28f-114">QName</span><span class="sxs-lookup"><span data-stu-id="bb28f-114">QName</span></span>  | <span data-ttu-id="bb28f-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bb28f-115">Not used.</span></span><br/>                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="bb28f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb28f-116">Remarks</span></span>

<span data-ttu-id="bb28f-117">El elemento de datos puede ser un elemento de datos de nivel superior o un elemento de datos de una estructura.</span><span class="sxs-lookup"><span data-stu-id="bb28f-117">The data item can be a top-level data item or a data item in a structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb28f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb28f-118">Requirements</span></span>



| <span data-ttu-id="bb28f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb28f-119">Requirement</span></span> | <span data-ttu-id="bb28f-120">Value</span><span class="sxs-lookup"><span data-stu-id="bb28f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bb28f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb28f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb28f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb28f-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb28f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb28f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb28f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb28f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





