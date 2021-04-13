---
title: Tipo complejo de PatternMapListType
description: No se utiliza. Define una lista de pares de expresiones regulares que se utilizan para modificar la cadena de mensaje.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- PatternMapListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359659"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="3255b-105">Tipo complejo de PatternMapListType</span><span class="sxs-lookup"><span data-stu-id="3255b-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="3255b-106">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3255b-106">Not used.</span></span> <span data-ttu-id="3255b-107">Define una lista de pares de expresiones regulares que se utilizan para modificar la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="3255b-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3255b-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3255b-108">Child elements</span></span>



| <span data-ttu-id="3255b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="3255b-109">Element</span></span>                                                                         | <span data-ttu-id="3255b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3255b-110">Type</span></span>                                                                     | <span data-ttu-id="3255b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3255b-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3255b-112">**patternMap**</span><span class="sxs-lookup"><span data-stu-id="3255b-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="3255b-113">**PatternMapType**</span><span class="sxs-lookup"><span data-stu-id="3255b-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="3255b-114">Define una asignación entre dos expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="3255b-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="3255b-115">Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="3255b-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="3255b-116">Se usa la primera asignación de patrones que coincide y no se intentan otros patrones.</span><span class="sxs-lookup"><span data-stu-id="3255b-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3255b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3255b-117">Requirements</span></span>



| <span data-ttu-id="3255b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3255b-118">Requirement</span></span> | <span data-ttu-id="3255b-119">Value</span><span class="sxs-lookup"><span data-stu-id="3255b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3255b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3255b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3255b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3255b-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3255b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3255b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3255b-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3255b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





