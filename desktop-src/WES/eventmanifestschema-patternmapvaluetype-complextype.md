---
title: Tipo complejo de PatternMapValueType
description: No se utiliza. Define las expresiones regulares que se usan para buscar una cadena coincidente en la cadena de mensaje y modificarla.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- PatternMapValueType tipo complejo EventLog
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800949"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="9f1ce-105">Tipo complejo de PatternMapValueType</span><span class="sxs-lookup"><span data-stu-id="9f1ce-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="9f1ce-106">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9f1ce-106">Not used.</span></span> <span data-ttu-id="9f1ce-107">Define las expresiones regulares que se usan para buscar una cadena coincidente en la cadena de mensaje y modificarla.</span><span class="sxs-lookup"><span data-stu-id="9f1ce-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="9f1ce-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9f1ce-108">Attributes</span></span>



| <span data-ttu-id="9f1ce-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="9f1ce-109">Name</span></span>  | <span data-ttu-id="9f1ce-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f1ce-110">Type</span></span>   | <span data-ttu-id="9f1ce-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f1ce-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f1ce-112">name</span><span class="sxs-lookup"><span data-stu-id="9f1ce-112">name</span></span>  | <span data-ttu-id="9f1ce-113">string</span><span class="sxs-lookup"><span data-stu-id="9f1ce-113">string</span></span> | <span data-ttu-id="9f1ce-114">Expresión regular utilizada para buscar una cadena coincidente en la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f1ce-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="9f1ce-115">value</span><span class="sxs-lookup"><span data-stu-id="9f1ce-115">value</span></span> | <span data-ttu-id="9f1ce-116">string</span><span class="sxs-lookup"><span data-stu-id="9f1ce-116">string</span></span> | <span data-ttu-id="9f1ce-117">Expresión regular que se usa para modificar la cadena coincidente que se encontró en la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f1ce-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9f1ce-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f1ce-118">Requirements</span></span>



| <span data-ttu-id="9f1ce-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f1ce-119">Requirement</span></span> | <span data-ttu-id="9f1ce-120">Value</span><span class="sxs-lookup"><span data-stu-id="9f1ce-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f1ce-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f1ce-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9f1ce-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9f1ce-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9f1ce-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f1ce-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9f1ce-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f1ce-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





