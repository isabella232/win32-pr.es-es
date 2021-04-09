---
title: Elemento patternMap (PatternMapListType)
description: Define una asignación entre dos expresiones regulares. Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- elemento patternMap EventLog
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078800"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="9e36e-105">Elemento patternMap (PatternMapListType)</span><span class="sxs-lookup"><span data-stu-id="9e36e-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="9e36e-106">Define una asignación entre dos expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="9e36e-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="9e36e-107">Una expresión se utiliza para buscar una cadena coincidente en la cadena de mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a colocar en la cadena de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9e36e-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="9e36e-108">El elemento **patternMap** se define mediante el tipo complejo de [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9e36e-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e36e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e36e-109">Requirements</span></span>



| <span data-ttu-id="9e36e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e36e-110">Requirement</span></span> | <span data-ttu-id="9e36e-111">Value</span><span class="sxs-lookup"><span data-stu-id="9e36e-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e36e-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e36e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9e36e-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9e36e-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e36e-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e36e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9e36e-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e36e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e36e-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e36e-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e36e-117">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="9e36e-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="9e36e-118">**patternMaps (NamedQueryType)**</span><span class="sxs-lookup"><span data-stu-id="9e36e-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





